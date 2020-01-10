---
UID: NF:austream.IAudioMediaStream.GetFormat
title: IAudioMediaStream::GetFormat (austream.h)
description: Note  This interface is deprecated. New applications should not use it. Retrieves the stream data's current format.
old-location: dshow\iaudiomediastream_getformat.htm
tech.root: DirectShow
ms.assetid: df582b90-f537-42cf-a83e-109a20446d8a
ms.date: 12/05/2018
ms.keywords: GetFormat, GetFormat method [DirectShow], GetFormat method [DirectShow],IAudioMediaStream interface, IAudioMediaStream interface [DirectShow],GetFormat method, IAudioMediaStream.GetFormat, IAudioMediaStream::GetFormat, IAudioMediaStreamGetFormat, austream/IAudioMediaStream::GetFormat, dshow.iaudiomediastream_getformat
f1_keywords:
- austream/IAudioMediaStream.GetFormat
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAudioMediaStream::GetFormat


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
Retrieves the stream data's current format.




## -parameters




### -param pWaveFormatCurrent [out]

Pointer to a <a href="https://docs.microsoft.com/previous-versions/dd757713(v=vs.85)">WAVEFORMATEX</a> structure that contains the stream data's current format.


## -returns



Returns S_OK if successful or E_POINTER if the required parameter is <b>NULL</b>.




## -remarks



Currently, Microsoft DirectShow supports only PCM wave data.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/austream/nn-austream-iaudiomediastream">IAudioMediaStream Interface</a>
 

 

