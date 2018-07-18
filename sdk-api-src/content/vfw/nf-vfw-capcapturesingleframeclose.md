---
UID: NF:vfw.capCaptureSingleFrameClose
title: capCaptureSingleFrameClose macro
author: windows-sdk-content
description: The capCaptureSingleFrameClose macro closes the capture file opened by the capCaptureSingleFrameOpen macro. You can use this macro or explicitly send the WM_CAP_SINGLE_FRAME_CLOSE message.
old-location: multimedia\capcapturesingleframeclose.htm
old-project: Multimedia
ms.assetid: d0259662-6bcf-4c04-924c-e568db335fd2
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: "_win32_capCaptureSingleFrameClose, capCaptureSingleFrameClose, capCaptureSingleFrameClose macro [Windows Multimedia], multimedia.capcapturesingleframeclose, vfw/capCaptureSingleFrameClose"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
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
tech.root: 
req.typenames: VS_FIXEDFILEINFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vfw.h
api_name:
 - capCaptureSingleFrameClose
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# capCaptureSingleFrameClose macro


## -description



The <b>capCaptureSingleFrameClose</b> macro closes the capture file opened by the <a href="https://msdn.microsoft.com/980ba1ef-d86a-47f6-9876-84b5a099d14d">capCaptureSingleFrameOpen</a> macro. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/fde5f34b-0781-49a2-a509-64192a1d9ec0">WM_CAP_SINGLE_FRAME_CLOSE</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


## -remarks



For information about installing callback functions, see the <a href="https://msdn.microsoft.com/1f9d3dba-be6d-4f7d-a80c-5bca8632e13f">capSetCallbackOnError</a> and <a href="https://msdn.microsoft.com/7e9e33cb-9213-4111-a1de-700493949f2d">capSetCallbackOnFrame</a> macros.




## -see-also




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>
 

 

