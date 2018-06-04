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

# D2D1_COMPOSITE_MODE enumeration


## -description


Used to specify the blend mode for all of the Direct2D blending operations.


## -enum-fields




### -field D2D1_COMPOSITE_MODE_SOURCE_OVER

The standard source-over-destination blend mode.


### -field D2D1_COMPOSITE_MODE_DESTINATION_OVER

The destination is rendered over the source.


### -field D2D1_COMPOSITE_MODE_SOURCE_IN

Performs a logical clip of the source pixels against the destination pixels.


### -field D2D1_COMPOSITE_MODE_DESTINATION_IN

The inverse of the <b>D2D1_COMPOSITE_MODE_SOURCE_IN</b> operation.


### -field D2D1_COMPOSITE_MODE_SOURCE_OUT

This is the logical inverse to <b>D2D1_COMPOSITE_MODE_SOURCE_IN</b>.


### -field D2D1_COMPOSITE_MODE_DESTINATION_OUT

The is the logical inverse to <b>D2D1_COMPOSITE_MODE_DESTINATION_IN</b>.


### -field D2D1_COMPOSITE_MODE_SOURCE_ATOP

Writes the source pixels over the destination where there are destination pixels.


### -field D2D1_COMPOSITE_MODE_DESTINATION_ATOP

The logical inverse of <b>D2D1_COMPOSITE_MODE_SOURCE_ATOP</b>.


### -field D2D1_COMPOSITE_MODE_XOR

The source is inverted with the destination.


### -field D2D1_COMPOSITE_MODE_PLUS

The channel components are summed.


### -field D2D1_COMPOSITE_MODE_SOURCE_COPY

The source is copied to the destination; the destination pixels are ignored.


### -field D2D1_COMPOSITE_MODE_BOUNDED_SOURCE_COPY

Equivalent to <b>D2D1_COMPOSITE_MODE_SOURCE_COPY</b>, but pixels outside of the source bounds are unchanged.



### -field D2D1_COMPOSITE_MODE_MASK_INVERT

Destination colors are inverted according to a source mask.



### -field D2D1_COMPOSITE_MODE_FORCE_DWORD




## -remarks



The figure here shows an example of each of the modes with images that have an opacity of 1.0 or 0.5. 

<img alt="An example image of each of the modes with opacity set to 1.0 or 0.5." src="images/composite_types.png"/>

There can be slightly different interpretations of these enumeration values depending on where the value is used.

<ul>
<li>
With a composite effect:

<b>D2D1_COMPOSITE_MODE_DESTINATION_COPY</b> is equivalent to <b>D2D1_COMPOSITE_MODE_SOURCE_COPY</b> with the inputs inverted.</li>
<li>


As a parameter to <a href="https://msdn.microsoft.com/c41d8a79-280a-451e-b07b-f904d07da5c7">ID2D1DeviceContext::DrawImage</a>: 
<b>D2D1_COMPOSITE_MODE_DESTINATION_COPY</b> is a no-op since the destination is already in the selected target.</li>
</ul>
<h3><a id="Sample_code"></a><a id="sample_code"></a><a id="SAMPLE_CODE"></a>Sample code</h3>
For an example that uses composite modes, download the <a href="http://go.microsoft.com/fwlink/p/?linkid=231580">Direct2D composite effect modes sample</a>.




## -see-also




<a href="https://msdn.microsoft.com/c41d8a79-280a-451e-b07b-f904d07da5c7">ID2D1DeviceContext::DrawImage</a>
 

 

