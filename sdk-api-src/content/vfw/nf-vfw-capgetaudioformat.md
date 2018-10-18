---
UID: NF:vfw.capGetAudioFormat
title: capGetAudioFormat macro
author: windows-sdk-content
description: The capGetAudioFormat macro obtains the audio format. You can use this macro or explicitly call the WM_CAP_GET_AUDIOFORMAT message.
old-location: multimedia\capgetaudioformat.htm
tech.root: Multimedia
ms.assetid: 11a91da3-dd22-4828-9845-dc29e73c4526
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: "_win32_capGetAudioFormat, capGetAudioFormat, capGetAudioFormat macro [Windows Multimedia], multimedia.capgetaudioformat, vfw/capGetAudioFormat"
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
 - capGetAudioFormat
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# capGetAudioFormat macro


## -description



The <b>capGetAudioFormat</b> macro obtains the audio format. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/25e58863-2b1e-4ed8-9f34-c39617a15bc1">WM_CAP_GET_AUDIOFORMAT</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


### -param s

Pointer to a <a href="https://msdn.microsoft.com/bd0f96ec-d26a-4e6f-8802-50e8ff207f54">WAVEFORMATEX</a> structure, or <b>NULL</b>. If the value is <b>NULL</b>, the size, in bytes, required to hold the <b>WAVEFORMATEX</b> structure is returned. 


### -param wSize

Size, in bytes, of the structure referenced by <i>s</i>. 


## -remarks



Because compressed audio formats vary in size requirements applications must first retrieve the size, then allocate memory, and finally request the audio format data.




## -see-also




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>
 

 

