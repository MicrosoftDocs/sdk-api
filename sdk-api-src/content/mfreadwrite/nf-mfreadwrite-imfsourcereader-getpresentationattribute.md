---
UID: NF:mfreadwrite.IMFSourceReader.GetPresentationAttribute
title: IMFSourceReader::GetPresentationAttribute
author: windows-sdk-content
description: Gets an attribute from the underlying media source.
old-location: mf\imfsourcereader_getpresentationattribute.htm
tech.root: medfound
ms.assetid: 40544e1e-cce2-4860-aeb2-b60696b09145
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: GetPresentationAttribute, GetPresentationAttribute method [Media Foundation], GetPresentationAttribute method [Media Foundation],IMFSourceReader interface, IMFSourceReader interface [Media Foundation],GetPresentationAttribute method, IMFSourceReader.GetPresentationAttribute, IMFSourceReader::GetPresentationAttribute, MF_SOURCE_READER_FIRST_AUDIO_STREAM, MF_SOURCE_READER_FIRST_VIDEO_STREAM, MF_SOURCE_READER_MEDIASOURCE, mf.imfsourcereader_getpresentationattribute, mfreadwrite/IMFSourceReader::GetPresentationAttribute
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfreadwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista and Platform Update Supplement for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - mfreadwrite.h
api_name:
 - IMFSourceReader.GetPresentationAttribute
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mfreadwrite.h
: 
- IMFSourceReader.GetPresentationAttribute
: 
---

# IMFSourceReader::GetPresentationAttribute


## -description


Gets an attribute from the underlying media source.


## -parameters




### -param dwStreamIndex [in]

The stream or object to query. The value can be any of the following.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0–0xFFFFFFFB</dt>
</dl>
</td>
<td width="60%">
The zero-based index of a stream.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_SOURCE_READER_FIRST_VIDEO_STREAM"></a><a id="mf_source_reader_first_video_stream"></a><dl>
<dt><b><b>MF_SOURCE_READER_FIRST_VIDEO_STREAM</b></b></dt>
<dt>0xFFFFFFFC</dt>
</dl>
</td>
<td width="60%">
The first video stream.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_SOURCE_READER_FIRST_AUDIO_STREAM"></a><a id="mf_source_reader_first_audio_stream"></a><dl>
<dt><b><b>MF_SOURCE_READER_FIRST_AUDIO_STREAM</b></b></dt>
<dt>0xFFFFFFFD</dt>
</dl>
</td>
<td width="60%">
The first audio stream.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_SOURCE_READER_MEDIASOURCE"></a><a id="mf_source_reader_mediasource"></a><dl>
<dt><b><b>MF_SOURCE_READER_MEDIASOURCE</b></b></dt>
<dt>0xFFFFFFFF</dt>
</dl>
</td>
<td width="60%">
The media source.


</td>
</tr>
</table>
 


### -param guidAttribute [in]

A GUID that identifies the attribute to retrieve. If the <i>dwStreamIndex</i> parameter equals  <b>MF_SOURCE_READER_MEDIASOURCE</b>, <i>guidAttribute</i> can specify one of the following:

<ul>
<li>A presentation descriptor attribute. For a list of values, see <a href="https://msdn.microsoft.com/2a092a6a-956b-4c1f-955f-529ec08665fe">Presentation Descriptor Attributes</a>.</li>
<li>
<a href="https://msdn.microsoft.com/4cd48b69-6f7b-4b13-86f3-b38969025f70">MF_SOURCE_READER_MEDIASOURCE_CHARACTERISTICS</a>. Use this value to get characteristics flags from the media source.</li>
</ul>
Otherwise, if the <i>dwStreamIndex</i> parameter specifies a stream, <i>guidAttribute</i> specifies a stream descriptor attribute. For a list of values, see <a href="https://msdn.microsoft.com/1364d7c5-67e8-49b6-8038-d6d4ea03fb7d">Stream Descriptor Attributes</a>.


### -param pvarAttribute [out]

A pointer to a <b>PROPVARIANT</b> that receives the value of the attribute. Call the <b>PropVariantClear</b> function to free the <b>PROPVARIANT</b>. 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This interface is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.




## -see-also




<a href="https://msdn.microsoft.com/7d3cc314-6b9e-437c-afda-ee1965a12721">IMFSourceReader</a>



<a href="https://msdn.microsoft.com/445fc879-3c9e-409d-8d05-ecd1ff9afc19">Media Foundation Attributes</a>



<a href="https://msdn.microsoft.com/8a17a754-53ef-4c05-9189-7978d864b17a">Source Reader</a>
 

 

