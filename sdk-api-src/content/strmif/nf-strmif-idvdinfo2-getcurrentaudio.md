---
UID: NF:strmif.IDvdInfo2.GetCurrentAudio
title: IDvdInfo2::GetCurrentAudio
author: windows-sdk-content
description: The GetCurrentAudio method retrieves the number of available audio streams and the number of the currently selected audio stream.
old-location: dshow\idvdinfo2_getcurrentaudio.htm
old-project: DirectShow
ms.assetid: 0f2ff79f-cefa-43e5-ab91-348a5341a171
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: GetCurrentAudio, GetCurrentAudio method [DirectShow], GetCurrentAudio method [DirectShow],IDvdInfo2 interface, IDvdInfo2 interface [DirectShow],GetCurrentAudio method, IDvdInfo2.GetCurrentAudio, IDvdInfo2::GetCurrentAudio, IDvdInfo2GetCurrentAudio, dshow.idvdinfo2_getcurrentaudio, strmif/IDvdInfo2::GetCurrentAudio
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IDvdInfo2.GetCurrentAudio
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IDvdInfo2::GetCurrentAudio


## -description



The <code>GetCurrentAudio</code> method retrieves the number of available audio streams and the number of the currently selected audio stream.




## -parameters




### -param pulStreamsAvailable [out]

Receives the number of available audio streams.


### -param pulCurrentStream [out]

Receives the currently selected audio stream number in the current title.


## -returns



Returns one of the following <b>HRESULT</b> values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
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
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Input arguments are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_INVALIDDOMAIN</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/3b2c01a2-d52c-4497-8fc9-d1113e8507e8">DVD Navigator</a> is not initialized or not in a valid domain.

</td>
</tr>
</table>
 




## -remarks



To get the available audio languages on the disc, call <code>GetCurrentAudio</code> and then call <a href="https://msdn.microsoft.com/c95afa36-879b-4fd5-bf92-0b9b93c708ef">GetAudioLanguage</a> for each stream, starting from zero through (<i>pulStreamsAvailable</i> - 1) to get the language content.




## -see-also




<a href="https://msdn.microsoft.com/6f41e0f1-e550-4ca6-9a80-ce4d498289e2">DVD Applications</a>



<a href="https://msdn.microsoft.com/ab626c6b-765a-4b2e-be96-f45260d1a078">EC_DVD_AUDIO_STREAM_CHANGE</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/da30d3dc-feec-4f54-b2db-a771ce404286">IDvdInfo2 Interface</a>
 

 

