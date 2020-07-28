---
UID: NF:austream.IAudioMediaStream.CreateSample
title: IAudioMediaStream::CreateSample (austream.h)
description: Note  This interface is deprecated. New applications should not use it. Creates an audio stream sample for use with the specified stream.
helpviewer_keywords: ["CreateSample","CreateSample method [DirectShow]","CreateSample method [DirectShow]","IAudioMediaStream interface","IAudioMediaStream interface [DirectShow]","CreateSample method","IAudioMediaStream.CreateSample","IAudioMediaStream::CreateSample","IAudioMediaStreamCreateSample","austream/IAudioMediaStream::CreateSample","dshow.iaudiomediastream_createsample"]
old-location: dshow\iaudiomediastream_createsample.htm
tech.root: dshow
ms.assetid: c7d62a2c-54a9-4690-8ba0-34e927f9f093
ms.date: 12/05/2018
ms.keywords: CreateSample, CreateSample method [DirectShow], CreateSample method [DirectShow],IAudioMediaStream interface, IAudioMediaStream interface [DirectShow],CreateSample method, IAudioMediaStream.CreateSample, IAudioMediaStream::CreateSample, IAudioMediaStreamCreateSample, austream/IAudioMediaStream::CreateSample, dshow.iaudiomediastream_createsample
f1_keywords:
- austream/IAudioMediaStream.CreateSample
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
- IAudioMediaStream.CreateSample
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAudioMediaStream::CreateSample


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
Creates an audio stream sample for use with the specified stream.




## -parameters




### -param pAudioData [in]

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/austream/nn-austream-iaudiodata">IAudioData</a> container. <b>IAudioData</b> objects can be referenced by samples in more than one stream.


### -param dwFlags [in]

Reserved for flag data. Must be zero.


### -param ppSample [out]

Address of a pointer to the new <a href="https://docs.microsoft.com/windows/desktop/api/austream/nn-austream-iaudiostreamsample">IAudioStreamSample</a> interface.


## -returns



Returns S_OK if successful or E_POINTER if one or more of the required parameters are <b>NULL</b>.




## -remarks



The <i>pAudioData</i> object defines the data's format.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/austream/nn-austream-iaudiomediastream">IAudioMediaStream Interface</a>
 

 

