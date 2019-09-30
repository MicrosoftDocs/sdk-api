---
UID: NF:vfw.capFileAlloc
title: capFileAlloc macro (vfw.h)
author: windows-sdk-content
description: The capFileAlloc macro creates (preallocates) a capture file of a specified size. You can use this macro or explicitly send the WM_CAP_FILE_ALLOCATE message.
old-location: multimedia\capfilealloc.htm
tech.root: Multimedia
ms.assetid: 579c5406-f44a-4ea2-9822-f09a890489fb
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "_win32_capFileAlloc, capFileAlloc, capFileAlloc macro [Windows Multimedia], multimedia.capfilealloc, vfw/capFileAlloc"
ms.topic: macro
f1_keywords: 
 - "vfw/capFileAlloc"
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
 - capFileAlloc
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# capFileAlloc macro


## -description



The <b>capFileAlloc</b> macro creates (preallocates) a capture file of a specified size. You can use this macro or explicitly send the <a href="https://docs.microsoft.com/windows/desktop/Multimedia/wm-cap-file-allocate">WM_CAP_FILE_ALLOCATE</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


### -param dwSize

Size, in bytes, to create the capture file. 


## -remarks



You can improve streaming capture performance significantly by preallocating a capture file large enough to store an entire video clip and by defragmenting the capture file before capturing the clip.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-capture-macros">Video Capture Macros</a>
 

 

