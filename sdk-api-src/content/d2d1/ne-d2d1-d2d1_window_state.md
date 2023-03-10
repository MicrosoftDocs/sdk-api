---
UID: NE:d2d1.D2D1_WINDOW_STATE
title: D2D1_WINDOW_STATE (d2d1.h)
description: Describes whether a window is occluded.
helpviewer_keywords: ["D2D1_WINDOW_STATE","D2D1_WINDOW_STATE enumeration [Direct2D]","D2D1_WINDOW_STATE_NONE","D2D1_WINDOW_STATE_OCCLUDED","d2d1/D2D1_WINDOW_STATE","d2d1/D2D1_WINDOW_STATE_NONE","d2d1/D2D1_WINDOW_STATE_OCCLUDED","direct2d.D2D1_WINDOW_STATE"]
old-location: direct2d\D2D1_WINDOW_STATE.htm
tech.root: Direct2D
ms.assetid: 79d3a903-f29e-4d0d-9918-85fbfc846517
ms.date: 12/05/2018
ms.keywords: D2D1_WINDOW_STATE, D2D1_WINDOW_STATE enumeration [Direct2D], D2D1_WINDOW_STATE_NONE, D2D1_WINDOW_STATE_OCCLUDED, d2d1/D2D1_WINDOW_STATE, d2d1/D2D1_WINDOW_STATE_NONE, d2d1/D2D1_WINDOW_STATE_OCCLUDED, direct2d.D2D1_WINDOW_STATE
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
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
req.typenames: D2D1_WINDOW_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_WINDOW_STATE
 - d2d1/D2D1_WINDOW_STATE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1.h
api_name:
 - D2D1_WINDOW_STATE
---

# D2D1_WINDOW_STATE enumeration


## -description

Describes whether a window is occluded.

## -enum-fields

### -field D2D1_WINDOW_STATE_NONE:0x0000000

The window is not occluded.

### -field D2D1_WINDOW_STATE_OCCLUDED:0x0000001

The window is occluded.

### -field D2D1_WINDOW_STATE_FORCE_DWORD:0xffffffff

## -remarks

If the window was occluded the last time  <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw">EndDraw</a> was called, the next time the render target calls <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1hwndrendertarget-checkwindowstate">CheckWindowState</a>, it  returns <b>D2D1_WINDOW_STATE_OCCLUDED</b> regardless of the current window state. If you want to use <b>CheckWindowState</b> to check the current window state, call <b>CheckWindowState</b> after every <b>EndDraw</b> call and ignore its return value. This will ensure that your next call to <b>CheckWindowState</b> state  returns the actual window state.

## -see-also

<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1hwndrendertarget-checkwindowstate">CheckWindowState</a>

