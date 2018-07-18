---
UID: NF:vfw.capGetAudioFormatSize
title: capGetAudioFormatSize macro
author: windows-sdk-content
description: The capGetAudioFormatSize macro obtains the size of the audio format. You can use this macro or explicitly call the WM_CAP_GET_AUDIOFORMAT message.
old-location: multimedia\capgetaudioformatsize.htm
old-project: Multimedia
ms.assetid: 6f2dbedb-bece-4082-aa68-c2390c75b4d7
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: "_win32_capGetAudioFormatSize, capGetAudioFormatSize, capGetAudioFormatSize macro [Windows Multimedia], multimedia.capgetaudioformatsize, vfw/capGetAudioFormatSize"
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
 - capGetAudioFormatSize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# capGetAudioFormatSize macro


## -description



The <b>capGetAudioFormatSize</b> macro obtains the size of the audio format. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/25e58863-2b1e-4ed8-9f34-c39617a15bc1">WM_CAP_GET_AUDIOFORMAT</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


## -remarks



Because compressed audio formats vary in size requirements applications must first retrieve the size, then allocate memory, and finally request the audio format data.




## -see-also




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>
 

 

