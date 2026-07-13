---
UID: NF:wmsdkidl.IWMCodecInfo3.GetCodecProp
title: IWMCodecInfo3::GetCodecProp (wmsdkidl.h)
description: The GetCodecProp method retrieves a codec property.
helpviewer_keywords: ["GetCodecProp","GetCodecProp method [windows Media Format]","GetCodecProp method [windows Media Format]","IWMCodecInfo3 interface","IWMCodecInfo3 interface [windows Media Format]","GetCodecProp method","IWMCodecInfo3.GetCodecProp","IWMCodecInfo3::GetCodecProp","IWMCodecInfo3GetCodecProp","wmformat.iwmcodecinfo3_getcodecprop","wmsdkidl/IWMCodecInfo3::GetCodecProp"]
old-location: wmformat\iwmcodecinfo3_getcodecprop.htm
tech.root: wmformat
ms.assetid: 444f5789-c5e5-4eeb-a2b4-11f959641206
ms.date: 4/26/2023
ms.keywords: GetCodecProp, GetCodecProp method [windows Media Format], GetCodecProp method [windows Media Format],IWMCodecInfo3 interface, IWMCodecInfo3 interface [windows Media Format],GetCodecProp method, IWMCodecInfo3.GetCodecProp, IWMCodecInfo3::GetCodecProp, IWMCodecInfo3GetCodecProp, wmformat.iwmcodecinfo3_getcodecprop, wmsdkidl/IWMCodecInfo3::GetCodecProp
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
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
 - IWMCodecInfo3::GetCodecProp
 - wmsdkidl/IWMCodecInfo3::GetCodecProp
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
 - IWMCodecInfo3.GetCodecProp
---

# IWMCodecInfo3::GetCodecProp


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetCodecProp</b> method retrieves a codec property.

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

### -param pszName [in]

Pointer to a <b>null</b>-terminated string containing the name of the property to retrieve.

The following table lists the codec properties you can retrieve. The property dictates the data type and value; this information is also included in the table.

<table>
<tr>
<th>Global constant
                </th>
<th>Data type
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>g_wszComplexityMax</td>
<td><b>WMT_TYPE_DWORD</b></td>
<td>The value is the maximum complexity value for the codec. Codec complexity applies only to video codecs. The range of complexity values is from 0 to this value.</td>
</tr>
<tr>
<td>g_wszComplexityOffline</td>
<td><b>WMT_TYPE_DWORD</b></td>
<td>The value is the suggested complexity value for the codec when encoding files for local playback. Codec complexity applies only to video codecs. The range of complexity values is from 0 to the value retrieved with g_wszComplexityMax.</td>
</tr>
<tr>
<td>g_wszComplexityLive</td>
<td><b>WMT_TYPE_DWORD</b></td>
<td>The value is the suggested complexity value for the codec when encoding files for streaming playback. Codec complexity applies only to video codecs. The range of complexity values is from 0 to the value retrieved with g_wszComplexityMax.</td>
</tr>
<tr>
<td>g_wszIsVBRSupported</td>
<td><b>WMT_TYPE_BOOL</b></td>
<td>The value indicates whether the codec supports VBR.</td>
</tr>
</table>

### -param pType [out]

Pointer to a variable that will receive a member of the <b>WMT_ATTR_DATATYPE</b> enumeration type. This value specifies the type of information returned to the buffer at <i>pValue</i>.

### -param pValue [out]

Pointer to a buffer that will receive the value of the property. The data returned is of a type specified by <i>pType</i>.

### -param pdwSize [in, out]

Pointer to a <b>DWORD</b> value specifying the length of the buffer at <i>pValue</i>.

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
<i>pszName</i> or <i>pType</i> or <i>pdwSize</i> is <b>NULL</b>.

OR

<i>guidType</i> specifies an invalid input type.

OR

<i>pszName</i> specifies an invalid property name.

</td>
</tr>
</table>

## -remarks

You should make two calls to <b>GetCodecProp</b> for each property you want to retrieve. On the first call, pass <b>NULL</b> as <i>pValue</i>. On return, the value of <i>pdwSize</i> will be set to the buffer size required to hold the value of the specified property. Then you can allocate the required amount of memory for the buffer and pass a pointer to it as <i>pValue</i> on the second call.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3">IWMCodecInfo3 Interface</a>