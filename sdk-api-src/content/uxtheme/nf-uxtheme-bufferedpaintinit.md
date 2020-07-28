---
UID: NF:uxtheme.BufferedPaintInit
title: BufferedPaintInit function (uxtheme.h)
description: Initialize buffered painting for the current thread.
helpviewer_keywords: ["BufferedPaintInit","BufferedPaintInit function [Windows Controls]","_shell_BufferedPaintInit","_shell_BufferedPaintInit_cpp","controls.BufferedPaintInit","controls._shell_BufferedPaintInit","uxtheme/BufferedPaintInit"]
old-location: controls\BufferedPaintInit.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\bufferedpaintinit.htm
ms.date: 12/05/2018
ms.keywords: BufferedPaintInit, BufferedPaintInit function [Windows Controls], _shell_BufferedPaintInit, _shell_BufferedPaintInit_cpp, controls.BufferedPaintInit, controls._shell_BufferedPaintInit, uxtheme/BufferedPaintInit
f1_keywords:
- uxtheme/BufferedPaintInit
dev_langs:
- c++
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
req.lib: 
req.dll: UxTheme.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- UxTheme.dll
- ext-ms-win-uxtheme-themes-l1-1-1.dll
- xamlpalwp.dll
api_name:
- BufferedPaintInit
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# BufferedPaintInit function


## -description


Initialize buffered painting for the current thread.


## -parameters






## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>BufferedPaintInit</b> is called before <a href="https://docs.microsoft.com/windows/desktop/api/uxtheme/nf-uxtheme-beginbufferedpaint">BeginBufferedPaint</a> or <a href="https://docs.microsoft.com/windows/desktop/api/uxtheme/nf-uxtheme-beginbufferedanimation">BeginBufferedAnimation</a> for each thread that uses these functions.

Each call to <b>BufferedPaintInit</b> should be matched with a call to <a href="https://docs.microsoft.com/windows/desktop/api/uxtheme/nf-uxtheme-bufferedpaintuninit">BufferedPaintUnInit</a> when calls to buffered paint APIs are no longer needed. 
			An application may call this API multiple times, as long as each call to <b>BufferedPaintInit</b> is balanced with a call to <b>BufferedPaintUnInit</b>.


This function only needs to be called once in the lifetime of a thread. Typically, this function is called before creating the main application window, or during <a href="https://docs.microsoft.com/windows/desktop/winmsg/wm-create">WM_CREATE</a>. Call <a href="https://docs.microsoft.com/windows/desktop/api/uxtheme/nf-uxtheme-bufferedpaintuninit">BufferedPaintUnInit</a> after destroying the window, or during <a href="https://docs.microsoft.com/windows/desktop/winmsg/wm-ncdestroy">WM_NCDESTROY</a>.



