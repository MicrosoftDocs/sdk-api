---
UID: NF:austream.IAudioData.GetFormat
title: IAudioData::GetFormat method
author: windows-driver-content
description: Note  This interface is deprecated. New applications should not use it. The GetFormat method retrieves the current data format.
old-location: dshow\iaudiodata_getformat.htm
old-project: DirectShow
ms.assetid: 7b06592d-2b9d-4f5a-bf74-331b07a13f0f
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetFormat method [DirectShow], GetFormat method [DirectShow], IAudioData interface, GetFormat,IAudioData.GetFormat, IAudioData, IAudioData interface [DirectShow], GetFormat method, IAudioData::GetFormat, IAudioDataGetFormat, austream/IAudioData::GetFormat, dshow.iaudiodata_getformat
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
req.typenames: AUDIO_STREAM_CATEGORY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	austream.h
api_name:
-	IAudioData.GetFormat
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAudioData::GetFormat method


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>GetFormat</code> method retrieves the current data format.




## -parameters




### -param pWaveFormatCurrent [out]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff538799">WAVEFORMATEX</a> structure that contains the current data format.


## -returns



Returns S_OK if successful or E_POINTER if pointer is invalid.




## -remarks



Currently, Microsoft DirectShow supports only PCM wave data.




## -see-also




<a href="https://msdn.microsoft.com/8b253715-a294-4e95-b730-e6efe7f895af">IAudioData Interface</a>



<a href="https://msdn.microsoft.com/792112a6-b10a-432f-854a-07bd74173e84">IAudioData::SetFormat</a>
 

 

