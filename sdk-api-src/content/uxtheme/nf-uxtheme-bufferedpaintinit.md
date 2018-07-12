---
UID: NF:uxtheme.BufferedPaintInit
title: BufferedPaintInit function
author: windows-sdk-content
description: Initialize buffered painting for the current thread.
old-location: controls\BufferedPaintInit.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\userex\functions\bufferedpaintinit.htm
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: BufferedPaintInit, BufferedPaintInit function [Windows Controls], _shell_BufferedPaintInit, _shell_BufferedPaintInit_cpp, controls.BufferedPaintInit, controls._shell_BufferedPaintInit, uxtheme/BufferedPaintInit
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: BP_BUFFERFORMAT
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
product: Windows
targetos: Windows
req.lib: 
req.dll: UxTheme.dll
req.irql: 
req.product: Windows UI
---

# BufferedPaintInit function


## -description


Initialize buffered painting for the current thread.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>BufferedPaintInit</b> is called before <a href="https://msdn.microsoft.com/library/Bb773257(v=VS.85).aspx">BeginBufferedPaint</a> or <a href="https://msdn.microsoft.com/library/Bb773252(v=VS.85).aspx">BeginBufferedAnimation</a> for each thread that uses these functions.

Each call to <b>BufferedPaintInit</b> should be matched with a call to <a href="https://msdn.microsoft.com/library/Bb773284(v=VS.85).aspx">BufferedPaintUnInit</a> when calls to buffered paint APIs are no longer needed. 
			An application may call this API multiple times, as long as each call to <b>BufferedPaintInit</b> is balanced with a call to <b>BufferedPaintUnInit</b>.


This function only needs to be called once in the lifetime of a thread. Typically, this function is called before creating the main application window, or during <a href="https://msdn.microsoft.com/library/ms632619(v=VS.85).aspx">WM_CREATE</a>. Call <a href="https://msdn.microsoft.com/library/Bb773284(v=VS.85).aspx">BufferedPaintUnInit</a> after destroying the window, or during <a href="https://msdn.microsoft.com/library/ms632636(v=VS.85).aspx">WM_NCDESTROY</a>.



