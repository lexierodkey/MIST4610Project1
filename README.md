# MIST4610Project1

## Team Name: 
Sp24_61608_Group1

## Team Members:
- Dylan Palenik: [@DylanPalenik](https://github.com/dylanpalenik)
- Aakash Dholakia:[@AakashDholakia](https://github.com/AakashDholakia)
- Dan Kerik: 
- Hayley Daniels: [@hayleydaniels](https://github.com/hayleydaniels)
- Jordan Beal: 
- Lexie-Anne Rodkey: [@LexieRodkey](https://github.com/lexierodkey)

## Problem Description
The objective of this project is to model and develop a relational database that comprehensively covers all aspects of a soccer club’s operations. This includes Facilities, Training Sessions, Players, Managers, Squads, Matches, Sponsors, Injuries, and Player Stats. 

The database will be populated with valid sample data to reflect real-life scenarios and will be optimized for queries that help extract insights into player performance, squad efficiency, match outcomes, facility utilization, and the financial landscape of sponsorships.

By incorporating these entities and their relationships into the database, efficient management of club operations is ensured, encompassing tasks such as scheduling sessions, monitoring player participation, analyzing performance metrics, managing injuries, and facilitating sponsorship agreements. The database will serve as an informational hub for stakeholders and help the team make strategic decisions and achieve operational effectiveness within the soccer club

## Data Model 
Explanation of the data model:
The data model best suited for our soccer club scenario requires thirteen entities. These include Facilities, Training Sessions, Training Session Attendance, Coaches, Roster, Squad, Squad Composition, Matches, Match Sponsor, Sponsors, Injuries, Player Stats, and Statistic Type. Each of these entities must exist for this soccer club.

Starting with Facilities, each facility has its own specific name along with its type, location, and schedule information. Each facility can have multiple training sessions, and sometimes training sessions can exist without a facility, just like a facility can exist without any current training sessions. As such, having a non-identifying one-to-many relationship, in this case, allows for more flexibility and independence between these entities.
In regards to Training Sessions, each training session takes place in one facility, but can also have multiple individuals in attendance at these sessions. Multiple training sessions can have multiple attendees. Therefore, an associative entity called Training Session Attendance was created. This entity links the Training Sessions with the Roster entity. This Training Session Attendance entity allows users to view who is and is not attending each training session by receiving the primary keys from the associated entity as foreign keys.

The Roster entity is our main central entity which hosts information regarding the players in the club. This entity contains personal information regarding each player such as contact information and their nationality, and each athlete is identified by their playerID. As such, it is related to multiple other entities in many different ways. Players in the Roster can attend training sessions, be part of a Squad, have multiple injuries, and play multiple matches. The relationship between Roster and Training Sessions was previously mentioned as a many-to-many relationship with an associated entity named Training Session Attendance. The relationship between Roster and Squad is also a many-to-many identifying relationship. Therefore, the associative entity named Squad Composition was created. Many players can play on many squads.

In continuation, multiple players can play multiple matches, and multiple matches can have multiple players. Therefore, the relationship between Roster and Matches is also a many-to-many relationship. Because it is many-to-many, the associative entity labeled Player Stats was created. This entity contains the primary keys from Roster and Matches as foreign keys in itself. The Matches entity includes important information regarding the date, location, and scores, along with key figures including opponents and squads. There is also a one-to-many relationship between the entity called Statistic Type and Player Stats. The Statistic Type entity includes the specific type of statistic each player can obtain.

It should also be noted that players on Rosters can receive injuries through their time playing in the club. Therefore the relationship between Roster and Injury is one-to-many. One player can obtain multiple injuries.

Squads can consist of multiple players, multiple Coaches, and play multiple Matches. Therefore there are three relationships defined in this case. These include the previously mentioned many-to-many relation between Roster and Squad, a one-to-many non-identifying relationship between Squad and Coaches, and a one-to-many non-identifying relationship between Squad and Matches. Each Coach can manage multiple squads, but each squad may only have one coach. The Coaches entity contains relevant information regarding each coach such as their name, contact information, their position, and the squad they manage as a foreign key.

Finally, it’s worth mentioning that Matches can have multiple Sponsors and multiple Sponsors can sponsor multiple Matches. This calls for another associative entity to bridge the gap for the many-to-many relationship. This entity is named Match Sponsor. The Sponsor entity includes relevant information regarding each sponsor such as their name and amount.


Picture to data model: 

![image](https://github.com/lexierodkey/MIST4610Project1/assets/149977033/9890349a-6623-407c-bd19-9615462c778c)


## Data Dictionary

![image](https://github.com/lexierodkey/MIST4610Project1/assets/149977033/0a576a53-72e1-4f59-8b18-df9ddaa3bd03)

![image](https://github.com/lexierodkey/MIST4610Project1/assets/149977033/2bc8d3af-25b0-4d69-a559-c0d228dbc624)

![image](https://github.com/lexierodkey/MIST4610Project1/assets/149977033/988b2ea2-c28f-4d65-9633-78d76275e890)

![image](https://github.com/lexierodkey/MIST4610Project1/assets/149977033/ea03960d-b034-4c33-908c-03067f189c4b)

![image](https://github.com/lexierodkey/MIST4610Project1/assets/149977033/f71c2a7b-68b2-4866-9610-6783572cb412)

![image](https://github.com/lexierodkey/MIST4610Project1/assets/149977033/bcf63417-0e9f-4483-88d3-cac0fb3ab23f)

![image](https://github.com/lexierodkey/MIST4610Project1/assets/149977033/6538186b-5d5c-42ba-809c-42ba3e509405)

![image](https://github.com/lexierodkey/MIST4610Project1/assets/149977033/2ea314d1-028d-4368-9124-4beeb0c20972)

![image](https://github.com/lexierodkey/MIST4610Project1/assets/149977033/66f5706f-e69a-437a-95fc-c58be18a0a23)

![image](https://github.com/lexierodkey/MIST4610Project1/assets/149977033/b80dfa6d-dcb5-4ba0-9960-f71a0724a5a6)

![image](https://github.com/lexierodkey/MIST4610Project1/assets/149977033/8d42cc8c-7965-4590-ac05-1b5cc1896060)

![image](https://github.com/lexierodkey/MIST4610Project1/assets/149977033/982d3285-c64d-4831-a5ba-430910a8fc7c)

![image](https://github.com/lexierodkey/MIST4610Project1/assets/149977033/2007219e-d807-4fc1-8b88-0d0670d849c0)



## Queries: 

## Database information: 
Name of database: ns_Sp24_61608_Group1

