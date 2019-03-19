---
UID: NF:vfw.capPreviewRate
title: capPreviewRate macro (vfw.h)
author: windows-sdk-content
description: The capPreviewRate macro sets the frame display rate in preview mode. You can use this macro or explicitly call the WM_CAP_SET_PREVIEWRATE message.
old-location: multimedia\cappreviewrate.htm
tech.root: Multimedia
ms.assetid: 72d885cb-5a48-4403-a668-c3c437405317
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "_win32_capPreviewRate, capPreviewRate, capPreviewRate macro [Windows Multimedia], multimedia.cappreviewrate, vfw/capPreviewRate"
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
 - capPreviewRate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# capPreviewRate macro


## -description



The <b>capPreviewRate</b> macro sets the frame display rate in preview mode. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/1189ad4a-1f32-4684-920b-ee3c26ef97f8">WM_CAP_SET_PREVIEWRATE</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


### -param wMS

Rate, in milliseconds, at which new frames are captured and displayed. 


## -remarks



The preview mode uses substantial CPU resources. Applications can disable preview or lower the preview rate when another application has the focus. During streaming video capture, the previewing task is lower priority than writing frames to disk, and preview frames are displayed only if no other buffers are available for writing.




## -see-also




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>
 

 

