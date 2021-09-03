
https://www.calhoun.io/connecting-to-a-postgresql-database-with-gos-database-sql-package/
https://yourbasic.org/golang/day-of-week-int/
https://github.com/golang-standards/project-layout
https://medium.com/@bnprashanth256/reading-configuration-files-and-environment-variables-in-go-golang-c2607f912b63
https://dev.to/ilyakaznacheev/a-clean-way-to-pass-configs-in-a-go-application-1g64



SELECT count(*) from holidays where observed > now();

SELECT * from vacation_days ORDER BY dayoff;

SELECT count(*) from vacation_days where dayoff > now();

https://tapoueh.org/blog/2017/06/postgresql-and-the-calendar/

select date::date,
       extract('isodow' from date) as dow,
       to_char(date, 'dy') as day,
       extract('isoyear' from date) as "iso year",
       extract('week' from date) as week,
       extract('day' from
               (date + interval '2 month - 1 day')
              )
        as feb,
       extract('year' from date) as year,
       extract('day' from
               (date + interval '2 month - 1 day')
              ) = 29
       as leap
  from generate_series(date '2020-01-01',
                       date '2022-01-01',
                       interval '1 year')
       as t(date);
       # time-off
