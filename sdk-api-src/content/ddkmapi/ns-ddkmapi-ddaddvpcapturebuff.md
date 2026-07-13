---
UID: NS:ddkmapi._DDADDVPCAPTUREBUFF
title: DDADDVPCAPTUREBUFF (ddkmapi.h)
description: The DDADDVPCAPTUREBUFF structure contains the information required to add a new buffer to the internal capture queue.
helpviewer_keywords: ["*LPDDADDVPCAPTUREBUFF","DDADDVPCAPTUREBUFF","DDADDVPCAPTUREBUFF structure [Display Devices]","LPDDADDVPCAPTUREBUFF","LPDDADDVPCAPTUREBUFF structure pointer [Display Devices]","ddkmapi/DDADDVPCAPTUREBUFF","ddkmapi/LPDDADDVPCAPTUREBUFF","ddstrcts_8aed47e9-8635-4a52-aba6-7768f11f9177.xml","display.ddaddvpcapturebuff"]
old-location: display\ddaddvpcapturebuff.htm
tech.root: display
ms.assetid: 7ee3f5ce-987a-42c9-8681-5bcb9028178a
ms.date: 12/05/2018
ms.keywords: '*LPDDADDVPCAPTUREBUFF, DDADDVPCAPTUREBUFF, DDADDVPCAPTUREBUFF structure [Display Devices], LPDDADDVPCAPTUREBUFF, LPDDADDVPCAPTUREBUFF structure pointer [Display Devices], ddkmapi/DDADDVPCAPTUREBUFF, ddkmapi/LPDDADDVPCAPTUREBUFF, ddstrcts_8aed47e9-8635-4a52-aba6-7768f11f9177.xml, display.ddaddvpcapturebuff'
req.header: ddkmapi.h
req.include-header: Ddkmapi.h
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
req.typenames: DDADDVPCAPTUREBUFF, *LPDDADDVPCAPTUREBUFF
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DDADDVPCAPTUREBUFF
 - ddkmapi/_DDADDVPCAPTUREBUFF
 - LPDDADDVPCAPTUREBUFF
 - ddkmapi/LPDDADDVPCAPTUREBUFF
 - DDADDVPCAPTUREBUFF
 - ddkmapi/DDADDVPCAPTUREBUFF
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ddkmapi.h
api_name:
 - DDADDVPCAPTUREBUFF
---

# DDADDVPCAPTUREBUFF structure


## -description

The DDADDVPCAPTUREBUFF structure contains the information required to add a new buffer to the internal capture queue.

## -struct-fields

### -field hCapture

Handle to the <a href="/windows-hardware/drivers/">video port extensions (VPE)</a> object.

### -field dwFlags

Indicates whether the destination buffer exists in regular system memory or nonlocal display memory (AGP). This member can be one of the following values:

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>
DDADDBUFF_INVERT

</td>
<td>
The buffer is to be inverted during capture.

</td>
</tr>
<tr>
<td>
DDADDBUFF_NONLOCALVIDMEM

</td>
<td>
The destination buffer exists in nonlocal display memory.

</td>
</tr>
<tr>
<td>
DDADDBUFF_SYSTEMMEMORY

</td>
<td>
The destination buffer exists in system memory.

</td>
</tr>
</table>

### -field pMDL

Points to an <a href="/windows-hardware/drivers/">MDL</a> (defined in <i>wdm.h</i>) that describes the physical pages of the destination buffer.

### -field pKEvent

Points to a KEVENT that the kernel-mode video transport sets when the destination has been filled.

### -field lpBuffInfo

Points to a <a href="/windows/desktop/api/ddkmapi/ns-ddkmapi-ddcapbuffinfo">DDCAPBUFFINFO</a> structure that the kernel-mode video transport fills in before setting the KEVENT.

## -see-also

<a href="/windows/desktop/api/ddkmapi/ns-ddkmapi-ddcapbuffinfo">DDCAPBUFFINFO</a>



<a href="/previous-versions/windows/hardware/drivers/ff550599(v=vs.85)">DD_DXAPI_ADDVPCAPTUREBUFFER</a>



<a href="/previous-versions/windows/drivers/display/nf-dxapi-dxapi">DxApi</a>