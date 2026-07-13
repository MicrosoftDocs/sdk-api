---
UID: NF:vfw.capCreateCaptureWindowA
title: capCreateCaptureWindowA function (vfw.h)
description: The capCreateCaptureWindow function creates a capture window. (ANSI)
helpviewer_keywords: ["capCreateCaptureWindowA", "vfw/capCreateCaptureWindowA"]
old-location: multimedia\capcreatecapturewindow.htm
tech.root: Multimedia
ms.assetid: b08785f8-9850-4d3b-acbf-b065f45910e1
ms.date: 12/05/2018
ms.keywords: _win32_capCreateCaptureWindow, capCreateCaptureWindow, capCreateCaptureWindow function [Windows Multimedia], capCreateCaptureWindowA, capCreateCaptureWindowW, multimedia.capcreatecapturewindow, vfw/capCreateCaptureWindow, vfw/capCreateCaptureWindowA, vfw/capCreateCaptureWindowW
req.header: vfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: capCreateCaptureWindowW (Unicode) and capCreateCaptureWindowA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Vfw32.lib
req.dll: Avicap32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - capCreateCaptureWindowA
 - vfw/capCreateCaptureWindowA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Avicap32.dll
api_name:
 - capCreateCaptureWindow
 - capCreateCaptureWindowA
 - capCreateCaptureWindowW
---

# capCreateCaptureWindowA function


## -description

The <b>capCreateCaptureWindow</b> function creates a capture window.

## -parameters

### -param lpszWindowName

Null-terminated string containing the name used for the capture window.

### -param dwStyle

Window styles used for the capture window. Window styles are described with the <a href="/windows/desktop/api/winuser/nf-winuser-createwindowexa">CreateWindowEx</a> function.

### -param x

The x-coordinate of the upper left corner of the capture window.

### -param y

The y-coordinate of the upper left corner of the capture window.

### -param nWidth

Width of the capture window.

### -param nHeight

Height of the capture window.

### -param hwndParent

Handle to the parent window.

### -param nID

Window identifier.

## -returns

Returns a handle of the capture window if successful or <b>NULL</b> otherwise.

## -see-also

<a href="/windows/desktop/Multimedia/creating-a-capture-window">Creating a Capture Window</a>



<a href="/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="/windows/desktop/Multimedia/video-capture-functions">Video Capture Functions</a>

## -remarks

> [!NOTE]
> The vfw.h header defines capCreateCaptureWindow as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
