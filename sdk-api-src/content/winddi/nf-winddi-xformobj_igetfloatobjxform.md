---
UID: NF:winddi.XFORMOBJ_iGetFloatObjXform
title: XFORMOBJ_iGetFloatObjXform function (winddi.h)
description: The XFORMOBJ_iGetFloatObjXform function downloads a FLOATOBJ transform to the driver.
helpviewer_keywords: ["XFORMOBJ_iGetFloatObjXform","XFORMOBJ_iGetFloatObjXform function [Display Devices]","display.xformobj_igetfloatobjxform","gdifncs_26b564b5-f2ca-448a-9ca8-f34e7f8fb57a.xml","winddi/XFORMOBJ_iGetFloatObjXform"]
old-location: display\xformobj_igetfloatobjxform.htm
tech.root: display
ms.assetid: 761c6061-841b-4187-a826-575d2a5086db
ms.date: 12/05/2018
ms.keywords: XFORMOBJ_iGetFloatObjXform, XFORMOBJ_iGetFloatObjXform function [Display Devices], display.xformobj_igetfloatobjxform, gdifncs_26b564b5-f2ca-448a-9ca8-f34e7f8fb57a.xml, winddi/XFORMOBJ_iGetFloatObjXform
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
 - XFORMOBJ_iGetFloatObjXform
 - winddi/XFORMOBJ_iGetFloatObjXform
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
 - XFORMOBJ_iGetFloatObjXform
---

# XFORMOBJ_iGetFloatObjXform function


## -description

The <b>XFORMOBJ_iGetFloatObjXform</b> function downloads a FLOATOBJ transform to the driver.

## -parameters

### -param pxo

Pointer to the <a href="/previous-versions/windows/hardware/drivers/ff570618(v=vs.85)">XFORMOBJ</a> structure that defines the transform to be downloaded.

### -param pfxo

Pointer to the buffer that is to receive the <a href="/windows/desktop/api/winddi/ns-winddi-floatobj_xform">FLOATOBJ_XFORM</a> structure. This parameter can be <b>NULL</b>.

## -returns

If an error occurs, the return value is DDI_ERROR. Otherwise, the return value is a complexity hint about the transform object. The value of this transform characterization can be one of the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>GX_GENERAL</b></dt>
</dl>
</td>
<td width="60%">
Arbitrary 2 x 2 matrix and offset.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>GX_IDENTITY</b></dt>
</dl>
</td>
<td width="60%">
Identity matrix; no translation offset.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>GX_OFFSET</b></dt>
</dl>
</td>
<td width="60%">
Identity matrix; there is a translation offset.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>GX_SCALE</b></dt>
</dl>
</td>
<td width="60%">
Off-diagonal matrix elements are zero.

</td>
</tr>
</table>

## -remarks

If <i>pxfo</i> is not <b>NULL</b>, <b>XFORMOBJ_iGetFloatObjXform</b> loads a FLOATOBJ_XFORM into the memory location <i>pxfo</i> points to. This function allows graphics drivers to emulate floating-point arithmetic. NT-based operating systems do not support kernel-mode floating-point operations on some systems.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-floatobj">FLOATOBJ</a>



<a href="/windows/desktop/api/winddi/ns-winddi-floatobj_xform">FLOATOBJ_XFORM</a>



<a href="/previous-versions/windows/hardware/drivers/ff570618(v=vs.85)">XFORMOBJ</a>