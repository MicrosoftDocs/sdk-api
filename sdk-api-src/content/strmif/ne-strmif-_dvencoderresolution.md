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

# _DVENCODERRESOLUTION enumeration


## -description



Indicates the digital video (DV) encoding resolution.




## -enum-fields




### -field DVENCODERRESOLUTION_720x480

See Remarks.


### -field DVENCODERRESOLUTION_360x240

See Remarks.


### -field DVENCODERRESOLUTION_180x120

See Remarks.


### -field DVENCODERRESOLUTION_88x60

See Remarks.


## -remarks



The meaning of the enumeration elements depends on whether the current format is NTSC or PAL:

<table>
<tr>
<th>Element</th>
<th>NTSC</th>
<th>PAL</th>
</tr>
<tr>
<td>DVENCODERRESOLUTION_720x480</td>
<td>720 x 480</td>
<td>720 x 576</td>
</tr>
<tr>
<td>DVENCODERRESOLUTION_360x240</td>
<td>360 x 240</td>
<td>360 x 288</td>
</tr>
<tr>
<td>DVENCODERRESOLUTION_180x120</td>
<td>180 x 120</td>
<td>180 x 144</td>
</tr>
<tr>
<td>DVENCODERRESOLUTION_88x60</td>
<td>88 x 60</td>
<td>88 x 72</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>



<a href="https://msdn.microsoft.com/f193b76f-ca6a-44f5-b097-1570c4527ab4">IDVEnc Interface</a>
 

 

