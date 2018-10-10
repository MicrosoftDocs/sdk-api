---
UID: NF:d2d1.ID2D1HwndRenderTarget.CheckWindowState
title: ID2D1HwndRenderTarget::CheckWindowState
author: windows-sdk-content
description: Indicates whether the HWND associated with this render target is occluded.
old-location: direct2d\ID2D1HwndRenderTarget_CheckWindowState.htm
tech.root: Direct2D
ms.assetid: f40d46dc-04ec-4d11-bc3e-96043b16dcb3
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: CheckWindowState, CheckWindowState method [Direct2D], CheckWindowState method [Direct2D],ID2D1HwndRenderTarget interface, ID2D1HwndRenderTarget interface [Direct2D],CheckWindowState method, ID2D1HwndRenderTarget.CheckWindowState, ID2D1HwndRenderTarget::CheckWindowState, d2d1/ID2D1HwndRenderTarget::CheckWindowState, direct2d.ID2D1HwndRenderTarget_CheckWindowState
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1HwndRenderTarget.CheckWindowState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1HwndRenderTarget::CheckWindowState


## -description


Indicates whether the HWND associated with this render target is occluded.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/79d3a903-f29e-4d0d-9918-85fbfc846517">D2D1_WINDOW_STATE</a></b>

A value that indicates whether the HWND associated with this render target is occluded.




## -remarks



<div class="alert"><b>Note</b>  If the window was occluded the last time  that <a href="https://msdn.microsoft.com/a8f24501-4e85-4981-bb38-2bd6333a7b49">EndDraw</a> was called, the next time that the render target calls <b>CheckWindowState</b>, it will return <a href="https://msdn.microsoft.com/79d3a903-f29e-4d0d-9918-85fbfc846517">D2D1_WINDOW_STATE_OCCLUDED</a> regardless of the current window state. If you want to use <b>CheckWindowState</b> to determine the current window state, you should call <b>CheckWindowState</b> after every <b>EndDraw</b> call and ignore its return value. This call will ensure that your next call to <b>CheckWindowState</b> state will return the actual window state.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/860342cc-989c-4432-b879-07f3da07d50a">ID2D1HwndRenderTarget</a>
 

 

