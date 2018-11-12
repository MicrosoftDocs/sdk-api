---
UID: NF:vfw.capSetAudioFormat
title: capSetAudioFormat macro
author: windows-sdk-content
description: The capSetAudioFormat macro sets the audio format to use when performing streaming or step capture. You can use this macro or explicitly call the WM_CAP_SET_AUDIOFORMAT message.
old-location: multimedia\capsetaudioformat.htm
tech.root: Multimedia
ms.assetid: 9f14b76c-3b12-4dfb-937d-e8a173e077bd
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: "_win32_capSetAudioFormat, capSetAudioFormat, capSetAudioFormat macro [Windows Multimedia], multimedia.capsetaudioformat, vfw/capSetAudioFormat"
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
 - capSetAudioFormat
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# capSetAudioFormat macro


## -description



The <b>capSetAudioFormat</b> macro sets the audio format to use when performing streaming or step capture. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/8bffa401-3d36-43bb-9f69-988ebc69b860">WM_CAP_SET_AUDIOFORMAT</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


### -param s

Pointer to a <a href="https://msdn.microsoft.com/bd0f96ec-d26a-4e6f-8802-50e8ff207f54">WAVEFORMATEX</a> or <a href="https://msdn.microsoft.com/c09dc3f0-e1bc-4643-9b27-bcf1dcc5710c">PCMWAVEFORMAT</a> structure that defines the audio format. 


### -param wSize

Size, in bytes, of the structure referenced by <i>psAudioFormat</i>. 


## -see-also




<a href="https://msdn.microsoft.com/c09dc3f0-e1bc-4643-9b27-bcf1dcc5710c">PCMWAVEFORMAT</a>



<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>



<a href="https://msdn.microsoft.com/bd0f96ec-d26a-4e6f-8802-50e8ff207f54">WAVEFORMATEX</a>



<a href="https://msdn.microsoft.com/8bffa401-3d36-43bb-9f69-988ebc69b860">WM_CAP_SET_AUDIOFORMAT</a>
 

 

