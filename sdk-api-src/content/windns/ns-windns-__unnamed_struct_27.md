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

# DNS_LOC_DATA structure


## -description


The 
<b>DNS_LOC_DATA</b> structure represents a DNS location (LOC) resource record (RR) as specified in <a href=" http://go.microsoft.com/fwlink/p/?linkid=106954">RFC 1876</a>.


## -struct-fields




### -field wVersion

The version number of the representation. Must be zero.


### -field wSize

The diameter of a sphere enclosing the described entity, defined as "SIZE"         in section 2 of <a href=" http://go.microsoft.com/fwlink/p/?linkid=106954">RFC 1876</a>.


### -field wHorPrec

The horizontal data precision, defined as "HORIZ PRE"         in section 2 of <a href=" http://go.microsoft.com/fwlink/p/?linkid=106954">RFC 1876</a>.


### -field wVerPrec

The vertical data precision, defined as "VERT PRE"         in section 2 of <a href=" http://go.microsoft.com/fwlink/p/?linkid=106954">RFC 1876</a>.


### -field dwLatitude

The latitude of the center of the sphere, defined as "LATITUDE"         in section 2 of <a href=" http://go.microsoft.com/fwlink/p/?linkid=106954">RFC 1876</a>.


### -field dwLongitude

The longitude of the center of the sphere, defined as "LONGITUDE"         in section 2 of <a href=" http://go.microsoft.com/fwlink/p/?linkid=106954">RFC 1876</a>.


### -field dwAltitude

The altitude of the center of the sphere, defined as "ALTITUDE"         in section 2 of <a href=" http://go.microsoft.com/fwlink/p/?linkid=106954">RFC 1876</a>.


## -remarks



The 
<b>DNS_LOC_DATA</b> structure is used in conjunction with the 
<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a> structure to programmatically manage DNS entries.




## -see-also




<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a>
 

 

