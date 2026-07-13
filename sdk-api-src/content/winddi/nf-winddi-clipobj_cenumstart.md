---
UID: NF:winddi.CLIPOBJ_cEnumStart
title: CLIPOBJ_cEnumStart function (winddi.h)
description: The CLIPOBJ_cEnumStart function sets parameters for enumerating rectangles in a specified clip region.
helpviewer_keywords: ["CLIPOBJ_cEnumStart","CLIPOBJ_cEnumStart function [Display Devices]","display.clipobj_cenumstart","gdifncs_53ccc337-0aa7-442c-a612-facb369b66c6.xml","winddi/CLIPOBJ_cEnumStart"]
old-location: display\clipobj_cenumstart.htm
tech.root: display
ms.assetid: e719f856-04a9-480d-b79a-df2307a48162
ms.date: 12/05/2018
ms.keywords: CLIPOBJ_cEnumStart, CLIPOBJ_cEnumStart function [Display Devices], display.clipobj_cenumstart, gdifncs_53ccc337-0aa7-442c-a612-facb369b66c6.xml, winddi/CLIPOBJ_cEnumStart
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
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
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLIPOBJ_cEnumStart
 - winddi/CLIPOBJ_cEnumStart
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-core-win32k-common-export-l1-1-0.dll
 - Win32k.sys
api_name:
 - CLIPOBJ_cEnumStart
---

# CLIPOBJ_cEnumStart function


## -description

The <b>CLIPOBJ_cEnumStart</b> function sets parameters for enumerating rectangles in a specified <a href="/windows-hardware/drivers/">clip region</a>.

## -parameters

### -param pco [in]

Pointer to the <a href="/windows/desktop/api/winddi/ns-winddi-clipobj">CLIPOBJ</a> structure that defines the clip region to be enumerated.

### -param bAll [in]

Specifies whether the entire region should be enumerated. This parameter is <b>TRUE</b> if the whole region should be enumerated. It is <b>FALSE</b> if only the parts relevant to the present drawing operation should be enumerated.

A driver that caches clip regions must enumerate the entire region.

### -param iType [in]

Specifies the data structures that are to be written by <a href="/windows/desktop/api/winddi/nf-winddi-clipobj_benum">CLIPOBJ_bEnum</a>. This parameter currently must be CT_RECTANGLES, indicating that the region is to be enumerated as a list of rectangles.

### -param iDirection [in]

Determines the order in which the rectangles are to be enumerated. This order can be essential if a <a href="/windows/desktop/api/winddi/nf-winddi-drvbitblt">DrvBitBlt</a> operation is executing concurrently on the same surface. If the order is not relevant to the device driver, CD_ANY should be specified for complex regions, allowing GDI to optimize the enumeration. This value can be one of the following:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
CD_ANY

</td>
<td>
Any order convenient for GDI.

</td>
</tr>
<tr>
<td>
CD_LEFTDOWN

</td>
<td>
Right to left, top to bottom.

</td>
</tr>
<tr>
<td>
CD_LEFTUP

</td>
<td>
Right to left, bottom to top.

</td>
</tr>
<tr>
<td>
CD_RIGHTDOWN

</td>
<td>
Left to right, top to bottom.

</td>
</tr>
<tr>
<td>
CD_RIGHTUP

</td>
<td>
Left to right, bottom to top.

</td>
</tr>
</table>

### -param cLimit [in]

Specifies the maximum number of rectangles to be enumerated. If this parameter is zero, counting is omitted.

## -returns

The return value is the count of enumerated rectangles. If the count exceeds <b>cLimit</b>, the return value is 0xFFFFFFFF.

## -remarks

A region can be enumerated whether this function is called. By default, the driver only enumerates relevant rectangles, starting at the upper left.

The driver can restart enumeration by calling this function again.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-clipobj">CLIPOBJ</a>



<a href="/windows/desktop/api/winddi/nf-winddi-clipobj_benum">CLIPOBJ_bEnum</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvbitblt">DrvBitBlt</a>