REVENUE WEEK_Tuhrsday dan POO

SELECT 'Revenue' as [val_tipe],
       'Performance' as [tipe],
       year(doi) as [tahun_doi],
       month(doi) as [month_doi],
       Day([doi]) as [Date_doi],
       year(dot) as [tahun_dot],
       month(dot) as [month_dot],
             [DOI,[DOT],
       
       CASE 
    WHEN dot < DATEADD(DAY, 
                      (8 - DATEPART(WEEKDAY, CAST(CAST(YEAR(dot) AS VARCHAR) + '-01-01' AS DATE))) % 7, 
                      CAST(CAST(YEAR(dot) AS VARCHAR) + '-01-01' AS DATE))
    THEN 0
    ELSE DATEDIFF(WEEK, 
                  DATEADD(DAY, 
                          (8 - DATEPART(WEEKDAY, CAST(CAST(YEAR(dot) AS VARCHAR) + '-01-01' AS DATE))) % 7, 
                          CAST(CAST(YEAR(dot) AS VARCHAR) + '-01-01' AS DATE)), 
                  dot) + 1
END AS WEEK,

CASE 
        WHEN dot < DATEADD(DAY,
                           (5 - DATEPART(WEEKDAY, CAST(CAST(YEAR(dot) AS VARCHAR) + '-01-01' AS DATE)) + @@DATEFIRST + 7) % 7,
                           CAST(CAST(YEAR(dot) AS VARCHAR) + '-01-01' AS DATE))
        THEN 0
        ELSE DATEDIFF(WEEK,
                      DATEADD(DAY,
                              (5 - DATEPART(WEEKDAY, CAST(CAST(YEAR(dot) AS VARCHAR) + '-01-01' AS DATE)) + @@DATEFIRST + 7) % 7,
                              CAST(CAST(YEAR(dot) AS VARCHAR) + '-01-01' AS DATE)),
                      dot) + 1
    END AS [week_thursday],
       b.[region], 
       branch_office,CCY_SC, SUBCLASS,POI,SECTOR,TOURCODE,AC_TYPE,
       [platform],[AGEN_NO], [FAREBASIS],BO_POO,
case when branch_office = 'BKK' then 'TH'
when branch_office = 'BOM' then 'IN'
when branch_office = 'CMB' then 'LK'
when branch_office = 'KUL' then 'MY'
when branch_office = 'MNL' then 'PH'
when branch_office = 'SGN' then 'VN'
when branch_office = 'SIN' then 'SG'
when branch_office = 'BJS' then 'CN'
when branch_office = 'CAN' then 'CN'
when branch_office = 'CTU' then 'CN'
when branch_office = 'HKG' then 'HK'
when branch_office = 'SHA' then 'CN'
when branch_office = 'TPE' then 'TW'
when branch_office = 'AMI' then 'ID'
when branch_office = 'BMU' then 'ID'
when branch_office = 'DPS' then 'ID'
when branch_office = 'ENE' then 'ID'
when branch_office = 'KOE' then 'ID'
when branch_office = 'LBJ' then 'ID'
when branch_office = 'LOP' then 'ID'
when branch_office = 'AMS' then 'NL'
when branch_office = 'BRU' then 'BE'
when branch_office = 'FRA' then 'DE'
when branch_office = 'IST' then 'TR'
when branch_office = 'LON' then 'GB'
when branch_office = 'MAD' then 'ES'
when branch_office = 'PAR' then 'FR'
when branch_office = 'ROM' then 'IT'
when branch_office = 'STO' then 'SE'
when branch_office = 'VIE' then 'AT'
when branch_office = 'ZRH' then 'CH'
when branch_office = 'BDO' then 'ID'
when branch_office = 'JKT' then 'ID'
when branch_office = 'AUH' then 'AE'
when branch_office = 'DMM' then 'SA'
when branch_office = 'DOH' then 'QA'
when branch_office = 'HLP' then 'ID'
when branch_office = 'JED' then 'SA'
when branch_office = 'MED' then 'SA'
when branch_office = 'RUH' then 'SA'
when branch_office = 'FUK' then 'JP'
when branch_office = 'LAX' then 'US'
when branch_office = 'OSA' then 'JP'
when branch_office = 'SEL' then 'KR'
when branch_office = 'TYO' then 'JP'
when branch_office = 'BKS' then 'ID'
when branch_office = 'BTH' then 'ID'
when branch_office = 'BTJ' then 'ID'
when branch_office = 'DJB' then 'ID'
when branch_office = 'FLZ' then 'ID'
when branch_office = 'GNS' then 'ID'
when branch_office = 'LSW' then 'ID'
when branch_office = 'MES' then 'ID'
when branch_office = 'PDG' then 'ID'
when branch_office = 'PGK' then 'ID'
when branch_office = 'PKU' then 'ID'
when branch_office = 'PLM' then 'ID'
when branch_office = 'TJQ' then 'ID'
when branch_office = 'TKG' then 'ID'
when branch_office = 'TNJ' then 'ID'
when branch_office = 'BWX' then 'ID'
when branch_office = 'JOG' then 'ID'
when branch_office = 'MLG' then 'ID'
when branch_office = 'SOC' then 'ID'
when branch_office = 'SRG' then 'ID'
when branch_office = 'SUB' then 'ID'
when branch_office = 'ADL' then 'AU'
when branch_office = 'AKL' then 'NZ'
when branch_office = 'BNE' then 'AU'
when branch_office = 'MEL' then 'AU'
when branch_office = 'PER' then 'AU'
when branch_office = 'SYD' then 'AU'
when branch_office = 'AMQ' then 'ID'
when branch_office = 'BDJ' then 'ID'
when branch_office = 'BEJ' then 'ID'
when branch_office = 'BIK' then 'ID'
when branch_office = 'BPN' then 'ID'
when branch_office = 'BUW' then 'ID'
when branch_office = 'DJJ' then 'ID'
when branch_office = 'GTO' then 'ID'
when branch_office = 'KDI' then 'ID'
when branch_office = 'KTG' then 'ID'
when branch_office = 'LLO' then 'ID'
when branch_office = 'MDC' then 'ID'
when branch_office = 'MJU' then 'ID'
when branch_office = 'MKQ' then 'ID'
when branch_office = 'MKW' then 'ID'
when branch_office = 'NBX' then 'ID'
when branch_office = 'PKY' then 'ID'
when branch_office = 'PLW' then 'ID'
when branch_office = 'PNK' then 'ID'
when branch_office = 'SOQ' then 'ID'
when branch_office = 'SRI' then 'ID'
when branch_office = 'TIM' then 'ID'
when branch_office = 'TRK' then 'ID'
when branch_office = 'TTE' then 'ID'
when branch_office = 'UPG' then 'ID'
when branch_office = 'MOW' then 'RU'
else [branch_office] end as country,
       case when [grouping_channel] is null then 'Travel Agent'
	   when AGEN_NO = '1531406' or AGEN_NO = '1531447' then 'OTA'  
            else [grouping_channel] end as [grouping_channel],
       [servicetypecode],
       [subservicecode],
       [route_vv],
       [agent_grouping],
	   sum(GROSS_IDR) as GROSS_IDR, sum(DISC_IDR) as DISC_IDR, sum(COMM_IDR) as COMM_IDR, 
	   sum(YQ_IDR) as YQ_IDR, sum(GROSS_USD) as GROSS_USD, sum(DISC_USD) as DISC_USD, sum(COMM_USD) as COMM_USD, 
	   sum(YQ_USD) as YQ_USD,
       sum( isnull(a.GROSS_USD,0)-isnull(DISC_USD,0)+ isnull(a.YQ_USD,0)) as revusd,
       count(*) AS pax
FROM   alflown2025 a
left join Reff_BO b on a.branch_office = b.BO
left join reff_grouping_channel_temp c on a.channel = c.Channel
WHERE   CPNSTS in ('flown', 'Unutilised')  and a.DOCTYPE in( 'PAX','FIM') and a.OPRT_ALN != 's'
GROUP  BY [agent_grouping],
          dot,
          b.[region], 
          a.branch_office,CCY_SC, SUBCLASS,POI,SECTOR,TOURCODE,AC_TYPE,
          c.[platform],
          [servicetypecode],
          [subservicecode],
          [route_vv],
          [grouping_channel] ,[AGEN_NO], [FAREBASIS],BO_POO,
  CASE 
      WHEN dot < DATEADD(DAY, 
                         (8 - DATEPART(WEEKDAY, CAST(CAST(YEAR(dot) AS VARCHAR) + '-01-01' AS DATE))) % 7, 
                         CAST(CAST(YEAR(dot) AS VARCHAR) + '-01-01' AS DATE))
      THEN 0
      ELSE DATEDIFF(WEEK, 
                    DATEADD(DAY, 
                            (8 - DATEPART(WEEKDAY, CAST(CAST(YEAR(dot) AS VARCHAR) + '-01-01' AS DATE))) % 7, 
                            CAST(CAST(YEAR(dot) AS VARCHAR) + '-01-01' AS DATE)), 
                    dot) + 1
  END,

  CASE 
        WHEN dot < DATEADD(DAY,
                           (5 - DATEPART(WEEKDAY, CAST(CAST(YEAR(dot) AS VARCHAR) + '-01-01' AS DATE)) + @@DATEFIRST + 7) % 7,
                           CAST(CAST(YEAR(dot) AS VARCHAR) + '-01-01' AS DATE))
        THEN 0
        ELSE DATEDIFF(WEEK,
                      DATEADD(DAY,
                              (5 - DATEPART(WEEKDAY, CAST(CAST(YEAR(dot) AS VARCHAR) + '-01-01' AS DATE)) + @@DATEFIRST + 7) % 7,
                              CAST(CAST(YEAR(dot) AS VARCHAR) + '-01-01' AS DATE)),
                      dot) + 1
    END
	

union

SELECT 'Revenue' as [val_tipe],
       'Performance' as [tipe],
       year(dot) as [tahun],
       month(dot) as [month],
       Day([dot])     AS Date,
  CASE 
      WHEN dot < DATEADD(DAY, 
                         (8 - DATEPART(WEEKDAY, CAST(CAST(YEAR(dot) AS VARCHAR) + '-01-01' AS DATE))) % 7, 
                         CAST(CAST(YEAR(dot) AS VARCHAR) + '-01-01' AS DATE))
      THEN 0
      ELSE DATEDIFF(WEEK, 
                    DATEADD(DAY, 
                            (8 - DATEPART(WEEKDAY, CAST(CAST(YEAR(dot) AS VARCHAR) + '-01-01' AS DATE))) % 7, 
                            CAST(CAST(YEAR(dot) AS VARCHAR) + '-01-01' AS DATE)), 
                    dot) + 1
  END AS WEEK,

  CASE 
        WHEN dot < DATEADD(DAY,
                           (5 - DATEPART(WEEKDAY, CAST(CAST(YEAR(dot) AS VARCHAR) + '-01-01' AS DATE)) + @@DATEFIRST + 7) % 7,
                           CAST(CAST(YEAR(dot) AS VARCHAR) + '-01-01' AS DATE))
        THEN 0
        ELSE DATEDIFF(WEEK,
                      DATEADD(DAY,
                              (5 - DATEPART(WEEKDAY, CAST(CAST(YEAR(dot) AS VARCHAR) + '-01-01' AS DATE)) + @@DATEFIRST + 7) % 7,
                              CAST(CAST(YEAR(dot) AS VARCHAR) + '-01-01' AS DATE)),
                      dot) + 1
    END AS [week_thursday],

       b.[region], 
       branch_office,CCY_SC, SUBCLASS,POI,SECTOR,TOURCODE,AC_TYPE,
       [platform],[AGEN_NO], [FAREBASIS],BO_POO,
	   case when branch_office = 'BKK' then 'TH'
when branch_office = 'BOM' then 'IN'
when branch_office = 'CMB' then 'LK'
when branch_office = 'KUL' then 'MY'
when branch_office = 'MNL' then 'PH'
when branch_office = 'SGN' then 'VN'
when branch_office = 'SIN' then 'SG'
when branch_office = 'BJS' then 'CN'
when branch_office = 'CAN' then 'CN'
when branch_office = 'CTU' then 'CN'
when branch_office = 'HKG' then 'HK'
when branch_office = 'SHA' then 'CN'
when branch_office = 'TPE' then 'TW'
when branch_office = 'AMI' then 'ID'
when branch_office = 'BMU' then 'ID'
when branch_office = 'DPS' then 'ID'
when branch_office = 'ENE' then 'ID'
when branch_office = 'KOE' then 'ID'
when branch_office = 'LBJ' then 'ID'
when branch_office = 'LOP' then 'ID'
when branch_office = 'AMS' then 'NL'
when branch_office = 'BRU' then 'BE'
when branch_office = 'FRA' then 'DE'
when branch_office = 'IST' then 'TR'
when branch_office = 'LON' then 'GB'
when branch_office = 'MAD' then 'ES'
when branch_office = 'PAR' then 'FR'
when branch_office = 'ROM' then 'IT'
when branch_office = 'STO' then 'SE'
when branch_office = 'VIE' then 'AT'
when branch_office = 'ZRH' then 'CH'
when branch_office = 'BDO' then 'ID'
when branch_office = 'JKT' then 'ID'
when branch_office = 'AUH' then 'AE'
when branch_office = 'DMM' then 'SA'
when branch_office = 'DOH' then 'QA'
when branch_office = 'HLP' then 'ID'
when branch_office = 'JED' then 'SA'
when branch_office = 'MED' then 'SA'
when branch_office = 'RUH' then 'SA'
when branch_office = 'FUK' then 'JP'
when branch_office = 'LAX' then 'US'
when branch_office = 'OSA' then 'JP'
when branch_office = 'SEL' then 'KR'
when branch_office = 'TYO' then 'JP'
when branch_office = 'BKS' then 'ID'
when branch_office = 'BTH' then 'ID'
when branch_office = 'BTJ' then 'ID'
when branch_office = 'DJB' then 'ID'
when branch_office = 'FLZ' then 'ID'
when branch_office = 'GNS' then 'ID'
when branch_office = 'LSW' then 'ID'
when branch_office = 'MES' then 'ID'
when branch_office = 'PDG' then 'ID'
when branch_office = 'PGK' then 'ID'
when branch_office = 'PKU' then 'ID'
when branch_office = 'PLM' then 'ID'
when branch_office = 'TJQ' then 'ID'
when branch_office = 'TKG' then 'ID'
when branch_office = 'TNJ' then 'ID'
when branch_office = 'BWX' then 'ID'
when branch_office = 'JOG' then 'ID'
when branch_office = 'MLG' then 'ID'
when branch_office = 'SOC' then 'ID'
when branch_office = 'SRG' then 'ID'
when branch_office = 'SUB' then 'ID'
when branch_office = 'ADL' then 'AU'
when branch_office = 'AKL' then 'NZ'
when branch_office = 'BNE' then 'AU'
when branch_office = 'MEL' then 'AU'
when branch_office = 'PER' then 'AU'
when branch_office = 'SYD' then 'AU'
when branch_office = 'AMQ' then 'ID'
when branch_office = 'BDJ' then 'ID'
when branch_office = 'BEJ' then 'ID'
when branch_office = 'BIK' then 'ID'
when branch_office = 'BPN' then 'ID'
when branch_office = 'BUW' then 'ID'
when branch_office = 'DJJ' then 'ID'
when branch_office = 'GTO' then 'ID'
when branch_office = 'KDI' then 'ID'
when branch_office = 'KTG' then 'ID'
when branch_office = 'LLO' then 'ID'
when branch_office = 'MDC' then 'ID'
when branch_office = 'MJU' then 'ID'
when branch_office = 'MKQ' then 'ID'
when branch_office = 'MKW' then 'ID'
when branch_office = 'NBX' then 'ID'
when branch_office = 'PKY' then 'ID'
when branch_office = 'PLW' then 'ID'
when branch_office = 'PNK' then 'ID'
when branch_office = 'SOQ' then 'ID'
when branch_office = 'SRI' then 'ID'
when branch_office = 'TIM' then 'ID'
when branch_office = 'TRK' then 'ID'
when branch_office = 'TTE' then 'ID'
when branch_office = 'UPG' then 'ID'
when branch_office = 'MOW' then 'RU'
else [branch_office] end as country,
       case when [grouping_channel] is null then 'Travel Agent'
	   when AGEN_NO = '1531406' or AGEN_NO = '1531447' then 'OTA' 
            else [grouping_channel] end as [grouping_channel],
       [servicetypecode],
       [subservicecode],
       [route_vv],
       [agent_grouping],
	   sum(GROSS_IDR) as GROSS_IDR, sum(DISC_IDR) as DISC_IDR, sum(COMM_IDR) as COMM_IDR, 
	   sum(YQ_IDR) as YQ_IDR, sum(GROSS_USD) as GROSS_USD, sum(DISC_USD) as DISC_USD, sum(COMM_USD) as COMM_USD, 
	   sum(YQ_USD) as YQ_USD,
       sum( isnull(a.GROSS_USD,0)-isnull(DISC_USD,0)+ isnull(a.YQ_USD,0)) as revusd,
       count(*) AS pax
FROM   alflown2024 a
left join Reff_BO b on a.branch_office = b.BO
left join reff_grouping_channel_temp c on a.channel = c.Channel
WHERE   CPNSTS in ('flown', 'Unutilised')  and a.DOCTYPE in( 'PAX','FIM') and a.OPRT_ALN != 's'
and dot <=  dateadd(year, -1, (select max(dot) from alflown2025))
GROUP  BY [agent_grouping],
          dot,
          b.[region], 
          a.branch_office,CCY_SC, SUBCLASS,POI,SECTOR,TOURCODE,AC_TYPE,
          c.[platform],
          [servicetypecode],
          [subservicecode],
          [route_vv],
          [grouping_channel] ,[AGEN_NO], [FAREBASIS], BO_POO,
  CASE 
      WHEN dot < DATEADD(DAY, 
                         (8 - DATEPART(WEEKDAY, CAST(CAST(YEAR(dot) AS VARCHAR) + '-01-01' AS DATE))) % 7, 
                         CAST(CAST(YEAR(dot) AS VARCHAR) + '-01-01' AS DATE))
      THEN 0
      ELSE DATEDIFF(WEEK, 
                    DATEADD(DAY, 
                            (8 - DATEPART(WEEKDAY, CAST(CAST(YEAR(dot) AS VARCHAR) + '-01-01' AS DATE))) % 7, 
                            CAST(CAST(YEAR(dot) AS VARCHAR) + '-01-01' AS DATE)), 
                    dot) + 1
  END,

  CASE 
        WHEN dot < DATEADD(DAY,
                           (5 - DATEPART(WEEKDAY, CAST(CAST(YEAR(dot) AS VARCHAR) + '-01-01' AS DATE)) + @@DATEFIRST + 7) % 7,
                           CAST(CAST(YEAR(dot) AS VARCHAR) + '-01-01' AS DATE))
        THEN 0
        ELSE DATEDIFF(WEEK,
                      DATEADD(DAY,
                              (5 - DATEPART(WEEKDAY, CAST(CAST(YEAR(dot) AS VARCHAR) + '-01-01' AS DATE)) + @@DATEFIRST + 7) % 7,
                              CAST(CAST(YEAR(dot) AS VARCHAR) + '-01-01' AS DATE)),
                      dot) + 1
    END

union

SELECT 'Revenue' as [val_tipe],
       'Target' as [tipe],
       2025 as [tahun], a.[Month], 
       1     AS Date, 1 as WEEK, 1 as [week_thursday],
       b.[region], 
       branch_office,
       a.[platform],'','','','','','','','','','','','','','','','','',
       a.Channel_Masking, svc, a.subSvc, a.routevv,'',
       sum(a.revenue) as revusd,
       sum(a.pax) AS pax,
	   '' as BO_POO
FROM budget_bo_2024 a
left join Reff_BO b on a.branch_office = b.BO
left join reff_grouping_channel_temp c on a.channel = c.Channel
GROUP  BY b.[region], a.[Month],
          a.branch_office,
          a.[platform],
          svc, a.subSvc, a.routevv, a.Channel_Masking
