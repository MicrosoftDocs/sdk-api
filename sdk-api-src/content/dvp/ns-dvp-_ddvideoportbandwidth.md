---
UID: NS:dvp._DDVIDEOPORTBANDWIDTH
title: "_DDVIDEOPORTBANDWIDTH"
author: windows-sdk-content
description: The DDVIDEOPORTBANDWIDTH structure describes the bandwidth characteristics of an overlay when used with a particular video port extensions (VPE) object/pixel format configuration.
old-location: display\ddvideoportbandwidth.htm
old-project: display
ms.assetid: 3e13874d-294e-4161-8131-f78799b2e90e
ms.author: windowssdkdev
ms.date: 06/26/2018
ms.keywords: "*LPDDVIDEOPORTBANDWIDTH, DDVIDEOPORTBANDWIDTH, DDVIDEOPORTBANDWIDTH structure [Display Devices], _DDVIDEOPORTBANDWIDTH, ddstrcts_e3e483bd-3cb2-41e2-9563-c6d8e5970c21.xml, display.ddvideoportbandwidth, dvp/DDVIDEOPORTBANDWIDTH"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dvp.h
req.include-header: Dvp.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Dvbsiparser.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: "*LPDDVIDEOPORTBANDWIDTH, DDVIDEOPORTBANDWIDTH"
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dvp.h
api_name:
 - DDVIDEOPORTBANDWIDTH
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# _DDVIDEOPORTBANDWIDTH structure


## -description


The DDVIDEOPORTBANDWIDTH structure describes the bandwidth characteristics of an overlay when used with a particular <a href="https://msdn.microsoft.com/a1de1905-09f3-4689-ace9-06690a1f930a">video port extensions (VPE)</a> object/pixel format configuration.


## -struct-fields




### -field dwSize

Specifies the size in bytes of this DDVIDEOPORTBANDWIDTH structure.


### -field dwCaps

Specifies the dependencies of the bandwidth. The driver's <a href="https://msdn.microsoft.com/4b9cfec1-a599-47a5-878e-2cde6b3b780a">DdVideoPortGetBandwidth</a> function sets this member to one of the following values:

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>
DDVPBCAPS_DESTINATION

</td>
<td>
The device's capabilities are described in terms of the destination overlay's minimum stretch factor. The bandwidth information set by the driver in the <b>dwOverlay</b>, <b>dwColorkey</b>, <b>dwYInterpolate</b>, and <b>dwYInterpAndColorkey</b> members refers to the destination overlay size.

</td>
</tr>
<tr>
<td>
DDVPBCAPS_SOURCE

</td>
<td>
The device's capabilities are described in terms of the required source overlay's rectangle size (in pixels). The bandwidth information set by the driver in the <b>dwOverlay</b>, <b>dwColorkey</b>, <b>dwYInterpolate</b>, and <b>dwYInterpAndColorkey</b> members refers to the source overlay size.

</td>
</tr>
</table>
 


### -field dwOverlay

Specifies the stretch factor or overlay source size at which the device can support an overlay, multiplied by 1000. The driver sets this value based on its device's type and capabilities, and on the dimensions specified in the <b>dwWidth</b> and <b>dwHeight</b> members of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff551593">DD_GETVPORTBANDWIDTHDATA</a> structure passed to <a href="https://msdn.microsoft.com/4b9cfec1-a599-47a5-878e-2cde6b3b780a">DdVideoPortGetBandwidth</a>. For example, a stretch factor of 2 is specified as 2000, and an overlay source size of 750 indicates that the specified source overlay be shrunk to 75 percent of its original size. The driver must return a valid number in this member.


### -field dwColorkey

Specifies the stretch factor or overlay source size at which an overlay with color keying is supported, multiplied by 1000. The driver sets this value based on its device's type and capabilities, and on the dimensions specified in the <b>dwWidth</b> and <b>dwHeight</b> members of the DD_GETVPORTBANDWIDTHDATA structure passed to <a href="https://msdn.microsoft.com/4b9cfec1-a599-47a5-878e-2cde6b3b780a">DdVideoPortGetBandwidth</a>. For example, a stretch factor of 2 is specified as 2000.


### -field dwYInterpolate

Specifies the stretch factor or overlay source size at which an overlay with y-axis interpolation is supported, multiplied by 1000. The driver sets this value based on its device's type and capabilities, and on the dimensions specified in the <b>dwWidth</b> and <b>dwHeight</b> members of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff551593">DD_GETVPORTBANDWIDTHDATA</a> structure passed to <a href="https://msdn.microsoft.com/4b9cfec1-a599-47a5-878e-2cde6b3b780a">DdVideoPortGetBandwidth</a>. For example, a stretch factor of 2 is specified as 2000.


### -field dwYInterpAndColorkey

Specifies the stretch factor or overlay source size at which an overlay with y-axis interpolation and color keying is supported, multiplied by 1000. The driver sets this value based on its device's type and capabilities, and on the dimensions specified in the <b>dwWidth</b> and <b>dwHeight</b> members of the DD_GETVPORTBANDWIDTHDATA structure passed to <a href="https://msdn.microsoft.com/4b9cfec1-a599-47a5-878e-2cde6b3b780a">DdVideoPortGetBandwidth</a>. For example, a stretch factor of 2 is specified as 2000.


### -field dwReserved1

Reserved for system use and should be ignored by the driver.


### -field dwReserved2

Reserved for system use and should be ignored by the driver.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551593">DD_GETVPORTBANDWIDTHDATA</a>



<a href="https://msdn.microsoft.com/4b9cfec1-a599-47a5-878e-2cde6b3b780a">DdVideoPortGetBandwidth</a>
 

 

