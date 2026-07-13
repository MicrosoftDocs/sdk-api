---
UID: NF:wmsdkidl.IWMCodecInfo2.GetCodecName
title: IWMCodecInfo2::GetCodecName (wmsdkidl.h)
description: The GetCodecName method retrieves the name of a specified codec.
helpviewer_keywords: ["GetCodecName","GetCodecName method [windows Media Format]","GetCodecName method [windows Media Format]","IWMCodecInfo2 interface","IWMCodecInfo2 interface [windows Media Format]","GetCodecName method","IWMCodecInfo2.GetCodecName","IWMCodecInfo2::GetCodecName","IWMCodecInfo2GetCodecName","wmformat.iwmcodecinfo2_getcodecname","wmsdkidl/IWMCodecInfo2::GetCodecName"]
old-location: wmformat\iwmcodecinfo2_getcodecname.htm
tech.root: wmformat
ms.assetid: 4ec4e242-9726-4fac-8867-cb4b13c4cbdc
ms.date: 4/26/2023
ms.keywords: GetCodecName, GetCodecName method [windows Media Format], GetCodecName method [windows Media Format],IWMCodecInfo2 interface, IWMCodecInfo2 interface [windows Media Format],GetCodecName method, IWMCodecInfo2.GetCodecName, IWMCodecInfo2::GetCodecName, IWMCodecInfo2GetCodecName, wmformat.iwmcodecinfo2_getcodecname, wmsdkidl/IWMCodecInfo2::GetCodecName
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
 - IWMCodecInfo2::GetCodecName
 - wmsdkidl/IWMCodecInfo2::GetCodecName
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
 - IWMCodecInfo2.GetCodecName
---

# IWMCodecInfo2::GetCodecName


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetCodecName</b> method retrieves the name of a specified codec.

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

### -param wszName [out]

Pointer to a wide-character <b>null</b>-terminated string that receives the codec name.

### -param pcchName [in, out]

On input, pointer to a <b>DWORD</b> containing the size, in wide characters, of the buffer <i>wszName</i>. On output, pointer to a variable containing the number of characters in <i>wszName</i>, including the terminating <b>null</b> character.

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

You should make two calls to <b>GetCodecName</b>. On the first call, pass <b>NULL</b> as <i>wszName</i>. On return, the value at <i>pcchName</i> will be set to the buffer size required to hold the codec name, including the terminating character. Then you can allocate the required amount of memory for the buffer and pass a pointer to it as <i>wszName</i> on the second call.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo2">IWMCodecInfo2 Interface</a>