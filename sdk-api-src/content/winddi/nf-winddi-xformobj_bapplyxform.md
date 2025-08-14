---
UID: NF:winddi.XFORMOBJ_bApplyXform
title: XFORMOBJ_bApplyXform function (winddi.h)
description: The XFORMOBJ_bApplyXform function applies the given transform or its inverse to the given array of points.
helpviewer_keywords: ["XFORMOBJ_bApplyXform","XFORMOBJ_bApplyXform function [Display Devices]","display.xformobj_bapplyxform","gdifncs_d95d97d6-6fd2-4deb-b7f9-627eef20fece.xml","winddi/XFORMOBJ_bApplyXform"]
old-location: display\xformobj_bapplyxform.htm
tech.root: display
ms.assetid: a9267d2a-96ab-4518-8045-428ab74bd599
ms.date: 12/05/2018
ms.keywords: XFORMOBJ_bApplyXform, XFORMOBJ_bApplyXform function [Display Devices], display.xformobj_bapplyxform, gdifncs_d95d97d6-6fd2-4deb-b7f9-627eef20fece.xml, winddi/XFORMOBJ_bApplyXform
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
 - XFORMOBJ_bApplyXform
 - winddi/XFORMOBJ_bApplyXform
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-core-win32k-full-export-l1-1-0.dll
 - Win32k.sys
api_name:
 - XFORMOBJ_bApplyXform
---

# XFORMOBJ_bApplyXform function


## -description

The <b>XFORMOBJ_bApplyXform</b> function applies the given transform or its inverse to the given array of points.

## -parameters

### -param pxo

Pointer to a <a href="/previous-versions/windows/hardware/drivers/ff570618(v=vs.85)">XFORMOBJ</a> structure that defines the transform to be applied to the <i>pvIn</i> array.

### -param iMode [in]

Identifies the transform and the input and output data types. This parameter can be one of the following:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
XF_INV_FXTOL

</td>
<td>
Applies the inverse of the transform to POINTFIX structures to get <a href="/windows/desktop/api/windef/ns-windef-pointl">POINTL</a> structures.

</td>
</tr>
<tr>
<td>
XF_INV_LTOL

</td>
<td>
Applies the inverse of the transform to POINTL structures to get POINTL structures.

</td>
</tr>
<tr>
<td>
XF_LTOFX

</td>
<td>
Applies the transform to POINTL structures to get POINTFIX structures (see <a href="/windows-hardware/drivers/display/gdi-data-types">GDI Data Types</a>).

</td>
</tr>
<tr>
<td>
XF_LTOL

</td>
<td>
Applies the transform to POINTL structures to get POINTL structures.

</td>
</tr>
</table>

### -param cPoints

Specifies the count of points in <i>pvIn</i> to be transformed.

### -param pvIn

Pointer to an array of input points. The format of the points is specified by the <i>iMode</i> parameter.

### -param pvOut

Pointer to the buffer that is to receive the transformed points. The <i>iMode</i> parameter specifies the format of the points.

## -returns

The return value is <b>TRUE</b> if all points were transformed without overflow. <b>FALSE</b> is returned if <i>pxo</i>, <i>pvIn</i>, or <i>pvOut</i> are <b>null</b>, or if overflow occurs during the transformation.

## -see-also

<a href="/previous-versions/windows/hardware/drivers/ff570618(v=vs.85)">XFORMOBJ</a>