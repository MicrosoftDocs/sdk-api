---
UID: NF:vfw.capFileAlloc
title: capFileAlloc macro
author: windows-sdk-content
description: The capFileAlloc macro creates (preallocates) a capture file of a specified size. You can use this macro or explicitly send the WM_CAP_FILE_ALLOCATE message.
old-location: multimedia\capfilealloc.htm
old-project: Multimedia
ms.assetid: 579c5406-f44a-4ea2-9822-f09a890489fb
ms.author: windowssdkdev
ms.date: 08/17/2018
ms.keywords: "_win32_capFileAlloc, capFileAlloc, capFileAlloc macro [Windows Multimedia], multimedia.capfilealloc, vfw/capFileAlloc"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
req.header: vfw.h
req.include-header: 
req.redist: 
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
 - capFileAlloc
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# capFileAlloc macro


## -description



The <b>capFileAlloc</b> macro creates (preallocates) a capture file of a specified size. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/31ebe824-4a30-4212-9479-a5cbd8fc1e1d">WM_CAP_FILE_ALLOCATE</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


### -param dwSize

Size, in bytes, to create the capture file. 


## -remarks



You can improve streaming capture performance significantly by preallocating a capture file large enough to store an entire video clip and by defragmenting the capture file before capturing the clip.




## -see-also




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>
 

 

