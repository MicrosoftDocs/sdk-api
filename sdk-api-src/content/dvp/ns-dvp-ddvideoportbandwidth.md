---
UID: NS:dvp._DDVIDEOPORTBANDWIDTH
title: DDVIDEOPORTBANDWIDTH (dvp.h)
description: The DDVIDEOPORTBANDWIDTH structure describes the bandwidth characteristics of an overlay when used with a particular video port extensions (VPE) object/pixel format configuration.
helpviewer_keywords: ["*LPDDVIDEOPORTBANDWIDTH","DDVIDEOPORTBANDWIDTH","DDVIDEOPORTBANDWIDTH structure [Display Devices]","ddstrcts_e3e483bd-3cb2-41e2-9563-c6d8e5970c21.xml","display.ddvideoportbandwidth","dvp/DDVIDEOPORTBANDWIDTH"]
old-location: display\ddvideoportbandwidth.htm
tech.root: display
ms.assetid: 3e13874d-294e-4161-8131-f78799b2e90e
ms.date: 12/05/2018
ms.keywords: '*LPDDVIDEOPORTBANDWIDTH, DDVIDEOPORTBANDWIDTH, DDVIDEOPORTBANDWIDTH structure [Display Devices], ddstrcts_e3e483bd-3cb2-41e2-9563-c6d8e5970c21.xml, display.ddvideoportbandwidth, dvp/DDVIDEOPORTBANDWIDTH'
req.header: dvp.h
req.include-header: Dvp.h
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
targetos: Windows
req.typenames: '*LPDDVIDEOPORTBANDWIDTH, DDVIDEOPORTBANDWIDTH'
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DDVIDEOPORTBANDWIDTH
 - dvp/_DDVIDEOPORTBANDWIDTH
 - LPDDVIDEOPORTBANDWIDTH
 - dvp/LPDDVIDEOPORTBANDWIDTH
 - DDVIDEOPORTBANDWIDTH
 - dvp/DDVIDEOPORTBANDWIDTH
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dvp.h
api_name:
 - DDVIDEOPORTBANDWIDTH
---

# DDVIDEOPORTBANDWIDTH structure


## -description

The DDVIDEOPORTBANDWIDTH structure describes the bandwidth characteristics of an overlay when used with a particular <a href="/windows-hardware/drivers/">video port extensions (VPE)</a> object/pixel format configuration.

## -struct-fields

### -field dwSize

Specifies the size in bytes of this DDVIDEOPORTBANDWIDTH structure.

### -field dwCaps

Specifies the dependencies of the bandwidth. The driver's <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_vportcb_getbandwidth">DdVideoPortGetBandwidth</a> function sets this member to one of the following values:

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

Specifies the stretch factor or overlay source size at which the device can support an overlay, multiplied by 1000. The driver sets this value based on its device's type and capabilities, and on the dimensions specified in the <b>dwWidth</b> and <b>dwHeight</b> members of the <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_getvportbandwidthdata">DD_GETVPORTBANDWIDTHDATA</a> structure passed to <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_vportcb_getbandwidth">DdVideoPortGetBandwidth</a>. For example, a stretch factor of 2 is specified as 2000, and an overlay source size of 750 indicates that the specified source overlay be shrunk to 75 percent of its original size. The driver must return a valid number in this member.

### -field dwColorkey

Specifies the stretch factor or overlay source size at which an overlay with color keying is supported, multiplied by 1000. The driver sets this value based on its device's type and capabilities, and on the dimensions specified in the <b>dwWidth</b> and <b>dwHeight</b> members of the DD_GETVPORTBANDWIDTHDATA structure passed to <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_vportcb_getbandwidth">DdVideoPortGetBandwidth</a>. For example, a stretch factor of 2 is specified as 2000.

### -field dwYInterpolate

Specifies the stretch factor or overlay source size at which an overlay with y-axis interpolation is supported, multiplied by 1000. The driver sets this value based on its device's type and capabilities, and on the dimensions specified in the <b>dwWidth</b> and <b>dwHeight</b> members of the <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_getvportbandwidthdata">DD_GETVPORTBANDWIDTHDATA</a> structure passed to <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_vportcb_getbandwidth">DdVideoPortGetBandwidth</a>. For example, a stretch factor of 2 is specified as 2000.

### -field dwYInterpAndColorkey

Specifies the stretch factor or overlay source size at which an overlay with y-axis interpolation and color keying is supported, multiplied by 1000. The driver sets this value based on its device's type and capabilities, and on the dimensions specified in the <b>dwWidth</b> and <b>dwHeight</b> members of the DD_GETVPORTBANDWIDTHDATA structure passed to <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_vportcb_getbandwidth">DdVideoPortGetBandwidth</a>. For example, a stretch factor of 2 is specified as 2000.

### -field dwReserved1

Reserved for system use and should be ignored by the driver.

### -field dwReserved2

Reserved for system use and should be ignored by the driver.

## -see-also

<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_getvportbandwidthdata">DD_GETVPORTBANDWIDTHDATA</a>



<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_vportcb_getbandwidth">DdVideoPortGetBandwidth</a>