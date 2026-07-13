---
UID: NF:uxtheme.BeginPanningFeedback
title: BeginPanningFeedback function (uxtheme.h)
description: Notifies the system to send feedback about a target window affected by panning gestures.
helpviewer_keywords: ["BeginPanningFeedback","BeginPanningFeedback function [Windows Controls]","_controls_BeginPanningFeedback","_controls_BeginPanningFeedback_cpp","controls.BeginPanningFeedback","controls._controls_BeginPanningFeedback","uxtheme/BeginPanningFeedback"]
old-location: controls\BeginPanningFeedback.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\beginpanningfeedback.htm
ms.date: 12/05/2018
ms.keywords: BeginPanningFeedback, BeginPanningFeedback function [Windows Controls], _controls_BeginPanningFeedback, _controls_BeginPanningFeedback_cpp, controls.BeginPanningFeedback, controls._controls_BeginPanningFeedback, uxtheme/BeginPanningFeedback
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
 - BeginPanningFeedback
 - uxtheme/BeginPanningFeedback
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
 - BeginPanningFeedback
---

# BeginPanningFeedback function


## -description

Notifies the system to send feedback about a target window affected by panning gestures.

## -parameters

### -param hwnd [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

The handle to the target window that will receive feedback.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

TRUE, if successful.

## -remarks

This function must be called before either the <a href="/windows/desktop/api/uxtheme/nf-uxtheme-updatepanningfeedback">UpdatePanningFeedback</a> or <a href="/windows/desktop/api/uxtheme/nf-uxtheme-endpanningfeedback">EndPanningFeedback</a> functions can be called.