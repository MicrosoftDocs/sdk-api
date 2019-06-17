---
UID: NC:vfw.CAPERRORCALLBACKA
title: CAPERRORCALLBACKA (vfw.h)
author: windows-sdk-content
description: The capErrorCallback function is the error callback function used with video capture. The name capErrorCallback is a placeholder for the application-supplied function name.
old-location: multimedia\caperrorcallback.htm
tech.root: Multimedia
ms.assetid: 3dc41a0e-1fed-423d-b05b-c42f361a3fb3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CAPERRORCALLBACKA, CAPERRORCALLBACKW, _win32_capErrorCallback, capErrorCallback, capErrorCallback callback, capErrorCallback callback function [Windows Multimedia], multimedia.caperrorcallback, vfw/CAPERRORCALLBACKA, vfw/CAPERRORCALLBACKW, vfw/capErrorCallback
ms.topic: callback
f1_keywords: ["vfw/capErrorCallback"]
req.header: vfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CAPERRORCALLBACKW (Unicode) and CAPERRORCALLBACKA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Vfw.h
api_name:
 - capErrorCallback
 - CAPERRORCALLBACKA
 - CAPERRORCALLBACKW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CAPERRORCALLBACKA callback function


## -description



The <b>capErrorCallback</b> function is the error callback function used with video capture. The name <b>capErrorCallback</b> is a placeholder for the application-supplied function name.



To set the callback, send the <a href="https://docs.microsoft.com/windows/desktop/Multimedia/wm-cap-set-callback-error">WM_CAP_SET_CALLBACK_ERROR</a> message to the capture window or call the <a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-capsetcallbackonerror">capSetCallbackOnError</a> macro.


## -parameters




### -param hWnd

Handle to the capture window associated with the callback function.


### -param nID

Error identification number.


### -param lpsz

Pointer to a textual description of the returned error.


## -remarks



A message identifier of zero indicates a new operation is starting and the callback function should clear the current error.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-capture-functions">Video Capture Functions</a>
 

 

