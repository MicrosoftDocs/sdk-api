---
UID: NS:ddrawint._DD_GETVPORTINPUTFORMATDATA
title: "_DD_GETVPORTINPUTFORMATDATA"
author: windows-sdk-content
description: The DD_GETVPORTINPUTFORMATDATA structure contains the information required for the driver to return the input formats that the video port extensions (VPE) object can accept.
old-location: display\dd_getvportinputformatdata.htm
tech.root: display
ms.assetid: d8cdfb24-0914-4e1f-bbdd-7bba31976ba0
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "*PDD_GETVPORTINPUTFORMATDATA, DD_GETVPORTINPUTFORMATDATA, DD_GETVPORTINPUTFORMATDATA structure [Display Devices], _DD_GETVPORTINPUTFORMATDATA, ddrawint/DD_GETVPORTINPUTFORMATDATA, ddstrcts_c9ca2266-9add-4320-8b29-51d67b121957.xml, display.dd_getvportinputformatdata"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ddrawint.h
req.include-header: Winddi.h
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ddrawint.h
api_name:
 - DD_GETVPORTINPUTFORMATDATA
product: Windows
targetos: Windows
req.typenames: "*PDD_GETVPORTINPUTFORMATDATA, DD_GETVPORTINPUTFORMATDATA"
req.redist: 
---

# _DD_GETVPORTINPUTFORMATDATA structure


## -description


The DD_GETVPORTINPUTFORMATDATA structure contains the information required for the driver to return the input formats that the <a href="https://msdn.microsoft.com/a1de1905-09f3-4689-ace9-06690a1f930a">video port extensions (VPE)</a> object can accept.


## -struct-fields




### -field lpDD

Points to a <a href="https://msdn.microsoft.com/58e378b7-863a-46d4-91cb-904ed4e892a3">DD_DIRECTDRAW_LOCAL</a> structure that is relevant to the current Microsoft DirectDraw process only. 


### -field lpVideoPort

Points to a <a href="https://msdn.microsoft.com/c497d1ef-0eb1-465f-978c-60cf5606de93">DD_VIDEOPORT_LOCAL</a> structure that represents this VPE object. 


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

Points to an array of <a href="https://msdn.microsoft.com/bbc26c03-c154-4b1e-883e-2942b59ded02">DDPIXELFORMAT</a> structures in which the driver should write the pixel formats supported by the VPE object. This member can be <b>NULL</b>.


### -field dwNumFormats

Specifies the location in which the driver should write the number of formats that the VPE object supports.


### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="https://msdn.microsoft.com/aac34116-a6a2-4d00-b0c4-87fac786b68d">DdVideoPortGetInputFormats</a> callback. A return code of DD_OK indicates success. For more information, see <a href="https://msdn.microsoft.com/da4cc7d7-6826-48aa-96c6-004e31fc3e3e">Return Values for DirectDraw</a>.


### -field GetVideoPortInputFormats

Used by the DirectDraw API and should not be filled in by the driver.


## -see-also




<a href="https://msdn.microsoft.com/aac34116-a6a2-4d00-b0c4-87fac786b68d">DdVideoPortGetInputFormats</a>
 

 

