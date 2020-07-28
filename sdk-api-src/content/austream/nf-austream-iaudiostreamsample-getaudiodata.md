---
UID: NF:austream.IAudioStreamSample.GetAudioData
title: IAudioStreamSample::GetAudioData (austream.h)
description: Note  This interface is deprecated. New applications should not use it. Retrieves the address of a pointer to the IAudioData object associated with the sample.
helpviewer_keywords: ["GetAudioData","GetAudioData method [DirectShow]","GetAudioData method [DirectShow]","IAudioStreamSample interface","IAudioStreamSample interface [DirectShow]","GetAudioData method","IAudioStreamSample.GetAudioData","IAudioStreamSample::GetAudioData","IAudioStreamSampleGetAudioData","austream/IAudioStreamSample::GetAudioData","dshow.iaudiostreamsample_getaudiodata"]
old-location: dshow\iaudiostreamsample_getaudiodata.htm
tech.root: dshow
ms.assetid: b482e628-d4bc-461e-b529-58e891689513
ms.date: 12/05/2018
ms.keywords: GetAudioData, GetAudioData method [DirectShow], GetAudioData method [DirectShow],IAudioStreamSample interface, IAudioStreamSample interface [DirectShow],GetAudioData method, IAudioStreamSample.GetAudioData, IAudioStreamSample::GetAudioData, IAudioStreamSampleGetAudioData, austream/IAudioStreamSample::GetAudioData, dshow.iaudiostreamsample_getaudiodata
f1_keywords:
- austream/IAudioStreamSample.GetAudioData
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
- IAudioStreamSample.GetAudioData
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAudioStreamSample::GetAudioData


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
Retrieves the address of a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/austream/nn-austream-iaudiodata">IAudioData</a> object associated with the sample.




## -parameters




### -param ppAudio [out]

Address of a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/austream/nn-austream-iaudiodata">IAudioData</a> object.


## -returns



Returns S_OK if successful or E_POINTER if the parameter is <b>NULL</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/austream/nn-austream-iaudiostreamsample">IAudioStreamSample Interface</a>
 

 

