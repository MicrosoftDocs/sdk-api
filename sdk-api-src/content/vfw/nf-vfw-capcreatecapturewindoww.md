---
UID: NF:vfw.capCreateCaptureWindowW
title: capCreateCaptureWindowW function (vfw.h)
description: The capCreateCaptureWindow function creates a capture window.
helpviewer_keywords: ["_win32_capCreateCaptureWindow","capCreateCaptureWindow","capCreateCaptureWindow function [Windows Multimedia]","capCreateCaptureWindowA","capCreateCaptureWindowW","multimedia.capcreatecapturewindow","vfw/capCreateCaptureWindow","vfw/capCreateCaptureWindowA","vfw/capCreateCaptureWindowW"]
old-location: multimedia\capcreatecapturewindow.htm
tech.root: Multimedia
ms.assetid: b08785f8-9850-4d3b-acbf-b065f45910e1
ms.date: 12/05/2018
ms.keywords: _win32_capCreateCaptureWindow, capCreateCaptureWindow, capCreateCaptureWindow function [Windows Multimedia], capCreateCaptureWindowA, capCreateCaptureWindowW, multimedia.capcreatecapturewindow, vfw/capCreateCaptureWindow, vfw/capCreateCaptureWindowA, vfw/capCreateCaptureWindowW
f1_keywords:
- vfw/capCreateCaptureWindow
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# capCreateCaptureWindowW function


## -description



The <b>capCreateCaptureWindow</b> function creates a capture window.




## -parameters




### -param lpszWindowName

Null-terminated string containing the name used for the capture window.
          


### -param dwStyle

Window styles used for the capture window. Window styles are described with the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-createwindowexa">CreateWindowEx</a> function.
          


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




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/creating-a-capture-window">Creating a Capture Window</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-capture-functions">Video Capture Functions</a>
 

 

