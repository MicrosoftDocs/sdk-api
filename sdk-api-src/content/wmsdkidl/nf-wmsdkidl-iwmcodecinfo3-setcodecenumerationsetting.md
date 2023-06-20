---
UID: NF:wmsdkidl.IWMCodecInfo3.SetCodecEnumerationSetting
title: IWMCodecInfo3::SetCodecEnumerationSetting (wmsdkidl.h)
description: The SetCodecEnumerationSetting method sets the value of one codec enumeration setting. Codec enumeration settings dictate the codec formats that can be enumerated by the methods of IWMCodecInfo.
helpviewer_keywords: ["IWMCodecInfo3 interface [windows Media Format]","SetCodecEnumerationSetting method","IWMCodecInfo3.SetCodecEnumerationSetting","IWMCodecInfo3::SetCodecEnumerationSetting","IWMCodecInfo3SetCodecEnumerationSetting","SetCodecEnumerationSetting","SetCodecEnumerationSetting method [windows Media Format]","SetCodecEnumerationSetting method [windows Media Format]","IWMCodecInfo3 interface","wmformat.iwmcodecinfo3_setcodecenumerationsetting","wmsdkidl/IWMCodecInfo3::SetCodecEnumerationSetting"]
old-location: wmformat\iwmcodecinfo3_setcodecenumerationsetting.htm
tech.root: wmformat
ms.assetid: 5b4883b8-63c0-40ff-b13f-303d30ebfe15
ms.date: 4/26/2023
ms.keywords: IWMCodecInfo3 interface [windows Media Format],SetCodecEnumerationSetting method, IWMCodecInfo3.SetCodecEnumerationSetting, IWMCodecInfo3::SetCodecEnumerationSetting, IWMCodecInfo3SetCodecEnumerationSetting, SetCodecEnumerationSetting, SetCodecEnumerationSetting method [windows Media Format], SetCodecEnumerationSetting method [windows Media Format],IWMCodecInfo3 interface, wmformat.iwmcodecinfo3_setcodecenumerationsetting, wmsdkidl/IWMCodecInfo3::SetCodecEnumerationSetting
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
 - IWMCodecInfo3::SetCodecEnumerationSetting
 - wmsdkidl/IWMCodecInfo3::SetCodecEnumerationSetting
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
 - IWMCodecInfo3.SetCodecEnumerationSetting
---

# IWMCodecInfo3::SetCodecEnumerationSetting


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>SetCodecEnumerationSetting</b> method sets the value of one codec enumeration setting. Codec enumeration settings dictate the codec formats that can be enumerated by the methods of <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo">IWMCodecInfo</a>.

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

Pointer to a wide-character null-terminated string containing the name of the enumeration setting. Use one of the following constants.

<table>
<tr>
<th>Constant
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>g_wszVBREnabled</td>
<td>Use to enumerate the supported codec formats that use variable bit rate (VBR) encoding.The value returned in <i>pValue</i> is a <b>BOOL</b>.

</td>
</tr>
<tr>
<td>g_wszNumPasses</td>
<td>Use to enumerate the supported codec formats that use a number of passes equal to the value in <i>pValue</i>.The value returned in <i>pValue</i> is a <b>DWORD</b> specifying the number of passes.

</td>
</tr>
</table>

### -param Type [in]

A <a href="/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_attr_datatype">WMT_ATTR_DATATYPE</a> value specifying the data type of the value in <i>pValue</i>.

### -param pValue [in]

A pointer to a <b>BYTE</b> array containing the setting value.

### -param dwSize [in]

<b>DWORD</b> containing the size of the <i>pValue</i> <b>BYTE</b> array.

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
The method succeeded; the feature is supported by the codec.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_UNSUPPORTED_PROPERTY</b></dt>
</dl>
</td>
<td width="60%">
The enumeration setting specified is not valid for the codec.

</td>
</tr>
</table>

## -remarks

The Windows Media Audio and Video 9 Series codecs can potentially enumerate four different sets of codec formats, as listed in the following table.

<table>
<tr>
<th></th>
<th>Constant bit rate (CBR) stream
            </th>
<th>Two-pass CBR stream
            </th>
<th>Quality-based variable bit rate (VBR) stream
            </th>
<th>Bit-rate-based VBR stream (constrained or unconstrained)
            </th>
</tr>
<tr>
<td>g_wszVBREnabled</td>
<td>FALSE</td>
<td>FALSE</td>
<td>TRUE</td>
<td>TRUE</td>
</tr>
<tr>
<td>g_wszNumPasses</td>
<td>1</td>
<td>2</td>
<td>1</td>
<td>2</td>
</tr>
</table>
 

Not all codecs support all formats.

If you make a call to this method and get the NS_E_UNSUPPORTED_PROPERTY error code, then the codec does not support that feature. For example, if an attempt to set g_wszNumPasses returns NS_E_UNSUPPORTED_PROPERTY, the codec does not support multiple encoding passes.

The return value of a call made to this method does not guarantee support of a codec feature. For example, the Windows Media Audio 9 Lossless codec does not return NS_E_UNSUPPORTED_PROPERTY for calls that set the number of passes, even though the codec does not support two-pass encoding.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-getcodecenumerationsetting">GetCodecEnumerationSetting</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3">IWMCodecInfo3 Interface</a>