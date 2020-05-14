---
UID: NF:vfw.capGetAudioFormat
title: capGetAudioFormat macro (vfw.h)
description: The capGetAudioFormat macro obtains the audio format. You can use this macro or explicitly call the WM_CAP_GET_AUDIOFORMAT message.helpviewer_keywords: ["_win32_capGetAudioFormat","capGetAudioFormat","capGetAudioFormat macro [Windows Multimedia]","multimedia.capgetaudioformat","vfw/capGetAudioFormat"]
old-location: multimedia\capgetaudioformat.htm
tech.root: Multimedia
ms.assetid: 11a91da3-dd22-4828-9845-dc29e73c4526
ms.date: 12/05/2018
ms.keywords: _win32_capGetAudioFormat, capGetAudioFormat, capGetAudioFormat macro [Windows Multimedia], multimedia.capgetaudioformat, vfw/capGetAudioFormat
f1_keywords:
- vfw/capGetAudioFormat
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
- capGetAudioFormat
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# capGetAudioFormat macro


## -description



The <b>capGetAudioFormat</b> macro obtains the audio format. You can use this macro or explicitly call the <a href="https://docs.microsoft.com/windows/desktop/Multimedia/wm-cap-get-audioformat">WM_CAP_GET_AUDIOFORMAT</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


### -param s

Pointer to a <a href="https://docs.microsoft.com/previous-versions/dd757713(v=vs.85)">WAVEFORMATEX</a> structure, or <b>NULL</b>. If the value is <b>NULL</b>, the size, in bytes, required to hold the <b>WAVEFORMATEX</b> structure is returned. 


### -param wSize

Size, in bytes, of the structure referenced by <i>s</i>. 


## -remarks



Because compressed audio formats vary in size requirements applications must first retrieve the size, then allocate memory, and finally request the audio format data.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-capture-macros">Video Capture Macros</a>
 

 

