---
UID: NS:ocidl.tagPOINTF
title: POINTF (ocidl.h)
author: windows-sdk-content
description: Contains information that is used to convert between container units, expressed in floating point, and control units, expressed in HIMETRIC.
old-location: com\pointf.htm
tech.root: com
ms.assetid: 2b201df8-efee-4302-a93c-b514b982cf2b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPPOINTF, LPPOINTF, LPPOINTF structure pointer [COM], POINTF, POINTF structure [COM], _ole_POINTF, com.pointf, ocidl/LPPOINTF, ocidl/POINTF"
ms.topic: struct
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - OCIdl.h
api_name:
 - POINTF
product: Windows
targetos: Windows
req.typenames: POINTF, *LPPOINTF
req.redist: 
---

# POINTF structure


## -description


Contains information that is used to convert between container units, expressed in floating point, and control units, expressed in <b>HIMETRIC</b>. The <b>POINTF</b> structure specifically holds the floating point container units. Controls do not attempt to interpret either value in the structure.




## -struct-fields




### -field x

The x coordinates of the point in units that the container finds convenient.


### -field y

The y coordinates of the point in units that the container finds convenient.



## -see-also




<a href="https://msdn.microsoft.com/c7add062-4b42-43be-a982-c881c947f8f0">IOleControlSite::TransformCoords</a>
 

 

