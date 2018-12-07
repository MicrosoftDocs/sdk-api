---
UID: NF:vfw.capGrabFrame
title: capGrabFrame macro
author: windows-sdk-content
description: The capGrabFrame macro retrieves and displays a single frame from the capture driver. After capture, overlay and preview are disabled. You can use this macro or explicitly call the WM_CAP_GRAB_FRAME message.
old-location: multimedia\capgrabframe.htm
tech.root: Multimedia
ms.assetid: bd306414-74a9-4683-ad63-797a37152e8f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "_win32_capGrabFrame, capGrabFrame, capGrabFrame macro [Windows Multimedia], multimedia.capgrabframe, vfw/capGrabFrame"
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
 - capGrabFrame
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# capGrabFrame macro


## -description



The <b>capGrabFrame</b> macro retrieves and displays a single frame from the capture driver. After capture, overlay and preview are disabled. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/91d58c1c-53b9-4813-88c2-7a1acf641d96">WM_CAP_GRAB_FRAME</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


## -remarks



For information about installing callback functions, see the <a href="https://msdn.microsoft.com/1f9d3dba-be6d-4f7d-a80c-5bca8632e13f">capSetCallbackOnError</a> and <a href="https://msdn.microsoft.com/7e9e33cb-9213-4111-a1de-700493949f2d">capSetCallbackOnFrame</a> macros.




## -see-also




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>
 

 

