---
UID: NF:wingdi.SetMiterLimit
title: SetMiterLimit function (wingdi.h)
description: The SetMiterLimit function sets the limit for the length of miter joins for the specified device context.
helpviewer_keywords: ["SetMiterLimit","SetMiterLimit function [Windows GDI]","_win32_SetMiterLimit","gdi.setmiterlimit","wingdi/SetMiterLimit"]
old-location: gdi\setmiterlimit.htm
tech.root: gdi
ms.assetid: 4bed113b-9e3f-441f-96d7-71630bf9298e
ms.date: 12/05/2018
ms.keywords: SetMiterLimit, SetMiterLimit function [Windows GDI], _win32_SetMiterLimit, gdi.setmiterlimit, wingdi/SetMiterLimit
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetMiterLimit
 - wingdi/SetMiterLimit
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
api_name:
 - SetMiterLimit
---

# SetMiterLimit function


## -description

The <b>SetMiterLimit</b> function sets the limit for the length of miter joins for the specified device context.

## -parameters

### -param hdc [in]

Handle to the device context.

### -param limit [in]

Specifies the new miter limit for the device context.

### -param old [out]

Pointer to a floating-point value that receives the previous miter limit. If this parameter is <b>NULL</b>, the previous miter limit is not returned.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

The miter length is defined as the distance from the intersection of the line walls on the inside of the join to the intersection of the line walls on the outside of the join. The miter limit is the maximum allowed ratio of the miter length to the line width.

The default miter limit is 10.0.

<div class="alert"><b>Note</b>  Setting <i>eNewLimit</i> to a float value less than 1.0f will cause the function to fail.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-extcreatepen">ExtCreatePen</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getmiterlimit">GetMiterLimit</a>



<a href="/windows/desktop/gdi/path-functions">Path Functions</a>



<a href="/windows/desktop/gdi/paths">Paths Overview</a>