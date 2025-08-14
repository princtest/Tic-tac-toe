Custom+Order+Form+with+WhatsApp+Notification

Overview

This+code+creates+a+custom+order+form+that+sends+notifications+to+a+WhatsApp+number+when+a+user+submits+the+form.+The+form+has+fields+for+name,+email,+and+order+details,+and+uses+Node.js+and+the+WhatsApp+Business+API+to+send+notifications.

HTML+Form

The+HTML+form+is+designed+to+collect+user+input+for+name,+email,+and+order+details.+The+form+uses+the+POST+method+to+submit+data+to+the+Node.js+server.

Node.js+Server

The+Node.js+server+uses+Express.js+to+handle+form+submissions+and+send+notifications+to+WhatsApp+using+the+WhatsApp+Business+API.

Dependencies

express:+Node.js+web+framework

body-parser:+Middleware+to+parse+JSON+and+URL-encoded+bodies

whatsapp-web.js:+WhatsApp+Business+API+client

Server+Code

WhatsApp+Business+API

To+use+the+WhatsApp+Business+API,+you'll+need+to:

1.+Create+a+WhatsApp+Business+account

2.+Obtain+a+WhatsApp+Business+API+key

3.+Configure+the+API+key+in+your+Node.js+server

Deployment

To+deploy+your+project+online,+you+can+use+a+cloud+platform+like+Heroku+or+AWS.+You'll+need+to:

1.+Create+an+account+on+the+chosen+platform

2.+Create+a+new+app

3.+Link+your+GitHub+repository+to+the+app

Example+Use+Case

When+a+user+submits+the+form,+the+Node.js+server+will+receive+the+data+and+send+a+notification+to+the+specified+WhatsApp+number.+The+notification+will+include+the+user's+name+and+order+details.

I+hope+this+helps!+Let+me+know+if+you+have+any+questions+or+need+further+clarification.

Code+Structure

index.html:+HTML+form

server.js:+Node.js+server

package.json:+Dependencies+and+scripts

Commit+Message
Initial+commit:+Custom+order+form+with+WhatsApp+notification

API+Documentation

POST+/submit-order:+Submit+form+data+and+send+WhatsApp+notification

Order+place+hote+hi+customer+ke+WhatsApp+par+instant+notification+jaaye+—+is+repo+mein+pure+code,+Dockerfile,+CI+aur+step‑by‑step+setup+diya+hai.

Stack:+Node.js+(Express)+++WhatsApp+Cloud+API+(Meta),+Vanilla+HTML/JS+frontend.

Instant+WhatsApp+notification+to+customers+on+order+placement.

Features

Simple+order+form+(name,+phone,+address,+items)

Sends+template+message+via+WhatsApp+Cloud+API

Dockerfile+++docker-compose+for+easy+run

Minimal+CI+(GitHub+Actions)

Prerequisites

Node.js+18+

Meta+WhatsApp+Cloud+API+access

Setup+—+WhatsApp+Cloud+API

1.+Go+to+Meta+for+Developers+→+Add+WhatsApp+product.

2.+Create+or+use+a+System+User+and+generate+a+Permanent+Access+Token+with+whatsapp_business_messaging+++whatsapp_business_management.

3.+Note+your+Phone+Number+ID.

4.+Create+a+Message+Template+named+order_confirmation+(or+change+in+.env):

Hi+{{1}},+thanks+for+your+order+{{2}}+totaling+₹{{3}}.+Items:+{{4}}+Delivery+address:+{{5}}

5.+Add+your+number+as+test+recipient+(Dev+mode)+or+switch+to+Live+for+real+customers.

.env

Copy+.env.example+to+.env+and+fill+values.

🚀+Quick+Start

#+1)+Clone++
git+clone+https://github.com/your-username/whatsapp-order-notify.git++
cd+whatsapp-order-notify++
++
#+2)+Env+copy++
cp+.env.example+.env++
#+.env+file+me+WhatsApp+Cloud+API+ke+values+daal+do+(neeche+README+me+steps+hain)++
++
#+3)+Install++
+++++npm+install++
++
#+4)+Run+(dev)++
npm+run+dev++
#+ya++
npm+start++
++
#+5)+Open++
#+http://localhost:3000+par+order+Form+submit+WhatsApp+received+message.++
++
++
Docker++
++
docker+build+-t+wa-order+.++
docker+run+-p+3000:3000+--env-file+.env+wa-order++
++
Deploy+(Render+example)++
++
Create+a+Web+Service+from+this+repo++
++
Set+env+vars+from+.env++
++
Build+command:+npm+ci++
++
Start+command:+npm+start

Notes

Phone+format:+international+digits+(e.g.+919876543210).

Business-initiated+messages+require+approved+template.+If+user+messages+your+number+first+(24h+window),+you+can+send+free-form+text.

This+demo+stores+orders+to+orders.db.json+(local).+Use+a+database+for+production.

This+code+give+me+unique+design+GitHub+readme.md+format+code

