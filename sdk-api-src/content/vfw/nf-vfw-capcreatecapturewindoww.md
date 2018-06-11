---
UID: NF:vfw.capCreateCaptureWindowW
title: capCreateCaptureWindowW function
author: windows-sdk-content
description: The capCreateCaptureWindow function creates a capture window.
old-location: multimedia\capcreatecapturewindow.htm
old-project: Multimedia
ms.assetid: b08785f8-9850-4d3b-acbf-b065f45910e1
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: "_win32_capCreateCaptureWindow, capCreateCaptureWindow, capCreateCaptureWindow function [Windows Multimedia], capCreateCaptureWindowA, capCreateCaptureWindowW, multimedia.capcreatecapturewindow, vfw/capCreateCaptureWindow, vfw/capCreateCaptureWindowA, vfw/capCreateCaptureWindowW"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: VS_FIXEDFILEINFO
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
product: Windows
targetos: Windows
req.lib: Vfw32.lib
req.dll: Avicap32.dll
req.irql: 
req.product: Windows UI
---

# capCreateCaptureWindowW function


## -description



The <b>capCreateCaptureWindow</b> function creates a capture window.




## -parameters




### -param lpszWindowName


            Null-terminated string containing the name used for the capture window.
          


### -param dwStyle


            Window styles used for the capture window. Window styles are described with the <a href="winui._win32_CreateWindowEx">CreateWindowEx</a> function.
          


### -param x


            The x-coordinate of the upper left corner of the capture window.
          


### -param y


            The y-coordinate of the upper left corner of the capture window.
          


### -param nWidth


            Width of the capture window.
          


### -param nHeight


            Height of the capture window.
          


### -param hwndParent

TBD


### -param nID


            Window identifier.
          


#### - hWnd


            Handle to the parent window.
          


## -returns




            Returns a handle of the capture window if successful or <b>NULL</b> otherwise.
          




## -see-also




<a href="https://msdn.microsoft.com/a727ce14-9b12-4f21-bab4-fa2eb245dce7">Creating a Capture Window</a>



<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/0fe87fa7-9f07-48f7-958b-da385d9ddaf0">Video Capture Functions</a>
 

 

