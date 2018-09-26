---
UID: NF:austream.IAudioMediaStream.GetFormat
title: IAudioMediaStream::GetFormat
author: windows-sdk-content
description: Note  This interface is deprecated. New applications should not use it. Retrieves the stream data's current format.
old-location: dshow\iaudiomediastream_getformat.htm
tech.root: DirectShow
ms.assetid: df582b90-f537-42cf-a83e-109a20446d8a
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: GetFormat, GetFormat method [DirectShow], GetFormat method [DirectShow],IAudioMediaStream interface, IAudioMediaStream interface [DirectShow],GetFormat method, IAudioMediaStream.GetFormat, IAudioMediaStream::GetFormat, IAudioMediaStreamGetFormat, austream/IAudioMediaStream::GetFormat, dshow.iaudiomediastream_getformat
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: austream.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - COM
api_location:
 - austream.h
api_name:
 - IAudioMediaStream.GetFormat
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAudioMediaStream::GetFormat


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
Retrieves the stream data's current format.




## -parameters




### -param pWaveFormatCurrent [out]

Pointer to a <a href="https://msdn.microsoft.com/4f3bf6fb-b15f-43b3-82f1-e7a8a3007057">WAVEFORMATEX</a> structure that contains the stream data's current format.


## -returns



Returns S_OK if successful or E_POINTER if the required parameter is <b>NULL</b>.




## -remarks



Currently, Microsoft DirectShow supports only PCM wave data.




## -see-also




<a href="https://msdn.microsoft.com/b4098876-6c11-4cc6-8b6d-16edc02316f3">IAudioMediaStream Interface</a>
 

 

