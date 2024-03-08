---
UID: NF:wmsdkidl.IWMCodecInfo2.GetCodecFormatDesc
title: IWMCodecInfo2::GetCodecFormatDesc (wmsdkidl.h)
description: The GetCodecFormatDesc method retrieves a description of a specified codec format. This method also retrieves a stream configuration object containing the settings for the codec format.
helpviewer_keywords: ["GetCodecFormatDesc","GetCodecFormatDesc method [windows Media Format]","GetCodecFormatDesc method [windows Media Format]","IWMCodecInfo2 interface","IWMCodecInfo2 interface [windows Media Format]","GetCodecFormatDesc method","IWMCodecInfo2.GetCodecFormatDesc","IWMCodecInfo2::GetCodecFormatDesc","IWMCodecInfo2GetCodecFormatDesc","wmformat.iwmcodecinfo2_getcodecformatdesc","wmsdkidl/IWMCodecInfo2::GetCodecFormatDesc"]
old-location: wmformat\iwmcodecinfo2_getcodecformatdesc.htm
tech.root: wmformat
ms.assetid: 24ca091e-72f6-4c7b-b25a-8957d70fa450
ms.date: 4/26/2023
ms.keywords: GetCodecFormatDesc, GetCodecFormatDesc method [windows Media Format], GetCodecFormatDesc method [windows Media Format],IWMCodecInfo2 interface, IWMCodecInfo2 interface [windows Media Format],GetCodecFormatDesc method, IWMCodecInfo2.GetCodecFormatDesc, IWMCodecInfo2::GetCodecFormatDesc, IWMCodecInfo2GetCodecFormatDesc, wmformat.iwmcodecinfo2_getcodecformatdesc, wmsdkidl/IWMCodecInfo2::GetCodecFormatDesc
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
 - IWMCodecInfo2::GetCodecFormatDesc
 - wmsdkidl/IWMCodecInfo2::GetCodecFormatDesc
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
 - IWMCodecInfo2.GetCodecFormatDesc
---

# IWMCodecInfo2::GetCodecFormatDesc


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetCodecFormatDesc</b> method retrieves a description of a specified codec format. This method also retrieves a stream configuration object containing the settings for the codec format.

## -parameters

### -param guidType [in]

GUID identifying the major type of digital media. This must be one of the following constants.

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

<b>DWORD</b> containing the codec index ranging from zero to one less than the number of supported codecs of the type specified by <i>guidType</i>. To retrieve the number of individual codecs supporting a major type, use the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmcodecinfo-getcodecinfocount">IWMCodecInfo::GetCodecInfoCount</a> method.

### -param dwFormatIndex [in]

<b>DWORD</b> containing the format index ranging from zero to one less than the number of supported formats. To retrieve the number of individual formats supported by a codec, use the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmcodecinfo-getcodecformatcount">IWMCodecInfo::GetCodecFormatCount</a> method.

### -param ppIStreamConfig [out]

Pointer to a pointer to the <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig">IWMStreamConfig</a> interface of a stream configuration object containing the settings of the specified format. When calling <b>GetCodecFormatDesc</b> to retrieve the size of the description string, pass <b>NULL</b> for this parameter.

### -param wszDesc [out]

Pointer to a wide-character <b>null</b>-terminated string containing the codec format description.

### -param pcchDesc [in, out]

On input, a pointer to the length of the <i>wszDesc</i> buffer. On output, a pointer to the length of the codec format description string, including the terminating <b>null</b> character.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
An invalid or <b>null</b> value has been passed in.

</td>
</tr>
</table>

## -remarks

You should make two calls to <b>GetCodecFormatDesc</b>. On the first call, pass <b>NULL</b> as <i>wszDesc</i>. On return, the value pointed to by <i>pcchDesc</i> will be set to the number of wide characters required to hold the description, including the terminating <b>null</b> character. Then you can allocate a buffer of the appropriate size and pass a pointer to it as <i>wszDesc</i> on the second call.

Some formats of the Windows Media Audio 9 codec and Windows Media Audio 9 Professional codec have very similar descriptions. For example both "64 kbps, 44 kHz, stereo CBR" and "64 kbps, 44 kHz, stereo (A/V) CBR" are listed. In these cases, the format with "(A/V)" in its description is designed for use in files that also contain one or more video streams. The other format is for files that contain only audio.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo2">IWMCodecInfo2 Interface</a>