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

# DWRITE_PANOSE_WEIGHT enumeration


## -description


The <b>DWRITE_PANOSE_WEIGHT</b> enumeration contains values that specify the weight of characters.


## -enum-fields




### -field DWRITE_PANOSE_WEIGHT_ANY

Any weight.


### -field DWRITE_PANOSE_WEIGHT_NO_FIT

No fit weight.


### -field DWRITE_PANOSE_WEIGHT_VERY_LIGHT

Very light weight.


### -field DWRITE_PANOSE_WEIGHT_LIGHT

Light weight.


### -field DWRITE_PANOSE_WEIGHT_THIN

Thin weight.


### -field DWRITE_PANOSE_WEIGHT_BOOK

Book weight.


### -field DWRITE_PANOSE_WEIGHT_MEDIUM

Medium weight.


### -field DWRITE_PANOSE_WEIGHT_DEMI

Demi weight.


### -field DWRITE_PANOSE_WEIGHT_BOLD

Bold weight.


### -field DWRITE_PANOSE_WEIGHT_HEAVY

Heavy weight.


### -field DWRITE_PANOSE_WEIGHT_BLACK

Black weight.


### -field DWRITE_PANOSE_WEIGHT_EXTRA_BLACK

Extra black weight.


### -field DWRITE_PANOSE_WEIGHT_NORD

Extra black weight.


## -remarks



The <b>DWRITE_PANOSE_WEIGHT</b> values roughly correspond to the <a href="https://msdn.microsoft.com/82396f80-eb62-4865-ba07-9653220c84f2">DWRITE_FONT_WEIGHT</a> values by using (panose_weight - 2) * 100 = font_weight.




## -see-also




<a href="https://msdn.microsoft.com/B65B4C8E-1CA0-47AC-AA3F-8F2EACC5C11A">DWRITE_PANOSE</a>
 

 

