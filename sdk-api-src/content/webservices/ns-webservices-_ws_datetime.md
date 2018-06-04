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

# _WS_DATETIME structure


## -description



        This structure is used to represent dates and times.
      


        Represents dates and times with values ranging from 12:00:00 midnight, 
        January 1, 0001 Anno Domini (Common Era) through 11:59:59 P.M., 
        December 31, 9999 A.D. (C.E.) to an accuracy of 100 nanoseconds.
      


        The functions <a href="https://msdn.microsoft.com/19e987d8-fe20-4bc6-a887-77bc1cfa65cf">WsDateTimeToFileTime</a> and <a href="https://msdn.microsoft.com/75a547f8-c8dc-47c3-97c9-2a39b046263f">WsFileTimeToDateTime</a> 
        can be used to convert a <b>WS_DATETIME</b> to and from a FILETIME.
      


## -struct-fields




### -field ticks


          The time in 100 nanosecond units, with 0 representing 12:00:00 midnight January 1, Anno Domini (Common Era).  The
          largest representable value is 3155378975999999999, which corresponds to 100 nanoseconds prior to 12:00:00 midnight
          January 1, 10000.
        


### -field format


          The format that is used when representing this time as text.
        

