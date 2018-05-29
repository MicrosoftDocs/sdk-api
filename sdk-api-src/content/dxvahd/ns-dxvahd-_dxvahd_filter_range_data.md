---
UID: NS:dxvahd._DXVAHD_FILTER_RANGE_DATA
title: "_DXVAHD_FILTER_RANGE_DATA"
author: windows-sdk-content
description: Defines the range of supported values for an image filter.
old-location: mf\dxvahd_filter_range_data.htm
old-project: medfound
ms.assetid: cd349ac5-9825-4dc8-8735-5d846abb353b
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: DXVAHD_FILTER_RANGE_DATA, DXVAHD_FILTER_RANGE_DATA structure [Media Foundation], _DXVAHD_FILTER_RANGE_DATA, dxvahd/DXVAHD_FILTER_RANGE_DATA, mf.dxvahd_filter_range_data
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dxvahd.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DXVAHD_FILTER_RANGE_DATA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	dxvahd.h
api_name:
-	DXVAHD_FILTER_RANGE_DATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# _DXVAHD_FILTER_RANGE_DATA structure


## -description


Defines the range of supported values for an image filter.


## -struct-fields




### -field Minimum

The minimum value of the filter.


### -field Maximum

The maximum value of the filter.


### -field Default

The default value of the filter.


### -field Multiplier

A multiplier. Use the following formula to translate the filter setting into the actual filter value: <i>Actual Value</i> = <i>Set Value</i> × <i>Multiplier</i>.


## -remarks



The multiplier enables the filter range to have a fractional step value.

For example, a hue filter might have an actual range of [-180.0 ... +180.0] with a step size of 0.25. The device would report the following range and multiplier:

<ul>
<li>Minimum: -720</li>
<li>Maximum: +720</li>
<li>Multiplier: 0.25</li>
</ul>
In this case,  a filter value of 2 would be interpreted by the device as 0.50 (or 2 × 0.25).

The device should use  a multiplier that can be represented exactly as a base-2 fraction.




## -see-also




<a href="https://msdn.microsoft.com/38ebec28-c4fc-4e72-ac87-1e41707d1908">DXVA-HD</a>



<a href="https://msdn.microsoft.com/584c087e-53f0-42d8-99ed-a0d013379363">Direct3D Video Structures</a>



<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 

