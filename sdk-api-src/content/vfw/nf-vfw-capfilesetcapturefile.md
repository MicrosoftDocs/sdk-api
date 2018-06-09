---
UID: NF:vfw.capFileSetCaptureFile
title: capFileSetCaptureFile macro
author: windows-sdk-content
description: The capFileSetCaptureFile macro names the file used for video capture. You can use this macro or explicitly call the WM_CAP_FILE_SET_CAPTURE_FILE message.
old-location: multimedia\capfilesetcapturefile.htm
old-project: Multimedia
ms.assetid: 47c69c62-5455-401e-adba-9a0eced548cf
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: "_win32_capFileSetCaptureFile, capFileSetCaptureFile, capFileSetCaptureFile macro [Windows Multimedia], multimedia.capfilesetcapturefile, vfw/capFileSetCaptureFile"
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
 - capFileSetCaptureFile
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# capFileSetCaptureFile macro


## -description



The <b>capFileSetCaptureFile</b> macro names the file used for video capture. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/d96e498b-6322-4d48-a5d7-156e95f23740">WM_CAP_FILE_SET_CAPTURE_FILE</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


### -param szName

Pointer to the null-terminated string that contains the name of the capture file to use. 


## -remarks



This message stores the filename in an internal structure. It does not create, allocate, or open the specified file. The default capture filename is C:\CAPTURE.AVI.




## -see-also




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>
 

 

