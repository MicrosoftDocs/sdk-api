---
UID: NF:austream.IAudioMediaStream.SetFormat
title: IAudioMediaStream::SetFormat (austream.h)
author: windows-sdk-content
description: Note  This interface is deprecated. New applications should not use it. Sets the format for the stream.
old-location: dshow\iaudiomediastream_setformat.htm
tech.root: DirectShow
ms.assetid: 5925f373-c862-4215-9877-5bb4d5411d36
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAudioMediaStream interface [DirectShow],SetFormat method, IAudioMediaStream.SetFormat, IAudioMediaStream::SetFormat, IAudioMediaStreamSetFormat, SetFormat, SetFormat method [DirectShow], SetFormat method [DirectShow],IAudioMediaStream interface, austream/IAudioMediaStream::SetFormat, dshow.iaudiomediastream_setformat
ms.topic: method
f1_keywords: ["austream/IAudioMediaStream.SetFormat"]
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
 - IAudioMediaStream.SetFormat
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAudioMediaStream::SetFormat


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
Sets the format for the stream.




## -parameters




### -param lpWaveFormat [in]

Pointer to a <a href="https://docs.microsoft.com/previous-versions/dd757713(v=vs.85)">WAVEFORMATEX</a> structure that contains stream format information.


## -returns



Returns an <b>HRESULT</b> value, which can include the following values or others not listed.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MS_E_INCOMPATIBLE</b></dt>
</dl>
</td>
<td width="60%">
Format of the <a href="https://docs.microsoft.com/windows/desktop/api/austream/nn-austream-iaudiodata">IAudioData</a> object is not compatible with stream.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/austream/nn-austream-iaudiomediastream">IAudioMediaStream Interface</a>
 

 

