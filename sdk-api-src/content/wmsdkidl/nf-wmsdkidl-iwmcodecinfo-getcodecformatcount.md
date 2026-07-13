---
UID: NF:wmsdkidl.IWMCodecInfo.GetCodecFormatCount
title: IWMCodecInfo::GetCodecFormatCount (wmsdkidl.h)
description: The GetCodecFormatCount method retrieves the number of formats supported by the specified codec. Each codec format is a stream configuration that is valid for use with the codec.
helpviewer_keywords: ["GetCodecFormatCount","GetCodecFormatCount method [windows Media Format]","GetCodecFormatCount method [windows Media Format]","IWMCodecInfo interface","IWMCodecInfo interface [windows Media Format]","GetCodecFormatCount method","IWMCodecInfo.GetCodecFormatCount","IWMCodecInfo::GetCodecFormatCount","IWMCodecInfoGetCodecFormatCount","wmformat.iwmcodecinfo_getcodecformatcount","wmsdkidl/IWMCodecInfo::GetCodecFormatCount"]
old-location: wmformat\iwmcodecinfo_getcodecformatcount.htm
tech.root: wmformat
ms.assetid: b93bfb01-4179-4a0b-bca0-92b1a9a8e605
ms.date: 4/26/2023
ms.keywords: GetCodecFormatCount, GetCodecFormatCount method [windows Media Format], GetCodecFormatCount method [windows Media Format],IWMCodecInfo interface, IWMCodecInfo interface [windows Media Format],GetCodecFormatCount method, IWMCodecInfo.GetCodecFormatCount, IWMCodecInfo::GetCodecFormatCount, IWMCodecInfoGetCodecFormatCount, wmformat.iwmcodecinfo_getcodecformatcount, wmsdkidl/IWMCodecInfo::GetCodecFormatCount
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
 - IWMCodecInfo::GetCodecFormatCount
 - wmsdkidl/IWMCodecInfo::GetCodecFormatCount
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
 - IWMCodecInfo.GetCodecFormatCount
---

# IWMCodecInfo::GetCodecFormatCount


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetCodecFormatCount</b> method retrieves the number of formats supported by the specified codec. Each codec format is a stream configuration that is valid for use with the codec.

## -parameters

### -param guidType [in]

<b>GUID</b> identifying the major type of digital media. This must be one of the following constants.

<table>
<tr>
<th>Constant
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>WMMEDIATYPE_Video</td>
<td>Specifies a video codec.</td>
</tr>
<tr>
<td>WMMEDIATYPE_Audio</td>
<td>Specifies an audio codec.</td>
</tr>
</table>

### -param dwCodecIndex [in]

<b>DWORD</b> containing the codec index ranging from zero to one less than the number of supported codecs of the type specified by <i>guidType</i>. To retrieve the number of individual codecs supporting a major media type, use the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmcodecinfo-getcodecinfocount">IWMCodecInfo::GetCodecInfoCount</a> method.

### -param pcFormat [out]

Pointer to a count of the formats supported by the codec.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>pcFormat</i> has been passed a null value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Other unspecified failure.

</td>
</tr>
</table>

## -remarks

Use this method along with <b>GetCodecFormat</b> to enumerate the formats supported by the codec.

The Windows Media Format SDK provides codecs only for audio and video. If you specify another major type, this method will return an error.

You do not need to call this method for the Windows Media Video codecs; each video codec supports only a single format. For more information see <a href="/windows/desktop/wmformat/configuring-video-streams">Configuring Video Streams</a>.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo">IWMCodecInfo Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmcodecinfo-getcodecformat">IWMCodecInfo::GetCodecFormat</a>