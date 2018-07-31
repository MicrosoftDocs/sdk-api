---
UID: NC:vfw.CAPSTATUSCALLBACKA
title: CAPSTATUSCALLBACKA
author: windows-sdk-content
description: The capStatusCallback function is the status callback function used with video capture. The name capStatusCallback is a placeholder for the application-supplied function name.
old-location: multimedia\capstatuscallback.htm
old-project: Multimedia
ms.assetid: b48021a7-7fa1-4837-a6ca-af266fd55f4f
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: CAPSTATUSCALLBACKA, CAPSTATUSCALLBACKW, _win32_capStatusCallback, capStatusCallback, capStatusCallback callback, capStatusCallback callback function [Windows Multimedia], multimedia.capstatuscallback, vfw/CAPSTATUSCALLBACKA, vfw/CAPSTATUSCALLBACKW, vfw/capStatusCallback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: vfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CAPSTATUSCALLBACKW (Unicode) and CAPSTATUSCALLBACKA (ANSI)
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
 - UserDefined
api_location:
 - Vfw.h
api_name:
 - capStatusCallback
 - CAPSTATUSCALLBACKA
 - CAPSTATUSCALLBACKW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# CAPSTATUSCALLBACKA callback function


## -description



The <b>capStatusCallback</b> function is the status callback function used with video capture. The name <b>capStatusCallback</b> is a placeholder for the application-supplied function name.



To set the callback, send the <a href="https://msdn.microsoft.com/451ba9f9-7bfb-4c57-af6c-d5f691f39618">WM_CAP_SET_CALLBACK_STATUS</a> message to the capture window or call the <a href="https://msdn.microsoft.com/7024aa3e-d227-4c22-8259-6299e9205f53">capSetCallbackOnStatus</a> macro.


## -parameters




### -param hWnd

Handle to the capture window associated with the callback function.


### -param nID

Message identification number.


### -param lpsz

Pointer to a textual description of the returned status.


## -remarks



During capture operations, the first message sent to the callback function is always IDS_CAP_BEGIN and the last is always IDS_CAP_END. A message identifier of zero indicates a new operation is starting and the callback function should clear the current status.




## -see-also




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/0fe87fa7-9f07-48f7-958b-da385d9ddaf0">Video Capture Functions</a>
 

 

