---
UID: NF:wmsdkidl.IWMCodecInfo3.GetCodecEnumerationSetting
title: IWMCodecInfo3::GetCodecEnumerationSetting (wmsdkidl.h)
description: The GetCodecEnumerationSetting method retrieves the current value for one codec enumeration setting.
helpviewer_keywords: ["GetCodecEnumerationSetting","GetCodecEnumerationSetting method [windows Media Format]","GetCodecEnumerationSetting method [windows Media Format]","IWMCodecInfo3 interface","IWMCodecInfo3 interface [windows Media Format]","GetCodecEnumerationSetting method","IWMCodecInfo3.GetCodecEnumerationSetting","IWMCodecInfo3::GetCodecEnumerationSetting","IWMCodecInfo3GetCodecEnumerationSetting","wmformat.iwmcodecinfo3_getcodecenumerationsetting","wmsdkidl/IWMCodecInfo3::GetCodecEnumerationSetting"]
old-location: wmformat\iwmcodecinfo3_getcodecenumerationsetting.htm
tech.root: wmformat
ms.assetid: 9a8f34ef-4d52-47d4-b6d5-e6f07f27cc8d
ms.date: 4/26/2023
ms.keywords: GetCodecEnumerationSetting, GetCodecEnumerationSetting method [windows Media Format], GetCodecEnumerationSetting method [windows Media Format],IWMCodecInfo3 interface, IWMCodecInfo3 interface [windows Media Format],GetCodecEnumerationSetting method, IWMCodecInfo3.GetCodecEnumerationSetting, IWMCodecInfo3::GetCodecEnumerationSetting, IWMCodecInfo3GetCodecEnumerationSetting, wmformat.iwmcodecinfo3_getcodecenumerationsetting, wmsdkidl/IWMCodecInfo3::GetCodecEnumerationSetting
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
 - IWMCodecInfo3::GetCodecEnumerationSetting
 - wmsdkidl/IWMCodecInfo3::GetCodecEnumerationSetting
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
 - IWMCodecInfo3.GetCodecEnumerationSetting
---

# IWMCodecInfo3::GetCodecEnumerationSetting


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetCodecEnumerationSetting</b> method retrieves the current value for one codec enumeration setting. Codec enumeration settings dictate the codec formats that can be enumerated by the methods of <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo">IWMCodecInfo</a>. You can change codec enumeration settings in order to retrieve codec formats supporting specific features by calling <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-setcodecenumerationsetting">IWMCodecInfo3::SetCodecEnumerationSetting</a>.

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

Pointer to a wide-character <b>null</b>-terminated string containing the name of the enumeration setting. Use one of the following constants.

<table>
<tr>
<th>Constant
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>g_wszVBREnabled</td>
<td>Use to enumerate the supported codec formats that use variable bit rate (VBR) encoding.The value returned in <i>pValue</i> is a <b></b>BOOL.

</td>
</tr>
<tr>
<td>g_wszNumPasses</td>
<td>Use to enumerate the supported codec formats that use a number of passes equal to the value in <i>pValue</i>.The value returned in <i>pValue</i> is a <b>DWORD</b> specifying the number of passes.

</td>
</tr>
</table>

### -param pType [out]

Pointer to a <a href="/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_attr_datatype">WMT_ATTR_DATATYPE</a> enumeration value specifying the data type of the value returned in <i>pValue</i>.

### -param pValue [out]

Pointer to a <b>BYTE</b> array containing the codec enumeration data. The data type and meaning of the data returned in this array depends on the setting specified by <i>pszName</i>. You can set this value to <b>NULL</b> to retrieve the required size of the array in <i>pdwSize</i>.

### -param pdwSize [in, out]

Pointer to a <b>DWORD</b> containing the size of the setting value in bytes. If you set <i>pValue</i> to <b>NULL</b>, this value will be set to the size required to hold the setting value.

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
<dt><b>NS_E_UNSUPPORTED_PROPERTY</b></dt>
</dl>
</td>
<td width="60%">
The enumeration setting specified is not valid for the codec.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3">IWMCodecInfo3 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-setcodecenumerationsetting">SetCodecEnumerationSetting</a>