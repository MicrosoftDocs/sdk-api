---
UID: NF:uxtheme.BufferedPaintClear
title: BufferedPaintClear function
author: windows-driver-content
description: Clears a specified rectangle in the buffer to ARGB = {0,0,0,0}.
old-location: controls\BufferedPaintClear.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\bufferedpaintclear.htm
ms.author: windowsdriverdev
ms.date: 4/27/2018
ms.keywords: BufferedPaintClear, BufferedPaintClear function [Windows Controls], _shell_BufferedPaintClear, _shell_BufferedPaintClear_cpp, controls.BufferedPaintClear, controls._shell_BufferedPaintClear, uxtheme/BufferedPaintClear
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
req.typenames: BP_BUFFERFORMAT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	UxTheme.dll
-	ext-ms-win-uxtheme-themes-l1-1-1.dll
-	xamlpalwp.dll
api_name:
-	BufferedPaintClear
product: Windows
targetos: Windows
req.lib: 
req.dll: UxTheme.dll
req.irql: 
req.product: Windows UI
---

# BufferedPaintClear function


## -description


Clears a specified rectangle in the buffer to ARGB = {0,0,0,0}.


## -parameters




### -param hBufferedPaint

Type: <b>HPAINTBUFFER</b>

The handle of the buffered paint context, obtained through <a href="https://msdn.microsoft.com/da574e22-b08e-47e8-b874-e158862c2f9a">BeginBufferedPaint</a>.


### -param prc [in]

Type: <b>const <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that specifies the rectangle to clear. Set this parameter to <b>NULL</b> to specify the entire buffer.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function accesses the buffer bits directly and is therefore faster than calling a GDI function to erase the buffer. 



