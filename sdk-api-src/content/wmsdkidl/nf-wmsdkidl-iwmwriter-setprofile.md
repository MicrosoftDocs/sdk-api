---
UID: NF:wmsdkidl.IWMWriter.SetProfile
title: IWMWriter::SetProfile
author: windows-sdk-content
description: The SetProfile method specifies the profile to use for the current writing task.
old-location: wmformat\iwmwriter_setprofile.htm
old-project: wmformat
ms.assetid: 1a931896-c102-4b3b-a5a3-b3ef85b276b9
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IWMWriter interface [windows Media Format],SetProfile method, IWMWriter.SetProfile, IWMWriter::SetProfile, IWMWriterSetProfile, SetProfile, SetProfile method [windows Media Format], SetProfile method [windows Media Format],IWMWriter interface, wmformat.iwmwriter_setprofile, wmsdkidl/IWMWriter::SetProfile
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: WM_AETYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmvcore.lib
 - Wmvcore.dll
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - IWMWriter.SetProfile
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMWriter::SetProfile


## -description



The <b>SetProfile</b> method specifies the profile to use for the current writing task.




## -parameters




### -param pProfile [in]

Pointer to an <a href="https://msdn.microsoft.com/00f28d6b-d27d-4268-960e-c8ea25e5359e">IWMProfile</a> interface.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ASF_E_STREAMNUMBERINUSE</b></dt>
</dl>
</td>
<td width="60%">
More than one stream in the profile has the same stream number.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALIDPROFILE</b></dt>
</dl>
</td>
<td width="60%">
The profile has zero streams.

The bit rate was specified as zero for a CBR-encoding mode.

More than one script stream was specified.

The bandwidth-sharing information is incorrect or inconsistent.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
The writer is not in a configurable state.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALID_STREAM</b></dt>
</dl>
</td>
<td width="60%">
For any stream:

<ul>
<li>A buffer window greater than 100,000 was specified.</li>
<li>A stream number was specified as less than one or greater than 63.</li>
</ul>
For audio streams:

<ul>
<li>The <b>formattype</b> is not <b>WMFORMAT_WaveFormatEx</b>.</li>
<li>The <b>wformatTag</b> is not WAVE_FORMAT_PCM and <b>nAvgBytesPerSec</b> is zero.</li>
<li>The FOURCC derived from the subtype <b>GUID</b> does not match the <b>dwFormatTag</b>.</li>
<li>For PCM audio, <b>nAvgBytesPerSec</b> is not equal to (<b>nSamplesPerSec</b> * <b>nBlockAlign</b>).</li>
<li>For PCM audio, <b>nBlockAlign</b> is not equal to (<b>nChannels</b> * <b>wBitsPerSample</b> / 8).</li>
</ul>
For video streams:

<ul>
<li>The <b>formattype</b> is not <b>WMFORMAT_VideoInfo</b>.</li>
<li><b>cbFormat</b> is not equal to sizeof(<b>WMVIDEOINFOHEADER</b>).</li>
<li>The bit rate specified through <b>IWMStreamConfig</b> is not equal to the value of <b>dwBitrate</b> in the <b>VIDEOINFOHEADER</b>. (Does not apply if <a href="https://msdn.microsoft.com/202be688-e739-4e80-9574-f85b2eb168fc">IWMStreamConfig::SetBitrate</a> was used to set a bit rate of zero.)</li>
<li>On uncompressed video streams, <b>bmiHeader.biSizeImage</b> has been specified incorrectly.</li>
<li>The rectangle width or height specified in the <b>bmiHeader</b> is not valid for the compression type. (Some types require two- or four-byte alignment.)</li>
<li>Any member of the <b>rcSource</b> or <b>rcTarget</b> rectangles is negative.</li>
<li>The FOURCC derived from the subtype <b>GUID</b> does not match <b>bmiHeader.biCompression</b>.</li>
<li>The <b>bmiHeader.biCompression</b> member is BI_BITFIELDS, but <b>cbFormat</b> is incorrect.</li>
<li>When <b>bmiHeader.biCompression</b> = BI_RGB or BI_BITFIELDS, the <b>biBitCount</b>, <b>biClrUsed</b>, or <b>cbFormat</b> values are inconsistent or invalid. (Remember that the size of the format block is larger if the <b>BITMAPINFOHEADER</b> contains an index of palette values.)</li>
</ul>
For script streams:

<ul>
<li>The <b>formattype</b> is not specified as <b>WMFORMAT_Script</b>.</li>
<li>The subtype is not specified as <b>GUID_NULL</b>.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_SDK_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">
The size specified for a language string in an audio stream is too small.

</td>
</tr>
</table>
 




## -remarks



Calling this method removes any previously set header attribute information.

Changes to the profile object made after this method is called do not take effect until <b>SetProfile</b> is called again.

The maximum number of streams in a profile is 63, as defined by the constant WM_MAX_STREAMS. Another constant, WM_MAX_VIDEO_STREAMS, defines the maximum number of video streams, which is also 63.




## -see-also




<a href="https://msdn.microsoft.com/1e9392b4-4fff-41ad-9d80-23c1c7f9e9a4">Attributes</a>



<a href="https://msdn.microsoft.com/00f28d6b-d27d-4268-960e-c8ea25e5359e">IWMProfile Interface</a>



<a href="https://msdn.microsoft.com/a194ef11-5203-4e85-af91-cdce0c53fe76">IWMWriter Interface</a>



<a href="https://msdn.microsoft.com/743212fd-a1e7-47c5-a220-c203cc2788e6">IWMWriter::SetProfileByID</a>



<a href="https://msdn.microsoft.com/8805bc57-5f19-4544-bcb8-5af880ba8ea0">To Use Profiles with the Writer</a>
 

 

