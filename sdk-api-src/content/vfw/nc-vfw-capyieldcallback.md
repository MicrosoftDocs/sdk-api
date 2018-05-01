---
UID: NC:vfw.CAPYIELDCALLBACK
title: CAPYIELDCALLBACK
author: windows-driver-content
description: The capYieldCallback function is the yield callback function used with video capture. The name capYieldCallback is a placeholder for the application-supplied function name.
old-location: multimedia\capyieldcallback.htm
old-project: Multimedia
ms.assetid: 4d92ab5e-5cde-4fed-a661-0458b5399c2a
ms.author: windowsdriverdev
ms.date: 4/25/2018
ms.keywords: "_win32_capYieldCallback, capYieldCallback, capYieldCallback callback function [Windows Multimedia], multimedia.capyieldcallback, vfw/capYieldCallback"
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
req.unicode-ansi: 
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
-	capYieldCallback
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# CAPYIELDCALLBACK callback


## -description



The <b>capYieldCallback</b> function is the yield callback function used with video capture. The name <b>capYieldCallback</b> is a placeholder for the application-supplied function name.



To set the callback, send the <a href="https://msdn.microsoft.com/d978dc3b-4336-46a4-85ae-7d588a63489b">WM_CAP_SET_CALLBACK_YIELD</a> message to the capture window or call the <a href="https://msdn.microsoft.com/efddbcbc-f1e3-451c-928e-984eea187de2">capSetCallbackOnYield</a> macro.


## -parameters




### -param hWnd

Handle to the capture window associated with the callback function.


## -remarks



The capture window calls the yield callback function at least once for every captured video frame, but the exact rate depends on the frame rate and the overhead of the capture driver and disk.




## -see-also




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/0fe87fa7-9f07-48f7-958b-da385d9ddaf0">Video Capture Functions</a>
 

 

