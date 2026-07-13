---
UID: NF:wmsdkidl.IWMCodecInfo.GetCodecInfoCount
title: IWMCodecInfo::GetCodecInfoCount (wmsdkidl.h)
description: The GetCodecInfoCount method retrieves the number of supported codecs for a specified major type of digital media (audio or video).
helpviewer_keywords: ["GetCodecInfoCount","GetCodecInfoCount method [windows Media Format]","GetCodecInfoCount method [windows Media Format]","IWMCodecInfo interface","IWMCodecInfo interface [windows Media Format]","GetCodecInfoCount method","IWMCodecInfo.GetCodecInfoCount","IWMCodecInfo::GetCodecInfoCount","IWMCodecInfoGetCodecInfoCount","wmformat.iwmcodecinfo_getcodecinfocount","wmsdkidl/IWMCodecInfo::GetCodecInfoCount"]
old-location: wmformat\iwmcodecinfo_getcodecinfocount.htm
tech.root: wmformat
ms.assetid: 873f8d03-5d7b-424c-91f3-e7c8156565be
ms.date: 4/26/2023
ms.keywords: GetCodecInfoCount, GetCodecInfoCount method [windows Media Format], GetCodecInfoCount method [windows Media Format],IWMCodecInfo interface, IWMCodecInfo interface [windows Media Format],GetCodecInfoCount method, IWMCodecInfo.GetCodecInfoCount, IWMCodecInfo::GetCodecInfoCount, IWMCodecInfoGetCodecInfoCount, wmformat.iwmcodecinfo_getcodecinfocount, wmsdkidl/IWMCodecInfo::GetCodecInfoCount
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
 - IWMCodecInfo::GetCodecInfoCount
 - wmsdkidl/IWMCodecInfo::GetCodecInfoCount
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
 - IWMCodecInfo.GetCodecInfoCount
---

# IWMCodecInfo::GetCodecInfoCount


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetCodecInfoCount</b> method retrieves the number of supported codecs for a specified major type of digital media (audio or video).

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

### -param pcCodecs [out]

Pointer to a count of supported codecs.

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
<i>pcCodecs</i> has been passed a null value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>guidType</i> is not a type for which codecs are used.

</td>
</tr>
</table>

## -remarks

Use this method along with <b>GetCodecFormatCount</b> and <b>GetCodecFormat</b> to enumerate through the supported codecs for each media type, and the supported formats for each codec.

The Windows Media Format SDK provides codecs only for audio and video. If you specify another major type, this method will return an error.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo">IWMCodecInfo Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmcodecinfo-getcodecformat">IWMCodecInfo::GetCodecFormat</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmcodecinfo-getcodecformatcount">IWMCodecInfo::GetCodecFormatCount</a>