---
UID: NF:wmsdkidl.IWMCodecInfo3.GetCodecFormatProp
title: IWMCodecInfo3::GetCodecFormatProp (wmsdkidl.h)
description: The GetCodecFormatProp method retrieves a property from one format of a codec.
helpviewer_keywords: ["GetCodecFormatProp","GetCodecFormatProp method [windows Media Format]","GetCodecFormatProp method [windows Media Format]","IWMCodecInfo3 interface","IWMCodecInfo3 interface [windows Media Format]","GetCodecFormatProp method","IWMCodecInfo3.GetCodecFormatProp","IWMCodecInfo3::GetCodecFormatProp","IWMCodecInfo3GetCodecFormatProp","wmformat.iwmcodecinfo3_getcodecformatprop","wmsdkidl/IWMCodecInfo3::GetCodecFormatProp"]
old-location: wmformat\iwmcodecinfo3_getcodecformatprop.htm
tech.root: wmformat
ms.assetid: 04f5301f-0033-4cf3-bc05-3159fe274a8d
ms.date: 4/26/2023
ms.keywords: GetCodecFormatProp, GetCodecFormatProp method [windows Media Format], GetCodecFormatProp method [windows Media Format],IWMCodecInfo3 interface, IWMCodecInfo3 interface [windows Media Format],GetCodecFormatProp method, IWMCodecInfo3.GetCodecFormatProp, IWMCodecInfo3::GetCodecFormatProp, IWMCodecInfo3GetCodecFormatProp, wmformat.iwmcodecinfo3_getcodecformatprop, wmsdkidl/IWMCodecInfo3::GetCodecFormatProp
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
 - IWMCodecInfo3::GetCodecFormatProp
 - wmsdkidl/IWMCodecInfo3::GetCodecFormatProp
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
 - IWMCodecInfo3.GetCodecFormatProp
---

# IWMCodecInfo3::GetCodecFormatProp


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetCodecFormatProp</b> method retrieves a property from one format of a codec.

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

### -param pszName [in]

Pointer to a wide-character <b>null</b>-terminated string containing the name of the property to retrieve.

Currently only one codec format property is supported; it is listed in the following table. The format property determines the data type and value of the property; this information is included in the table.

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
<td>g_wszSpeechCaps</td>
<td><b>WMT_TYPE_DWORD</b></td>
<td>The value is one from the <a href="/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_musicspeech_class_mode">WMT_MUSICSPEECH_CLASS_MODE</a> enumeration type indicating the supported mode of the format. This property applies only to the Windows Media Audio 9 Voice codec.</td>
</tr>
</table>

### -param pType [out]

Pointer to a variable that will receive a member of the <b>WMT_ATTR_DATATYPE</b> enumeration type. This value specifies the type of information returned to the buffer pointed to by <i>pValue</i>.

### -param pValue [out]

Pointer to a buffer that will receive the value of the property. The data returned is of a type specified by <i>pType</i>.

### -param pdwSize [in, out]

Pointer to a <b>DWORD</b> value specifying the length of the buffer pointed to by <i>pValue</i>.

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

You should make two calls to <b>GetCodecFormatProp</b> for each property you want to retrieve. On the first call, pass <b>NULL</b> as <i>pValue</i>. On return, the value of <i>pdwSize</i> will be set to the buffer size required to hold the value of the specified property. Then you can allocate the required amount of memory for the buffer and pass a pointer to it as <i>pValue</i> on the second call.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3">IWMCodecInfo3 Interface</a>