---
UID: NF:vfw.capGetVideoFormatSize
title: capGetVideoFormatSize macro
author: windows-sdk-content
description: The capGetVideoFormatSize macro retrieves the size required for the video format. You can use this macro or explicitly call the WM_CAP_GET_VIDEOFORMAT message.
old-location: multimedia\capgetvideoformatsize.htm
tech.root: Multimedia
ms.assetid: 4ee78b19-4171-4da8-ad26-199067bb6db8
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: "_win32_capGetVideoFormatSize, capGetVideoFormatSize, capGetVideoFormatSize macro [Windows Multimedia], multimedia.capgetvideoformatsize, vfw/capGetVideoFormatSize"
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
 - capGetVideoFormatSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# capGetVideoFormatSize macro


## -description



The <b>capGetVideoFormatSize</b> macro retrieves the size required for the video format. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/ac72dfdb-fe1a-4007-bdce-41e5e67d076a">WM_CAP_GET_VIDEOFORMAT</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


## -remarks



Because compressed video formats vary in size requirements applications must first retrieve the size, then allocate memory, and finally request the video format data.




## -see-also




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>
 

 

