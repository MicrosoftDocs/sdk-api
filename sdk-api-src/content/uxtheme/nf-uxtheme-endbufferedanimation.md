---
UID: NF:uxtheme.EndBufferedAnimation
title: EndBufferedAnimation function (uxtheme.h)
description: Renders the first frame of a buffered animation operation and starts the animation timer.
helpviewer_keywords: ["EndBufferedAnimation","EndBufferedAnimation function [Windows Controls]","_shell_EndBufferedAnimation","_shell_EndBufferedAnimation_cpp","controls.EndBufferedAnimation","controls._shell_EndBufferedAnimation","uxtheme/EndBufferedAnimation"]
old-location: controls\EndBufferedAnimation.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\endbufferedanimation.htm
ms.date: 12/05/2018
ms.keywords: EndBufferedAnimation, EndBufferedAnimation function [Windows Controls], _shell_EndBufferedAnimation, _shell_EndBufferedAnimation_cpp, controls.EndBufferedAnimation, controls._shell_EndBufferedAnimation, uxtheme/EndBufferedAnimation
req.header: uxtheme.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - EndBufferedAnimation
 - uxtheme/EndBufferedAnimation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - UxTheme.dll
api_name:
 - EndBufferedAnimation
---

# EndBufferedAnimation function


## -description

Renders the first frame of a buffered animation operation and starts the animation timer.

## -parameters

### -param hbpAnimation

Type: <b>HANIMATIONBUFFER</b>

The handle to the buffered animation context that was returned by <a href="/windows/desktop/api/uxtheme/nf-uxtheme-beginbufferedanimation">BeginBufferedAnimation</a>.

### -param fUpdateTarget

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

If <b>TRUE</b>, updates the target DC with the animation.  If <b>FALSE</b>, the animation is not started, the target DC is not updated, and the <i>hbpAnimation</i> parameter is freed.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.