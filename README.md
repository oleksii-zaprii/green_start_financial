+-------------------------------------------------------+
|            customer_dashboard (Phoenix)               |
|-------------------------------------------------------|
| - Application Submission                              |
| - Authentication                                      |             
| - Customer Dashboard                                  |
+--------------------------+----------------------------+
                           |
                           |  Notifies about new applications
                           v
             +-------------+-------------+
             |    broker (RabbitMQ)      |
             |    (Message Broker)       |
             +-------------+-------------+
                           ^
                           |  Sends updates made by agent
                           |
+--------------------------+----------------------------+
|                agent_portal (Rails)                   |
|-------------------------------------------------------|
| - Application Review                                  |
| - Approve / Deny / Request Additional Info            |
+-------------------------------------------------------+
