---
UID: NF:uxtheme.BufferedPaintInit
title: BufferedPaintInit function
author: windows-sdk-content
description: Initialize buffered painting for the current thread.
old-location: controls\BufferedPaintInit.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\userex\functions\bufferedpaintinit.htm
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: BufferedPaintInit, BufferedPaintInit function [Windows Controls], _shell_BufferedPaintInit, _shell_BufferedPaintInit_cpp, controls.BufferedPaintInit, controls._shell_BufferedPaintInit, uxtheme/BufferedPaintInit
ms.prod: windows-hardware
ms.technology: windows-devices
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# BufferedPaintInit function


## -description


Initialize buffered painting for the current thread.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>BufferedPaintInit</b> is called before <a href="https://msdn.microsoft.com/da574e22-b08e-47e8-b874-e158862c2f9a">BeginBufferedPaint</a> or <a href="https://msdn.microsoft.com/ca7204b3-3166-4911-96f9-16a0f59ecb09">BeginBufferedAnimation</a> for each thread that uses these functions.

Each call to <b>BufferedPaintInit</b> should be matched with a call to <a href="https://msdn.microsoft.com/e6d3cae8-2f4a-4436-99c0-0606eccd3048">BufferedPaintUnInit</a> when calls to buffered paint APIs are no longer needed. 
			An application may call this API multiple times, as long as each call to <b>BufferedPaintInit</b> is balanced with a call to <b>BufferedPaintUnInit</b>.


This function only needs to be called once in the lifetime of a thread. Typically, this function is called before creating the main application window, or during <a href="https://msdn.microsoft.com/d484d0fc-bad0-4fcb-bf4b-37cbc50846ee">WM_CREATE</a>. Call <a href="https://msdn.microsoft.com/e6d3cae8-2f4a-4436-99c0-0606eccd3048">BufferedPaintUnInit</a> after destroying the window, or during <a href="https://msdn.microsoft.com/64ab268d-0e90-4401-81d3-a4da64196001">WM_NCDESTROY</a>.



