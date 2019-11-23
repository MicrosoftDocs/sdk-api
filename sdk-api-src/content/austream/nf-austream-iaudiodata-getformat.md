---
UID: NF:austream.IAudioData.GetFormat
title: IAudioData::GetFormat (austream.h)

description: Note  This interface is deprecated. New applications should not use it. The GetFormat method retrieves the current data format.
old-location: dshow\iaudiodata_getformat.htm
tech.root: DirectShow
ms.assetid: 7b06592d-2b9d-4f5a-bf74-331b07a13f0f

ms.date: 12/05/2018
ms.keywords: GetFormat, GetFormat method [DirectShow], GetFormat method [DirectShow],IAudioData interface, IAudioData interface [DirectShow],GetFormat method, IAudioData.GetFormat, IAudioData::GetFormat, IAudioDataGetFormat, austream/IAudioData::GetFormat, dshow.iaudiodata_getformat
ms.topic: method
f1_keywords: 
 - "austream/IAudioData.GetFormat"
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
 - IAudioData.GetFormat
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAudioData::GetFormat


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>GetFormat</code> method retrieves the current data format.




## -parameters




### -param pWaveFormatCurrent [out]

Pointer to a <a href="https://docs.microsoft.com/previous-versions/dd757713(v=vs.85)">WAVEFORMATEX</a> structure that contains the current data format.


## -returns



Returns S_OK if successful or E_POINTER if pointer is invalid.




## -remarks



Currently, Microsoft DirectShow supports only PCM wave data.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/austream/nn-austream-iaudiodata">IAudioData Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/austream/nf-austream-iaudiodata-setformat">IAudioData::SetFormat</a>
 

 

