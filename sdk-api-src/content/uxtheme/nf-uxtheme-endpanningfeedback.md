---
UID: NF:uxtheme.EndPanningFeedback
title: EndPanningFeedback function (uxtheme.h)
description: Terminates any existing animation that was in process or set up by BeginPanningFeedback and UpdatePanningFeedback.
helpviewer_keywords: ["EndPanningFeedback","EndPanningFeedback function [Windows Controls]","_controls_EndPanningFeedback","_controls_EndPanningFeedback_cpp","controls.EndPanningFeedback","controls._controls_EndPanningFeedback","uxtheme/EndPanningFeedback"]
old-location: controls\EndPanningFeedback.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\endpanningfeedback.htm
ms.date: 12/05/2018
ms.keywords: EndPanningFeedback, EndPanningFeedback function [Windows Controls], _controls_EndPanningFeedback, _controls_EndPanningFeedback_cpp, controls.EndPanningFeedback, controls._controls_EndPanningFeedback, uxtheme/EndPanningFeedback
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
 - EndPanningFeedback
 - uxtheme/EndPanningFeedback
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
 - EndPanningFeedback
---

# EndPanningFeedback function


## -description

Terminates any existing animation that was in process or set up by <a href="/windows/desktop/api/uxtheme/nf-uxtheme-beginpanningfeedback">BeginPanningFeedback</a> and <a href="/windows/desktop/api/uxtheme/nf-uxtheme-updatepanningfeedback">UpdatePanningFeedback</a>.

## -parameters

### -param hwnd [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

The handle to the target window that will receive feedback.

### -param fAnimateBack [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Flag that indicates whether the displaced window should return to the original position using animation. If <b>FALSE</b>, the method restore the moved window using a direct jump.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>TRUE</b> if successful.

## -remarks

This function can only be called after a <a href="/windows/desktop/api/uxtheme/nf-uxtheme-beginpanningfeedback">BeginPanningFeedback</a> call.