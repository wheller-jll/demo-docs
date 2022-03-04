# Azara Lease Foundational Subject Area
![ERD](lease.png)

[areas](#areas)

[locations](#locations)


## **areas**
### Layout
| Keys | Field Name | Mappings |
|---|---|---|
|🔑|TENURE_HASH_KEY| [mappings](#TOTAL_SF)|
||TOTAL|FLOAT|Blah Blah Blah||
||TOTAL_SF|NULL||
||TOTAL_SM|NULL||
||BUILDING|NULL||
||BUILDING_SF|NULL||
||BUILDING_SM|NULL||
||LAND|NULL||
||LAND_SF|NULL||
||LAND_SM|NULL||
||TYPE|NULL||
||VACANT|NULL||
||VACANT_SF|NULL||
||VACANT_SM|NULL||

### Mappings
#### TOTAL_SF
> This is the total sf for the lease
##### Archibus
| Attribute | Value |
|---|---|
|Method|Calculation|
|Datatype|Float|
|Source|[Link](\sources\Archibus\Archibus.md#abus_table)|

```
case
    when archibus.attribute = 'SQFT' then archibus.attribute
    when archibus.attribute = 'SQM' then archibus.attribute * 10.764
    else null
end
```
##### OVLA
| Attribute | Value |
|---|---|
|Method|Calculation|
|Datatype|Float|
|Source|[Link](\sources\OVLA\OVLA.md#here)|
```
case
    when ovla.attribute = 'SQFT' then ovla.attribute
    when ovla.attribute = 'SQM' then ovla.attribute * 10.764
    else null
end
```
## locations
## tenures
## locations
## properties
## organizations
## tasks
## task_categories
## task_costs
## cost_schedules
## costs