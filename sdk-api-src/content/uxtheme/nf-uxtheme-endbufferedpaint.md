---
UID: NF:uxtheme.EndBufferedPaint
title: EndBufferedPaint function (uxtheme.h)
description: Completes a buffered paint operation and frees the associated buffered paint handle.
helpviewer_keywords: ["EndBufferedPaint","EndBufferedPaint function [Windows Controls]","_shell_EndBufferedPaint","_shell_EndBufferedPaint_cpp","controls.EndBufferedPaint","controls._shell_EndBufferedPaint","uxtheme/EndBufferedPaint"]
old-location: controls\EndBufferedPaint.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\endbufferedpaint.htm
ms.date: 12/05/2018
ms.keywords: EndBufferedPaint, EndBufferedPaint function [Windows Controls], _shell_EndBufferedPaint, _shell_EndBufferedPaint_cpp, controls.EndBufferedPaint, controls._shell_EndBufferedPaint, uxtheme/EndBufferedPaint
f1_keywords:
- uxtheme/EndBufferedPaint
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
- EndBufferedPaint
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# EndBufferedPaint function


## -description


Completes a buffered paint operation and frees the associated buffered paint handle.


## -parameters




### -param hBufferedPaint

Type: <b>HPAINTBUFFER</b>

The handle of the buffered paint context, obtained through <a href="https://docs.microsoft.com/windows/desktop/api/uxtheme/nf-uxtheme-beginbufferedpaint">BeginBufferedPaint</a>.


### -param fUpdateTarget

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>TRUE</b> to copy the buffer to the target DC.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



