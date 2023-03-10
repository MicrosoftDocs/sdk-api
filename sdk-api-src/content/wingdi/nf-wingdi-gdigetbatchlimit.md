---
UID: NF:wingdi.GdiGetBatchLimit
title: GdiGetBatchLimit function (wingdi.h)
description: The GdiGetBatchLimit function returns the maximum number of function calls that can be accumulated in the calling thread's current batch. The system flushes the current batch whenever this limit is exceeded.
helpviewer_keywords: ["GdiGetBatchLimit","GdiGetBatchLimit function [Windows GDI]","_win32_GdiGetBatchLimit","gdi.gdigetbatchlimit","wingdi/GdiGetBatchLimit"]
old-location: gdi\gdigetbatchlimit.htm
tech.root: gdi
ms.assetid: aafe7635-1a71-42a9-90b7-11179e245af4
ms.date: 12/05/2018
ms.keywords: GdiGetBatchLimit, GdiGetBatchLimit function [Windows GDI], _win32_GdiGetBatchLimit, gdi.gdigetbatchlimit, wingdi/GdiGetBatchLimit
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
 - GdiGetBatchLimit
 - wingdi/GdiGetBatchLimit
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
 - GDI32Full.dll
api_name:
 - GdiGetBatchLimit
---

# GdiGetBatchLimit function


## -description

The <b>GdiGetBatchLimit</b> function returns the maximum number of function calls that can be accumulated in the calling thread's current batch. The system flushes the current batch whenever this limit is exceeded.



## -returns

If the function succeeds, the return value is the batch limit.

If the function fails, the return value is zero.

## -remarks

The batch limit is set by using the <a href="/windows/desktop/api/wingdi/nf-wingdi-gdisetbatchlimit">GdiSetBatchLimit</a> function. Setting the limit to 1 effectively disables batching.

Only GDI drawing functions that return Boolean values can be batched; calls to any other GDI functions immediately flush the current batch. Exceeding the batch limit or calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-gdiflush">GdiFlush</a> function also flushes the current batch.

When the system batches a function call, the function returns <b>TRUE</b>. The actual return value for the function is reported only if <a href="/windows/desktop/api/wingdi/nf-wingdi-gdiflush">GdiFlush</a> is used to flush the batch.

<div class="alert"><b>Note</b>  The batch limit is maintained for each thread separately. In order to completely disable batching, call <a href="/windows/desktop/api/wingdi/nf-wingdi-gdisetbatchlimit">GdiSetBatchLimit</a> (1) during the initialization of each thread.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-gdiflush">GdiFlush
      </a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-gdisetbatchlimit">GdiSetBatchLimit
      </a>



<a href="/windows/desktop/gdi/painting-and-drawing-functions">Painting and Drawing Functions</a>



<a href="/windows/desktop/gdi/painting-and-drawing">Painting and Drawing Overview</a>
