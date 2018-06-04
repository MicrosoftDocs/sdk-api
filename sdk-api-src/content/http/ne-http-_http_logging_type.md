---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _HTTP_LOGGING_TYPE enumeration


## -description


The <b>HTTP_LOGGING_TYPE</b> enumeration defines the type of logging that is performed.

This enumeration is used  in the <a href="https://msdn.microsoft.com/12e12f83-c36a-4b4e-8890-50566cf00c2b">HTTP_LOGGING_INFO</a> structure.


## -enum-fields




### -field HttpLoggingTypeW3C

The log format is W3C style extended logging. Applications choose the fields that are logged in the  <b>Fields</b> member of the <a href="https://msdn.microsoft.com/12e12f83-c36a-4b4e-8890-50566cf00c2b">HTTP_LOGGING_INFO</a> structure.

 When this type of logging is set on a URL Group, logging is similar to the IIS6 site logging. When set on a server session this format functions as a centralized logging for all of the URL Groups.


### -field HttpLoggingTypeIIS

The log format is IIS5/6 style logging. This format has a fixed field definition; applications cannot choose which fields are logged. This format cannot be chosen when setting the logging property on a server session.


### -field HttpLoggingTypeNCSA

The log format is NCSA style logging. This format has a fixed field definition; applications cannot choose which fields are logged. This format cannot be chosen when setting the logging property on a server session.


### -field HttpLoggingTypeRaw

The log format is centralized binary logging. This format has a fixed field definition; applications cannot choose which fields are logged. This format cannot be chosen when setting the logging property on a URL Group. 


## -remarks



The log files are named based on the rollover type and logging format as shown in  the following table.


<table>
<tr>
<th>Format</th>
<th>Rollover  Type </th>
<th>Filename Pattern</th>
</tr>
<tr>
<td>Microsoft IIS Log Format</td>
<td>Size</td>
<td>inetsvnn.log</td>
</tr>
<tr>
<td></td>
<td>Hourly</td>
<td>inyymmddhh.log</td>
</tr>
<tr>
<td></td>
<td>Daily</td>
<td>inyymmdd.log</td>
</tr>
<tr>
<td></td>
<td>Weekly</td>
<td>inymmww.log</td>
</tr>
<tr>
<td></td>
<td>Monthly</td>
<td>inyymm.log</td>
</tr>
<tr>
<td>NCSA Common Log File Format</td>
<td>Size</td>
<td>ncsann.log
</td>
</tr>
<tr>
<td></td>
<td>Hourly</td>
<td>ncyymmddhh.log</td>
</tr>
<tr>
<td></td>
<td>Daily</td>
<td>ncyymmdd.log</td>
</tr>
<tr>
<td></td>
<td>Weekly</td>
<td>ncyymmww.log</td>
</tr>
<tr>
<td></td>
<td>Monthly</td>
<td>ncyymm.log</td>
</tr>
<tr>
<td>W3C Extended Log File Format</td>
<td>Size</td>
<td>extendnn.log</td>
</tr>
<tr>
<td></td>
<td>Hourly</td>
<td>exyymmddhh.log</td>
</tr>
<tr>
<td></td>
<td>Daily</td>
<td>exyymmdd.log</td>
</tr>
<tr>
<td></td>
<td>Weekly</td>
<td>exyymmww.log</td>
</tr>
<tr>
<td></td>
<td>Monthly</td>
<td>exyymm.log</td>
</tr>
</table>
 



The following table lists time element characters and what they represent. <table>
<tr>
<th>Item</th>
<th>Description </th>
</tr>
<tr>
<td>yy</td>
<td>The two digit representation of the year.</td>
</tr>
<tr>
<td>mm</td>
<td>The two digit representation of the month.</td>
</tr>
<tr>
<td>ww</td>
<td>The two digit representation of the week.</td>
</tr>
<tr>
<td>dd</td>
<td>The two digit representation of the day.</td>
</tr>
<tr>
<td>hh</td>
<td>The two digit representation of the hour in 24 hour notation.</td>
</tr>
<tr>
<td>nn</td>
<td>The two digit representation of the numerical sequence.</td>
</tr>
</table>
 



For more information about the log file formats, see <a href="Http://go.microsoft.com/fwlink/p/?linkid=83889">IIS Log File Formats</a>.




## -see-also




<a href="https://msdn.microsoft.com/849b88a1-e60b-4a1d-a660-cc3fe429d39f">HTTP Server API Version 2.0 Enumeration Types</a>



<a href="https://msdn.microsoft.com/12e12f83-c36a-4b4e-8890-50566cf00c2b">HTTP_LOGGING_INFO</a>
 

 

