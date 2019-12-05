---
UID: NF:vfw.capFileGetCaptureFile
title: capFileGetCaptureFile macro (vfw.h)
description: The capFileGetCaptureFile macro returns the name of the current capture file. You can use this macro or explicitly call the WM_CAP_FILE_GET_CAPTURE_FILE message.
old-location: multimedia\capfilegetcapturefile.htm
tech.root: Multimedia
ms.assetid: ea18ee1e-a53e-4032-ae9a-86f61365faaf
ms.date: 12/05/2018
ms.keywords: _win32_capFileGetCaptureFile, capFileGetCaptureFile, capFileGetCaptureFile macro [Windows Multimedia], multimedia.capfilegetcapturefile, vfw/capFileGetCaptureFile
ms.topic: macro
f1_keywords:
- vfw/capFileGetCaptureFile
dev_langs:
- c++
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
- capFileGetCaptureFile
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# capFileGetCaptureFile macro


## -description



The <b>capFileGetCaptureFile</b> macro returns the name of the current capture file. You can use this macro or explicitly call the <a href="https://docs.microsoft.com/windows/desktop/Multimedia/wm-cap-file-get-capture-file">WM_CAP_FILE_GET_CAPTURE_FILE</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


### -param szName

Pointer to an application-defined buffer used to return the name of the capture file as a null-terminated string. 


### -param wSize

Size, in bytes, of the application-defined buffer referenced by <i>szName</i>. 


## -remarks



The default capture filename is C:\CAPTURE.AVI.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-capture-macros">Video Capture Macros</a>
 

 

