---
UID: NF:uxtheme.EndBufferedPaint
title: EndBufferedPaint function
author: windows-sdk-content
description: Completes a buffered paint operation and frees the associated buffered paint handle.
old-location: controls\EndBufferedPaint.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\userex\functions\endbufferedpaint.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: EndBufferedPaint, EndBufferedPaint function [Windows Controls], _shell_EndBufferedPaint, _shell_EndBufferedPaint_cpp, controls.EndBufferedPaint, controls._shell_EndBufferedPaint, uxtheme/EndBufferedPaint
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
 - EndBufferedPaint
product: Windows
targetos: Windows
req.lib: 
req.dll: UxTheme.dll
req.irql: 
req.product: Windows UI
---

# EndBufferedPaint function


## -description


Completes a buffered paint operation and frees the associated buffered paint handle.


## -parameters




### -param hBufferedPaint

Type: <b>HPAINTBUFFER</b>

The handle of the buffered paint context, obtained through <a href="https://msdn.microsoft.com/en-us/library/Bb773257(v=VS.85).aspx">BeginBufferedPaint</a>.


### -param fUpdateTarget

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

<b>TRUE</b> to copy the buffer to the target DC.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



