---
UID: NF:uxtheme.BufferedPaintUnInit
title: BufferedPaintUnInit function (uxtheme.h)
description: Closes down buffered painting for the current thread. Called once for each call to BufferedPaintInit after calls to BeginBufferedPaint are no longer needed.
helpviewer_keywords: ["BufferedPaintUnInit","BufferedPaintUnInit function [Windows Controls]","_shell_BufferedPaintUnInit","_shell_BufferedPaintUnInit_cpp","controls.BufferedPaintUnInit","controls._shell_BufferedPaintUnInit","uxtheme/BufferedPaintUnInit"]
old-location: controls\BufferedPaintUnInit.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\bufferedpaintuninit.htm
ms.date: 12/05/2018
ms.keywords: BufferedPaintUnInit, BufferedPaintUnInit function [Windows Controls], _shell_BufferedPaintUnInit, _shell_BufferedPaintUnInit_cpp, controls.BufferedPaintUnInit, controls._shell_BufferedPaintUnInit, uxtheme/BufferedPaintUnInit
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - BufferedPaintUnInit
 - uxtheme/BufferedPaintUnInit
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-uxtheme-themes-l1-1-3.dll
 - ext-ms-win-uxtheme-themes-l1-1-2.dll
 - UxTheme.dll
 - ext-ms-win-uxtheme-themes-l1-1-1.dll
 - xamlpalwp.dll
api_name:
 - BufferedPaintUnInit
---

# BufferedPaintUnInit function


## -description

Closes down buffered painting for the current thread. Called once for each call to <a href="/windows/desktop/api/uxtheme/nf-uxtheme-bufferedpaintinit">BufferedPaintInit</a> after calls to <a href="/windows/desktop/api/uxtheme/nf-uxtheme-beginbufferedpaint">BeginBufferedPaint</a> are no longer needed.



## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.
