---
UID: NF:uxtheme.UpdatePanningFeedback
title: UpdatePanningFeedback function (uxtheme.h)
description: Updates clients about state of a window resulting from a panning gesture. This function can only be called after a BeginPanningFeedback call.
helpviewer_keywords: ["UpdatePanningFeedback","UpdatePanningFeedback function [Windows Controls]","_controls_UpdatePanningFeedback","_controls_UpdatePanningFeedback_cpp","controls.UpdatePanningFeedback","controls._controls_UpdatePanningFeedback","uxtheme/UpdatePanningFeedback"]
old-location: controls\UpdatePanningFeedback.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\updatepanningfeedback.htm
ms.date: 12/05/2018
ms.keywords: UpdatePanningFeedback, UpdatePanningFeedback function [Windows Controls], _controls_UpdatePanningFeedback, _controls_UpdatePanningFeedback_cpp, controls.UpdatePanningFeedback, controls._controls_UpdatePanningFeedback, uxtheme/UpdatePanningFeedback
req.header: uxtheme.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uxtheme.lib
req.dll: UxTheme.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - UpdatePanningFeedback
 - uxtheme/UpdatePanningFeedback
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-uxtheme-themes-l1-1-3.dll
 - UxTheme.dll
api_name:
 - UpdatePanningFeedback
---

# UpdatePanningFeedback function


## -description

Updates clients about state of a window resulting from a panning gesture. This function can only be called after a <a href="/windows/desktop/api/uxtheme/nf-uxtheme-beginpanningfeedback">BeginPanningFeedback</a> call.

## -parameters

### -param hwnd [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

The handle to the target window that will receive feedback. For the method to succeed, this must be the same HWND as provided in <a href="/windows/desktop/api/uxtheme/nf-uxtheme-beginpanningfeedback">BeginPanningFeedback</a>.

### -param lTotalOverpanOffsetX [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LONG</a></b>

The total displacement that the window has moved in the horizontal direction since the end of scrollable region was reached. A maximum displacement of 30 pixels is allowed.

### -param lTotalOverpanOffsetY [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LONG</a></b>

The total displacement that the window has moved in the vertical direction since the end of scrollable region was reached. A maximum displacement of 30 pixels is allowed.

### -param fInInertia [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Flag indicating whether the application is handling a WM_GESTURE message with the GF_INERTIA FLAG set.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>TRUE</b> if successful.

## -remarks

Incremental calls to this function should always pass the sum of the increments and not just the latest increment itself.