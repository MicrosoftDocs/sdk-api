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

# _CSV_QUERY_VETO_FILE_DIRECT_IO_OUTPUT structure


## -description


Contains troubleshooting information about why a volume is in redirected mode.


## -struct-fields




### -field VetoedFromAltitudeIntegral

The integer portion of VetoedFromAltitude.


### -field VetoedFromAltitudeDecimal

The decimal portion of VetoedFromAltitude.


### -field Reason

The reason why volume is in a redirected mode.


## -remarks



CSV writes the troubleshooting strings to a diagnostic log that, when filtered, can provide hints as to why 
    a volume is in a redirected mode.




## -see-also




<a href="https://msdn.microsoft.com/bbde9dfb-c205-4432-be71-250d73b881f1">Volume Management Structures</a>
 

 

