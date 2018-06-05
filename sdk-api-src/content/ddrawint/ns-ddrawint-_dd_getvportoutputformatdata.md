---
UID: NS:ddrawint._DD_GETVPORTOUTPUTFORMATDATA
title: "_DD_GETVPORTOUTPUTFORMATDATA"
author: windows-sdk-content
description: The DD_GETVPORTOUTPUTFORMATDATA structure contains the information required for the driver to return all of the output formats that the video port extensions (VPE) object supports for a given input format.
old-location: display\dd_getvportoutputformatdata.htm
old-project: display
ms.assetid: 3033a4e9-3f94-4702-9db8-098a358ab1c2
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: "*PDD_GETVPORTOUTPUTFORMATDATA, DD_GETVPORTOUTPUTFORMATDATA, DD_GETVPORTOUTPUTFORMATDATA structure [Display Devices], _DD_GETVPORTOUTPUTFORMATDATA, ddrawint/DD_GETVPORTOUTPUTFORMATDATA, ddstrcts_c8b41b3c-cb15-46d2-aa72-f59301276ffe.xml, display.dd_getvportoutputformatdata"
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: "*PDD_GETVPORTOUTPUTFORMATDATA, DD_GETVPORTOUTPUTFORMATDATA"
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	ddrawint.h
api_name:
-	DD_GETVPORTOUTPUTFORMATDATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DD_GETVPORTOUTPUTFORMATDATA structure


## -description


The DD_GETVPORTOUTPUTFORMATDATA structure contains the information required for the driver to return all of the output formats that the <a href="https://msdn.microsoft.com/a1de1905-09f3-4689-ace9-06690a1f930a">video port extensions (VPE)</a> object supports for a given input format.


## -struct-fields




### -field lpDD

Points to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff550595">DD_DIRECTDRAW_LOCAL</a> structure that is relevant to the current Microsoft DirectDraw process only. 


### -field lpVideoPort

Points to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff551761">DD_VIDEOPORT_LOCAL</a> structure that represents this VPE object.


### -field dwFlags

Indicates the type of output formats for which support is being queried. This member can be one or more of the following values:

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
 


### -field lpddpfInputFormat

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550274">DDPIXELFORMAT</a> structure that contains an input format supported by the VPE object. This format was returned by <a href="https://msdn.microsoft.com/aac34116-a6a2-4d00-b0c4-87fac786b68d">DdVideoPortGetInputFormats</a>.


### -field lpddpfOutputFormats

Points to an array of DDPIXELFORMAT structures in which the driver should return the output formats that the VPE object supports for the input format specified by <b>lpddpfInputFormat</b>. This member can be <b>NULL</b>.


### -field dwNumFormats

Specifies the location in which the driver should return the number of output formats that the VPE object supports for the specified input format.


### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="https://msdn.microsoft.com/8e9df88b-a50a-4838-9732-9f818936cbcb">DdVideoPortGetOutputFormats</a> callback. A return code of DD_OK indicates success. For more information, see <a href="https://msdn.microsoft.com/da4cc7d7-6826-48aa-96c6-004e31fc3e3e">Return Values for DirectDraw</a>.


### -field GetVideoPortInputFormats

Unused: Win95 compatibility


## -see-also




<a href="https://msdn.microsoft.com/8e9df88b-a50a-4838-9732-9f818936cbcb">DdVideoPortGetOutputFormats</a>
 

 

