---
UID: NF:mfreadwrite.IMFSourceReaderEx.GetTransformForStream
title: IMFSourceReaderEx::GetTransformForStream
author: windows-sdk-content
description: Gets a pointer to a Media Foundation transform (MFT) for a specified stream.
old-location: mf\imfsourcereaderex_gettransformforstream.htm
tech.root: medfound
ms.assetid: 39F2D132-5D2B-4389-AB30-FE2942EC3965
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: GetTransformForStream, GetTransformForStream method [Media Foundation], GetTransformForStream method [Media Foundation],IMFSourceReaderEx interface, IMFSourceReaderEx interface [Media Foundation],GetTransformForStream method, IMFSourceReaderEx.GetTransformForStream, IMFSourceReaderEx::GetTransformForStream, MF_SOURCE_READER_FIRST_AUDIO_STREAM, MF_SOURCE_READER_FIRST_VIDEO_STREAM, mf.imfsourcereaderex_gettransformforstream, mfreadwrite/IMFSourceReaderEx::GetTransformForStream
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfreadwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - IMFSourceReaderEx.GetTransformForStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFSourceReaderEx::GetTransformForStream


## -description


Gets a pointer to a Media Foundation transform (MFT) for a specified stream.


## -parameters




### -param dwStreamIndex [in]

The stream to query for the MFT. The value can be any of the following.

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
</table>
 


### -param dwTransformIndex [in]

The zero-based index of the MFT to retreive.


### -param pGuidCategory [out]

Receives a GUID that specifies the category of the MFT. For a list of possible values, see <a href="https://msdn.microsoft.com/eca3ae3b-e40a-407d-986c-d0a85b891f52">MFT_CATEGORY</a>.


### -param ppTransform [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/3cc502d8-d364-43b9-b0b6-d9474c002b20">IMFTransform</a> interface of the MFT. The caller must release the interface.


## -returns



This method can return one of these values.

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
<dt><b>MF_E_INVALIDINDEX</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwTransformIndex</i> parameter is out of range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>MF_E_INVALIDSTREAMNUMBER</b></b></dt>
</dl>
</td>
<td width="60%">
The <i>dwStreamIndex</i> parameter is invalid.

</td>
</tr>
</table>
 




## -remarks



You can use this method to configure an MFT after it is inserted into the processing chain. Do not use the pointer returned in <i>ppTransform</i> to set media types on the MFT or to process data. In particular, calling any of the following <a href="https://msdn.microsoft.com/3cc502d8-d364-43b9-b0b6-d9474c002b20">IMFTransform</a> methods could have unexpected results.

<ul>
<li>
<a href="https://msdn.microsoft.com/311ab66e-5dbd-452a-bad4-99a6293cbc60">AddInputStreams</a>
</li>
<li>
<a href="https://msdn.microsoft.com/cba37f7f-6ab2-469c-95c2-61d9e4d31d0b">DeleteInputStream</a>
</li>
<li>
<a href="https://msdn.microsoft.com/28366df3-c414-45ff-bb15-c5483f11de85">ProcessEvent</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c94d406b-7cd9-42d4-ae9e-3d21dbb47209">ProcessInput</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a6dc67e5-8473-444a-8463-24f411e59565">ProcessMessage</a>
</li>
<li>
<a href="https://msdn.microsoft.com/dc58cc75-7e01-4f47-a572-8e3ca1bc43b4">ProcessOutput</a>
</li>
<li>
<a href="https://msdn.microsoft.com/822a83d1-177a-4a8d-842e-eb76f8253283">SetInputType</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a9a1d03f-2e56-490c-885b-78c69dea8e92">SetOutputType</a>
</li>
</ul>
If a decoder is present, it appears at index position zero.

To avoid losing any data, you should drain the source reader before calling this method. For more information, see <a href="https://msdn.microsoft.com/en-us/library/Dd389281(v=VS.85).aspx">Draining the Data Pipeline</a>.




## -see-also




<a href="https://msdn.microsoft.com/59888F9B-C464-4045-AA77-03EE16E2B598">IMFSourceReaderEx</a>
 

 

