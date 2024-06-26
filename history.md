# Work history
## Encompass systems
Requirements analyst, software developer and tester of a custom sales management system for a company that sold and supported third party software. I initially authored the first few iterations using Microsoft Visual Foxpro as requested by the client. However, due to performance limitations of Visual Foxpro, I rewrote and continued further iterations with Delphi for better performance. I learnt Delphi and was productive in a couple of weeks. The project used Delphi (which used object oriented Pascal) and SQL (using InterBase). 

## Hectronic GmbH (via PSI data systems)
Tech lead of team that developed Point of Sale cash register system software for Hectronic GmbH. I also wrote interfacing code for credit card terminals and fuel station pumps. Visited customer sites in Bonndorf, Germany for deeper understanding and integration. We used Delphi (object oriented pascal) and Sybase RDBMS with SQL.

## Wipro Infotech
Joined their newly created eCommerce division. Developed an intranet web based leave management system for the department. Used Microsoft ASP, COM and SQL server.

## HP India (via System Logic)
Worked on development of their ChangeEngine workflow/process management system. Visited HP Japan for requirements and technical discussions.

## John Deere
### Application information management system
John Deere had (and has) a vast dealer network. The dealers were installing updates via CDROMs received via mail. We wrote a software to deliver software updates faster over an occasionally connected, modem based low bandwidth internet. We used Microsoft VC++, COM and network programming. I was in charge of the network connectivity and file transfer parts of the project. In today's world, some background update components are included with most software, as part of the installer (such as installshield)

### JDLink 
I was part of John Deere's foray into telematics since the early days in 2000. We were focussed on optimized machine data telemetry. I started as the lead of the web team (using Microsoft ASP and SQL server) and we developed the web for reporting, notifications, management of machines, users, organizations. However, my parallel background in embedded computing and hardware led to the client requesting me to lead the On-machine software which was having some delays in development. This part of the system used C, C++, RTXC. Once I stabilized that part of the project, I was asked to lead the next weakest link, which was the communication server and data center software (before the term "cloud" became prevalent). This part of the system used Java, C++. I used UML (new at the time) to document the flows and iterate changes, to stabilize the system. In the data center, we introduced preaggregation for better report generation performance, of the most commonly used reports.
In our first versions, we collected basic information on hours of operation, exception conditions and implemented geofences. Over time, I was a big part of evolving the data collection to be highly configurable, with optional onboard data aggregation where we eventually collected hundreds of parameters (with customer approval). Over the years, I've worked with realtime operating systems such as RTXC, VxWorks, Windows CE. Our new versions are able to use linux with realtime extensions with the onboard hardware having evolved to have sufficient compute and memory. For communications, we evolved from analog data thru UDP thru TCP/IP to eventually using AWS IoT (using MQTT). During our initial days, I've been part of interface definition with Qualcomm using their telematics device. After some iterations, we evolved to have our own cellular modems on our machines. We have also had satellite communications via OrbComm. We now have an agreement with Starlink for future use.
Teamwise, initally we had our own teams for all parts of the project. In further iterations, we contracted a team for some parts of the on-machine software. However, as systems architect, I was always very involved with defining the behavior of the on-machine systems, all data interface definitions between machine and cloud, and high level flows in the cloud. It is a large distributed system with hundreds of thousands of devices.

### Agronomic data collection at Deere
John Deere has come a long way in the agronomic data journey. I joined the journey in 2003 when we were just starting development on windows CE based devices as on-machine computers for data storage, processing and visualization. I wrote the initial build management system (we now use off the shelf ones), wrote the first EndOfLine test software and participated in the first board bring up. Soon, we hired many new contractors and there was a void in interfacing with the new teams. I became the liasion between them, the SMEs and the systems architect and helped move the project along more smoothly. In later iterations, I became an architect on the system. I was in charge of defining data storage and transmission formats that would be efficient, be relatively easy to encode/decode and would be compatible with the then emerging standard of ISO11783-10 for agronomic data. I defined a system with schemas based in protobuf. The format is extremely compact on the wire and is capable of being processed at high speeds, but is very extensible for a wide range of data. It has withstood the test of time and is in production today, many years after I initially defined it. I was also the founding member of an interface review team to ensure that the various components of the system integrate well. We reviewed any proposed changes to the system interfaces (on-vehicle, cloud, mobile). I also consulted with data engineering teams in the cloud to help define optimum ways to store and flow the data thru the system. In one instance, I prototyped and showed how the compact format could be used to generate reports and maps on the fly with just a few EC2 instances, without expensive pre processing/pre aggregation. Many of those ideas have made it into production, to reduce costs in the processing pipeline.

### Intelligent fleetwide work control.
In agriculture, it is important that seeds and chemicals should be applied with the right rates. Double applications may result in reduced yields or for certain chemicals, may exceed the regulated range. For faster work, customers wanted to use multiple machines (sometimes with varying equipment sizes) on the same field, simultaneously or asynchronously. I architected a system to efficiently and quickly share data between machines with the cloud as an intermediary. Using this platform, the machines can work as a team, automatically stopping product application when driving over an area that has already been worked on with that product. This was very successful in the market. Customers love it and the most common feedback we got was "It just works !". One of the reasons for "it just works" was that I also designed a system to simulate machines sharing data. Originally, I made this to help the development teams test their work. However, later, we were able to modify it to simulate thousands of machines to load test the entire system. This, along with work by all the other excellent people on the team, helps us get the feedback of "it just works". 
Technology wise, we used C++, Qt on the on-machine computing device. For communications, we started with using WebSockets to the cloud. We have since transitioned to using AWS IoT with MQTT. At the cloud, we use various AWS components such as the AWS IoT rules engine, AWS SQS, AWS Kinesis, AWS S3, AWS lambda, AWS EC2, AWS dynamoDB, AWS Aurora. I wrote the simulation software in C#.


# How I do my best
Over the years, I have been fortunate to have honed a few skills
* The art of active listening.
* The art of asking questions. This helps me understand the customer, the ecosystem, the opportunities.
* The art of documenting software architecture artifacts to the degree needed.
* The art of analyis of system flows. The paths of least resistance and the paths with resistance / errors. Most bugs are worked out here, before they get a chance to come into existence.
* The art of discussing system flows with the various stakeholders, to the degree needed.
* The art of debugging, for the few bugs that inevitably come up.
* The art of being flexible. Filling gaps that have emerged. I've been a liason, I've provided feedback to stardards commitees, I've written simulations for testing, I've even traveled to Fargo,ND in winter for 3 months to get a project unstuck. While architecting is my forte, flexibility is my well, flex !

These, along with the fortune of having seen many systems that work well, enable me to stand on the shoulders of giants and do my best work. It has also been my fortune that all my employers have been a pleasure to work with so far.

# What I'd like to do
Over the years, I've understood that there are many axes of balance
* New technologies Vs using/extending existing ones
* Technology choice Vs developer availability / flexibility
* System complexity Vs reliability Vs competitive landscape
While these depend on the company and the situation, the common need is good initial analysis (not upto paralysis), choosing an initial architectural direction, defining interfaces well and being flexible to change as needed.
With those in mind, I'd be happy to work on any projects that require the services of a good systems architect. I'm comfortable in certain domains but flexible to expand to new domains. I am a very fast and deep learner.
