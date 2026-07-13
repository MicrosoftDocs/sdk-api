---
UID: NF:wmsdkidl.IWMWriter.SetProfile
title: IWMWriter::SetProfile (wmsdkidl.h)
description: The SetProfile method specifies the profile to use for the current writing task.
helpviewer_keywords: ["IWMWriter interface [windows Media Format]","SetProfile method","IWMWriter.SetProfile","IWMWriter::SetProfile","IWMWriterSetProfile","SetProfile","SetProfile method [windows Media Format]","SetProfile method [windows Media Format]","IWMWriter interface","wmformat.iwmwriter_setprofile","wmsdkidl/IWMWriter::SetProfile"]
old-location: wmformat\iwmwriter_setprofile.htm
tech.root: wmformat
ms.assetid: 1a931896-c102-4b3b-a5a3-b3ef85b276b9
ms.date: 4/26/2023
ms.keywords: IWMWriter interface [windows Media Format],SetProfile method, IWMWriter.SetProfile, IWMWriter::SetProfile, IWMWriterSetProfile, SetProfile, SetProfile method [windows Media Format], SetProfile method [windows Media Format],IWMWriter interface, wmformat.iwmwriter_setprofile, wmsdkidl/IWMWriter::SetProfile
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
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMWriter::SetProfile
 - wmsdkidl/IWMWriter::SetProfile
dev_langs:
 - c++
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
---

# IWMWriter::SetProfile


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>SetProfile</b> method specifies the profile to use for the current writing task.

## -parameters

### -param pProfile [in]

Pointer to an <a href="/windows/desktop/wmformat/iwmprofile">IWMProfile</a> interface.

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
<li>The bit rate specified through <b>IWMStreamConfig</b> is not equal to the value of <b>dwBitrate</b> in the <b>VIDEOINFOHEADER</b>. (Does not apply if <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate">IWMStreamConfig::SetBitrate</a> was used to set a bit rate of zero.)</li>
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

<a href="/windows/desktop/wmformat/attributes">Attributes</a>



<a href="/windows/desktop/wmformat/iwmprofile">IWMProfile Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter">IWMWriter Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid">IWMWriter::SetProfileByID</a>



<a href="/windows/desktop/wmformat/to-use-profiles-with-the-writer">To Use Profiles with the Writer</a>