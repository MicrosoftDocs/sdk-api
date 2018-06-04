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

# D3D11_VIDEO_PROCESSOR_FILTER_RANGE structure


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

For example, a hue filter might have an actual range of [–180.0 ... +180.0] with a step size of 0.25. The device would report the following range and multiplier:

<ul>
<li>Minimum: –720</li>
<li>Maximum: +720</li>
<li>Multiplier: 0.25</li>
</ul>
In this case,  a filter value of 2 would be interpreted by the device as 0.50 (or 2 × 0.25).

The device should use  a multiplier that can be represented exactly as a base-2 fraction.




## -see-also




<a href="https://msdn.microsoft.com/416159A4-F50E-4027-9367-727BA81D2A21">Direct3D 11 Video Structures</a>



<a href="https://msdn.microsoft.com/F43A01D7-A0FE-4509-B3B2-094B09A7F04A">ID3D11VideoProcessorEnumerator::GetVideoProcessorFilterRange</a>
 

 

