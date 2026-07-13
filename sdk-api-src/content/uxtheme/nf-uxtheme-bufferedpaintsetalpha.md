---
UID: NF:uxtheme.BufferedPaintSetAlpha
title: BufferedPaintSetAlpha function (uxtheme.h)
description: Sets the alpha to a specified value in a given rectangle. The alpha controls the amount of transparency applied when blending with the buffer onto the destination target device context (DC).
helpviewer_keywords: ["BufferedPaintSetAlpha","BufferedPaintSetAlpha function [Windows Controls]","_shell_BufferedPaintSetAlpha","_shell_BufferedPaintSetAlpha_cpp","controls.BufferedPaintSetAlpha","controls._shell_BufferedPaintSetAlpha","uxtheme/BufferedPaintSetAlpha"]
old-location: controls\BufferedPaintSetAlpha.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\bufferedpaintsetalpha.htm
ms.date: 12/05/2018
ms.keywords: BufferedPaintSetAlpha, BufferedPaintSetAlpha function [Windows Controls], _shell_BufferedPaintSetAlpha, _shell_BufferedPaintSetAlpha_cpp, controls.BufferedPaintSetAlpha, controls._shell_BufferedPaintSetAlpha, uxtheme/BufferedPaintSetAlpha
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
 - BufferedPaintSetAlpha
 - uxtheme/BufferedPaintSetAlpha
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
 - BufferedPaintSetAlpha
---

# BufferedPaintSetAlpha function


## -description

Sets the alpha to a specified value in a given rectangle. The alpha controls the amount of transparency applied when blending with the buffer onto the destination target device context (DC).

## -parameters

### -param hBufferedPaint

Type: <b>HPAINTBUFFER</b>

The handle of the buffered paint context, obtained through <a href="/windows/desktop/api/uxtheme/nf-uxtheme-beginbufferedpaint">BeginBufferedPaint</a>.

### -param prc [in]

Type: <b>const <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that specifies the rectangle in which to set the alpha. Set this parameter to <b>NULL</b> to specify the entire buffer.

### -param alpha

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BYTE</a></b>

The alpha value to set. The alpha value can range from zero (fully transparent) to 255 (fully opaque).

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This function sets the alpha value for each pixel in the target rectangle. Passing an alpha value of 255 makes pixels fully opaque. The <b>BufferedPaintMakeOpaque</b> macro, which is  defined in uxtheme.h, sets alpha values to 255.  It is typically used to call GDI to draw into a memory buffer and then to make it opaque in order to draw it on glass.