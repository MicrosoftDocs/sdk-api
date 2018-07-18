---
UID: NF:vfw.capSetCallbackOnFrame
title: capSetCallbackOnFrame macro
author: windows-sdk-content
description: The capSetCallbackOnFrame macro sets a preview callback function in the application. AVICap calls this procedure when the capture window captures preview frames. You can use this macro or explicitly call the WM_CAP_SET_CALLBACK_FRAME message.
old-location: multimedia\capsetcallbackonframe.htm
old-project: Multimedia
ms.assetid: 7e9e33cb-9213-4111-a1de-700493949f2d
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: "_win32_capSetCallbackOnFrame, capSetCallbackOnFrame, capSetCallbackOnFrame macro [Windows Multimedia], multimedia.capsetcallbackonframe, vfw/capSetCallbackOnFrame"
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
 - capSetCallbackOnFrame
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# capSetCallbackOnFrame macro


## -description



The <b>capSetCallbackOnFrame</b> macro sets a preview callback function in the application. AVICap calls this procedure when the capture window captures preview frames. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/3882e6f6-c48c-4e50-9697-cbdf5b9342a5">WM_CAP_SET_CALLBACK_FRAME</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


### -param fpProc

Pointer to the preview callback function, of type <a href="https://msdn.microsoft.com/e21d7563-0ca8-4777-9fb0-de7c1c4ae618">capVideoStreamCallback</a>. Specify <b>NULL</b> for this parameter to disable a previously installed callback function. 


## -remarks



The capture window calls the callback function before displaying preview frames. This allows an application to modify the frame if desired. This callback function is not used during streaming video capture.




## -see-also




<a href="https://msdn.microsoft.com/37002ee0-9907-4aab-93cc-50fe9cd21cff">Creating a Frame Callback Function</a>



<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>
 

 

