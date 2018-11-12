---
UID: NF:vfw.capFileGetCaptureFile
title: capFileGetCaptureFile macro
author: windows-sdk-content
description: The capFileGetCaptureFile macro returns the name of the current capture file. You can use this macro or explicitly call the WM_CAP_FILE_GET_CAPTURE_FILE message.
old-location: multimedia\capfilegetcapturefile.htm
tech.root: Multimedia
ms.assetid: ea18ee1e-a53e-4032-ae9a-86f61365faaf
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: "_win32_capFileGetCaptureFile, capFileGetCaptureFile, capFileGetCaptureFile macro [Windows Multimedia], multimedia.capfilegetcapturefile, vfw/capFileGetCaptureFile"
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
 - capFileGetCaptureFile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# capFileGetCaptureFile macro


## -description



The <b>capFileGetCaptureFile</b> macro returns the name of the current capture file. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/86ce2904-834d-449f-9ef8-5a158c55bbaa">WM_CAP_FILE_GET_CAPTURE_FILE</a> message.




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




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>
 

 

