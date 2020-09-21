---
UID: NS:winddi._DEVHTADJDATA
title: DEVHTADJDATA (winddi.h)
description: The DEVHTADJDATA structure is used as input to the HTUI_DeviceColorAdjustment function.
helpviewer_keywords: ["*PDEVHTADJDATA","DEVHTADJDATA","DEVHTADJDATA structure [Display Devices]","PDEVHTADJDATA","PDEVHTADJDATA structure pointer [Display Devices]","display.devhtadjdata","grstrcts_bd1a058d-3d43-48f3-a87e-7f6f5276ba51.xml","winddi/DEVHTADJDATA","winddi/PDEVHTADJDATA"]
old-location: display\devhtadjdata.htm
tech.root: display
ms.assetid: a90f2283-7bc3-48e4-bb1c-172d9776a284
ms.date: 12/05/2018
ms.keywords: '*PDEVHTADJDATA, DEVHTADJDATA, DEVHTADJDATA structure [Display Devices], PDEVHTADJDATA, PDEVHTADJDATA structure pointer [Display Devices], display.devhtadjdata, grstrcts_bd1a058d-3d43-48f3-a87e-7f6f5276ba51.xml, winddi/DEVHTADJDATA, winddi/PDEVHTADJDATA'
req.header: winddi.h
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
targetos: Windows
req.typenames: DEVHTADJDATA, *PDEVHTADJDATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DEVHTADJDATA
 - winddi/_DEVHTADJDATA
 - PDEVHTADJDATA
 - winddi/PDEVHTADJDATA
 - DEVHTADJDATA
 - winddi/DEVHTADJDATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - DEVHTADJDATA
---

# DEVHTADJDATA structure


## -description

The DEVHTADJDATA structure is used as input to the <a href="/windows/desktop/api/winddi/nf-winddi-htui_devicecoloradjustment">HTUI_DeviceColorAdjustment</a> function.

## -struct-fields

### -field DeviceFlags

Is a set of flags, set by the caller, describing color mixing and color versus gray-scale output. Either, both, or neither of the following flags should be set, as appropriate:

<table>
<tr>
<th>Flag</th>
<th>Definition</th>
</tr>
<tr>
<td>
DEVHTADJF_ADDITIVE_DEVICE

</td>
<td>

<dl>
<dt>If set, the device uses additive color mixing.</dt>
<dt>If not set, the device uses subtractive color mixing.</dt>
</dl>


</td>
</tr>
<tr>
<td>
DEVHTADJF_COLOR_DEVICE

</td>
<td>

<dl>
<dt>If set, the device produces color output.</dt>
<dt>If not set, the device produces gray-scaled output.</dt>
</dl>


</td>
</tr>
</table>

### -field DeviceXDPI

Is the caller-supplied horizontal resolution, in dots per inch, for the device.

### -field DeviceYDPI

Is the caller-supplied vertical resolution, in dots per inch, for the device.

### -field pDefHTInfo

Is a caller-supplied pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-devhtinfo">DEVHTINFO</a> structure containing the device's default halftoning properties.

### -field pAdjHTInfo

Is a caller-supplied pointer to a DEVHTINFO structure containing the device's current halftoning properties. Before the <a href="/windows/desktop/api/winddi/nf-winddi-htui_devicecoloradjustment">HTUI_DeviceColorAdjustment</a> function returns, it modifies this structure's contents, if the user has adjusted the halftoning properties. Can be <b>NULL</b> (see the following Remarks section).

## -remarks

If <b>pAdjHTInfo</b> is <b>NULL</b>, or if <b>pAdjHTInfo</b> and <b>pDefHTInfo</b> point to the same buffer, the <a href="/windows/desktop/api/winddi/nf-winddi-htui_devicecoloradjustment">HTUI_DeviceColorAdjustment</a> function displays the halftoning properties supplied by <b>pDefHTInfo</b> but does not allow the user to modify them.