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

# ColorCorrectPalette function


## -description


The <b>ColorCorrectPalette</b> function corrects the entries of a palette using the WCS 1.0 parameters in the specified device context.


## -parameters




### -param hdc

TBD


### -param hPal

TBD


### -param deFirst

TBD


### -param num

TBD




#### - dwFirstEntry

Specifies the first entry in the palette to be color corrected.


#### - dwNumOfEntries

Specifies the number of entries to color correct.


#### - hDC

Specifies a device context whose WCS parameters to use.


#### - hPalette

Specifies the handle to the palette to be color corrected.


## -returns



If this function succeeds, the return value is <b>TRUE</b>.

If this function fails, the return value is <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>
 

 

