---
UID: NF:austream.IAudioStreamSample.GetAudioData
title: IAudioStreamSample::GetAudioData
author: windows-sdk-content
description: Note  This interface is deprecated. New applications should not use it. Retrieves the address of a pointer to the IAudioData object associated with the sample.
old-location: dshow\iaudiostreamsample_getaudiodata.htm
tech.root: DirectShow
ms.assetid: b482e628-d4bc-461e-b529-58e891689513
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetAudioData, GetAudioData method [DirectShow], GetAudioData method [DirectShow],IAudioStreamSample interface, IAudioStreamSample interface [DirectShow],GetAudioData method, IAudioStreamSample.GetAudioData, IAudioStreamSample::GetAudioData, IAudioStreamSampleGetAudioData, austream/IAudioStreamSample::GetAudioData, dshow.iaudiostreamsample_getaudiodata
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
 - IAudioStreamSample.GetAudioData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAudioStreamSample::GetAudioData


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
Retrieves the address of a pointer to the <a href="https://msdn.microsoft.com/en-us/library/Dd389513(v=VS.85).aspx">IAudioData</a> object associated with the sample.




## -parameters




### -param ppAudio [out]

Address of a pointer to the <a href="https://msdn.microsoft.com/en-us/library/Dd389513(v=VS.85).aspx">IAudioData</a> object.


## -returns



Returns S_OK if successful or E_POINTER if the parameter is <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd389520(v=VS.85).aspx">IAudioStreamSample Interface</a>
 

 

