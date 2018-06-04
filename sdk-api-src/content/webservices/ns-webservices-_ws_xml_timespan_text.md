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

# _WS_XML_TIMESPAN_TEXT structure


## -description



        Represents a time span formatted as the text "[+|-][d?.]HH:mm:ss[.fffffff]"
        <ul>
<li>d is a series of digits representing the day.
          </li>
<li>HH is a two digit number representing the hour of the day, from to 0 to 23.
          </li>
<li>mm is a two digit number representing the minute of the hour, from to 0 to 59.
          </li>
<li>ss is a two digit number representing the second of the minute, from to 0 to 59.
          </li>
<li>fffffff is up to 7 decimal digits representing the fraction of a second.
        </li>
</ul>



## -struct-fields




### -field text


          The base type for all types that derive from <a href="https://msdn.microsoft.com/430edd13-b664-4e10-8d61-ffa6a01dcb90">WS_XML_TEXT</a>.
        


### -field value

The timespan.

