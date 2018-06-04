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

# _DD_GETVPORTINPUTFORMATDATA structure


## -description


The DD_GETVPORTINPUTFORMATDATA structure contains the information required for the driver to return the input formats that the <a href="https://msdn.microsoft.com/a1de1905-09f3-4689-ace9-06690a1f930a">video port extensions (VPE)</a> object can accept.


## -struct-fields




### -field lpDD

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550595">DD_DIRECTDRAW_LOCAL</a> structure that is relevant to the current Microsoft DirectDraw process only. 


### -field lpVideoPort

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff551761">DD_VIDEOPORT_LOCAL</a> structure that represents this VPE object. 


### -field dwFlags

Indicates the type of formats for which support is being queried. This member can be one or more of the following values:

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>
DDVPFORMAT_VBI

</td>
<td>
The driver should return formats for the <a href="https://msdn.microsoft.com/a1de1905-09f3-4689-ace9-06690a1f930a">VBI</a> data.

</td>
</tr>
<tr>
<td>
DDVPFORMAT_VIDEO

</td>
<td>
The driver should return formats for the video data.

</td>
</tr>
</table>
 


### -field lpddpfFormat

Points to an array of <a href="https://msdn.microsoft.com/library/windows/hardware/ff550274">DDPIXELFORMAT</a> structures in which the driver should write the pixel formats supported by the VPE object. This member can be <b>NULL</b>.


### -field dwNumFormats

Specifies the location in which the driver should write the number of formats that the VPE object supports.


### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="https://msdn.microsoft.com/aac34116-a6a2-4d00-b0c4-87fac786b68d">DdVideoPortGetInputFormats</a> callback. A return code of DD_OK indicates success. For more information, see <a href="https://msdn.microsoft.com/da4cc7d7-6826-48aa-96c6-004e31fc3e3e">Return Values for DirectDraw</a>.


### -field GetVideoPortInputFormats

Used by the DirectDraw API and should not be filled in by the driver.


## -see-also




<a href="https://msdn.microsoft.com/aac34116-a6a2-4d00-b0c4-87fac786b68d">DdVideoPortGetInputFormats</a>
 

 

