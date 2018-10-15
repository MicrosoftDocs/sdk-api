---
UID: NF:vfw.capCaptureSingleFrameOpen
title: capCaptureSingleFrameOpen macro
author: windows-sdk-content
description: The capCaptureSingleFrameOpen macro opens the capture file for single-frame capturing. Any previous information in the capture file is overwritten. You can use this macro or explicitly send the WM_CAP_SINGLE_FRAME_OPEN message.
old-location: multimedia\capcapturesingleframeopen.htm
tech.root: Multimedia
ms.assetid: 980ba1ef-d86a-47f6-9876-84b5a099d14d
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: "_win32_capCaptureSingleFrameOpen, capCaptureSingleFrameOpen, capCaptureSingleFrameOpen macro [Windows Multimedia], multimedia.capcapturesingleframeopen, vfw/capCaptureSingleFrameOpen"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vfw.h
api_name:
 - capCaptureSingleFrameOpen
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# capCaptureSingleFrameOpen macro


## -description



The <b>capCaptureSingleFrameOpen</b> macro opens the capture file for single-frame capturing. Any previous information in the capture file is overwritten. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/4814737c-4395-4c01-a68e-fac43dd291fd">WM_CAP_SINGLE_FRAME_OPEN</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


## -remarks



For information about installing callback functions, see the <a href="https://msdn.microsoft.com/1f9d3dba-be6d-4f7d-a80c-5bca8632e13f">capSetCallbackOnError</a> and <a href="https://msdn.microsoft.com/7e9e33cb-9213-4111-a1de-700493949f2d">capSetCallbackOnFrame</a> macros.




## -see-also




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>
 

 

