---
UID: NF:uxtheme.BufferedPaintSetAlpha
title: BufferedPaintSetAlpha function
author: windows-sdk-content
description: Sets the alpha to a specified value in a given rectangle. The alpha controls the amount of transparency applied when blending with the buffer onto the destination target device context (DC).
old-location: controls\BufferedPaintSetAlpha.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\bufferedpaintsetalpha.htm
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: BufferedPaintSetAlpha, BufferedPaintSetAlpha function [Windows Controls], _shell_BufferedPaintSetAlpha, _shell_BufferedPaintSetAlpha_cpp, controls.BufferedPaintSetAlpha, controls._shell_BufferedPaintSetAlpha, uxtheme/BufferedPaintSetAlpha
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
api_name:
 - BufferedPaintSetAlpha
product: Windows
targetos: Windows
req.lib: 
req.dll: UxTheme.dll
req.irql: 
req.product: Windows UI
---

# BufferedPaintSetAlpha function


## -description


Sets the alpha to a specified value in a given rectangle. The alpha controls the amount of transparency applied when blending with the buffer onto the destination target device context (DC).



## -parameters




### -param hBufferedPaint

Type: <b>HPAINTBUFFER</b>

The handle of the buffered paint context, obtained through <a href="https://msdn.microsoft.com/da574e22-b08e-47e8-b874-e158862c2f9a">BeginBufferedPaint</a>.


### -param prc [in]

Type: <b>const <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that specifies the rectangle in which to set the alpha. Set this parameter to <b>NULL</b> to specify the entire buffer.


### -param alpha

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a></b>

The alpha value to set. The alpha value can range from zero (fully transparent) to 255 (fully opaque).


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function sets the alpha value for each pixel in the target rectangle. Passing an alpha value of 255 makes pixels fully opaque. The <b>BufferedPaintMakeOpaque</b> macro, which is  defined in uxtheme.h, sets alpha values to 255.  It is typically used to call GDI to draw into a memory buffer and then to make it opaque in order to draw it on glass.



