---
UID: NF:vfw.capGetVideoFormat
title: capGetVideoFormat macro
author: windows-sdk-content
description: The capGetVideoFormat macro retrieves a copy of the video format in use. You can use this macro or explicitly call the WM_CAP_GET_VIDEOFORMAT message.
old-location: multimedia\capgetvideoformat.htm
tech.root: Multimedia
ms.assetid: 2013bf9c-3759-440a-a62c-2ba3c54441c1
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: "_win32_capGetVideoFormat, capGetVideoFormat, capGetVideoFormat macro [Windows Multimedia], multimedia.capgetvideoformat, vfw/capGetVideoFormat"
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
 - capGetVideoFormat
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# capGetVideoFormat macro


## -description



The <b>capGetVideoFormat</b> macro retrieves a copy of the video format in use. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/ac72dfdb-fe1a-4007-bdce-41e5e67d076a">WM_CAP_GET_VIDEOFORMAT</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


### -param s

Pointer to a <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> structure. You can also specify <b>NULL</b> to retrieve the number of bytes needed by <b>BITMAPINFO</b>. 


### -param wSize

Size, in bytes, of the structure referenced by <i>s</i>. 


## -remarks



Because compressed video formats vary in size requirements applications must first retrieve the size, then allocate memory, and finally request the video format data.




## -see-also




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>
 

 

