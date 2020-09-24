---
UID: NF:wingdi.GdiSetBatchLimit
title: GdiSetBatchLimit function (wingdi.h)
description: The GdiSetBatchLimit function sets the maximum number of function calls that can be accumulated in the calling thread's current batch. The system flushes the current batch whenever this limit is exceeded.
helpviewer_keywords: ["GdiSetBatchLimit","GdiSetBatchLimit function [Windows GDI]","_win32_GdiSetBatchLimit","gdi.gdisetbatchlimit","wingdi/GdiSetBatchLimit"]
old-location: gdi\gdisetbatchlimit.htm
tech.root: gdi
ms.assetid: 53bf0dfe-e93c-401d-ac5d-6717bad2625e
ms.date: 12/05/2018
ms.keywords: GdiSetBatchLimit, GdiSetBatchLimit function [Windows GDI], _win32_GdiSetBatchLimit, gdi.gdisetbatchlimit, wingdi/GdiSetBatchLimit
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
 - GdiSetBatchLimit
 - wingdi/GdiSetBatchLimit
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
 - GdiSetBatchLimit
---

# GdiSetBatchLimit function


## -description

The <b>GdiSetBatchLimit</b> function sets the maximum number of function calls that can be accumulated in the calling thread's current batch. The system flushes the current batch whenever this limit is exceeded.

## -parameters

### -param dw [in]

Specifies the batch limit to be set. A value of 0 sets the default limit. A value of 1 disables batching.

## -returns

If the function succeeds, the return value is the previous batch limit.

If the function fails, the return value is zero.

## -remarks

Only GDI drawing functions that return Boolean values can be accumulated in the current batch; calls to any other GDI functions immediately flush the current batch. Exceeding the batch limit or calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-gdiflush">GdiFlush</a> function also flushes the current batch.

When the system accumulates a function call, the function returns <b>TRUE</b> to indicate it is in the batch. When the system flushes the current batch and executes the function for the second time, the return value is either <b>TRUE</b> or <b>FALSE</b>, depending on whether the function succeeds. This second return value is reported only if <a href="/windows/desktop/api/wingdi/nf-wingdi-gdiflush">GdiFlush</a> is used to flush the batch.

<div class="alert"><b>Note</b>  The batch limit is maintained for each thread separately. In order to completely disable batching, call <b>GdiSetBatchLimit</b> (1) during the initialization of each thread.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-gdiflush">GdiFlush
      </a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-gdigetbatchlimit">GdiGetBatchLimit
      </a>



<a href="/windows/desktop/gdi/painting-and-drawing-functions">Painting and Drawing Functions</a>



<a href="/windows/desktop/gdi/painting-and-drawing">Painting and Drawing Overview</a>