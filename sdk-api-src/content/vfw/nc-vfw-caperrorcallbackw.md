---
UID: NC:vfw.CAPERRORCALLBACKW
title: CAPERRORCALLBACKW
author: windows-driver-content
description: The capErrorCallback function is the error callback function used with video capture. The name capErrorCallback is a placeholder for the application-supplied function name.
old-location: multimedia\caperrorcallback.htm
old-project: Multimedia
ms.assetid: 3dc41a0e-1fed-423d-b05b-c42f361a3fb3
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: CAPERRORCALLBACKA, CAPERRORCALLBACKW, _win32_capErrorCallback, capErrorCallback, capErrorCallback callback, capErrorCallback callback function [Windows Multimedia], multimedia.caperrorcallback, vfw/CAPERRORCALLBACKA, vfw/CAPERRORCALLBACKW, vfw/capErrorCallback
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
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
req.typenames: VS_FIXEDFILEINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Vfw.h
api_name:
-	capErrorCallback
-	CAPERRORCALLBACKA
-	CAPERRORCALLBACKW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# CAPERRORCALLBACKW callback function


## -description



The <b>capErrorCallback</b> function is the error callback function used with video capture. The name <b>capErrorCallback</b> is a placeholder for the application-supplied function name.



To set the callback, send the <a href="https://msdn.microsoft.com/4eb57515-9b5a-466c-bbaa-fdee3bca19db">WM_CAP_SET_CALLBACK_ERROR</a> message to the capture window or call the <a href="https://msdn.microsoft.com/1f9d3dba-be6d-4f7d-a80c-5bca8632e13f">capSetCallbackOnError</a> macro.


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




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/0fe87fa7-9f07-48f7-958b-da385d9ddaf0">Video Capture Functions</a>
 

 

