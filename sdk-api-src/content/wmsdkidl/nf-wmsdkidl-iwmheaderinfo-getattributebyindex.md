---
UID: NF:wmsdkidl.IWMHeaderInfo.GetAttributeByIndex
title: IWMHeaderInfo::GetAttributeByIndex (wmsdkidl.h)
description: The GetAttributeByIndex method returns a descriptive attribute that is stored in the header section of the ASF file. This method is replaced by IWMHeaderInfo3::GetAttributeByIndexEx and should not be used.
helpviewer_keywords: ["GetAttributeByIndex","GetAttributeByIndex method [windows Media Format]","GetAttributeByIndex method [windows Media Format]","IWMHeaderInfo interface","GetAttributeByIndex method [windows Media Format]","IWMHeaderInfo2 interface","GetAttributeByIndex method [windows Media Format]","IWMHeaderInfo3 interface","IWMHeaderInfo interface [windows Media Format]","GetAttributeByIndex method","IWMHeaderInfo.GetAttributeByIndex","IWMHeaderInfo2 interface [windows Media Format]","GetAttributeByIndex method","IWMHeaderInfo2::GetAttributeByIndex","IWMHeaderInfo3 interface [windows Media Format]","GetAttributeByIndex method","IWMHeaderInfo3::GetAttributeByIndex","IWMHeaderInfo::GetAttributeByIndex","IWMHeaderInfoGetAttributeByIndex","wmformat.iwmheaderinfo_getattributebyindex","wmsdkidl/IWMHeaderInfo2::GetAttributeByIndex","wmsdkidl/IWMHeaderInfo3::GetAttributeByIndex","wmsdkidl/IWMHeaderInfo::GetAttributeByIndex"]
old-location: wmformat\iwmheaderinfo_getattributebyindex.htm
tech.root: wmformat
ms.assetid: 905fdf2c-a398-457e-80e9-aac124301f99
ms.date: 4/26/2023
ms.keywords: GetAttributeByIndex, GetAttributeByIndex method [windows Media Format], GetAttributeByIndex method [windows Media Format],IWMHeaderInfo interface, GetAttributeByIndex method [windows Media Format],IWMHeaderInfo2 interface, GetAttributeByIndex method [windows Media Format],IWMHeaderInfo3 interface, IWMHeaderInfo interface [windows Media Format],GetAttributeByIndex method, IWMHeaderInfo.GetAttributeByIndex, IWMHeaderInfo2 interface [windows Media Format],GetAttributeByIndex method, IWMHeaderInfo2::GetAttributeByIndex, IWMHeaderInfo3 interface [windows Media Format],GetAttributeByIndex method, IWMHeaderInfo3::GetAttributeByIndex, IWMHeaderInfo::GetAttributeByIndex, IWMHeaderInfoGetAttributeByIndex, wmformat.iwmheaderinfo_getattributebyindex, wmsdkidl/IWMHeaderInfo2::GetAttributeByIndex, wmsdkidl/IWMHeaderInfo3::GetAttributeByIndex, wmsdkidl/IWMHeaderInfo::GetAttributeByIndex
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
 - IWMHeaderInfo::GetAttributeByIndex
 - wmsdkidl/IWMHeaderInfo::GetAttributeByIndex
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
 - qasf.dll
api_name:
 - IWMHeaderInfo.GetAttributeByIndex
 - IWMHeaderInfo2.GetAttributeByIndex
 - IWMHeaderInfo3.GetAttributeByIndex
---

# IWMHeaderInfo::GetAttributeByIndex


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetAttributeByIndex</b> method returns a descriptive attribute that is stored in the header section of the ASF file. This method is replaced by <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributebyindexex">IWMHeaderInfo3::GetAttributeByIndexEx</a> and should not be used.

## -parameters

### -param wIndex [in]

<b>WORD</b> containing the index.

### -param pwStreamNum [in]

Pointer to a <b>WORD</b> containing the stream number. Although this parameter is a pointer, the method will not change the value. For file-level attributes, use zero for the stream number.

### -param pwszName [out]

Pointer to a wide-character <b>null</b>-terminated string containing the name. Pass <b>NULL</b> to this parameter to retrieve the required length for the name. Attribute names are limited to 1024 wide characters.

### -param pcchNameLen [in, out]

On input, a pointer to a variable containing the length of the <i>pwszName</i> array in wide characters (2 bytes). On output, if the method succeeds, the variable contains the actual length of the name, including the terminating <b>null</b> character.

### -param pType [out]

Pointer to a variable containing one value from the <b>WMT_ATTR_DATATYPE</b> enumeration type.

### -param pValue [out]

Pointer to a byte array containing the value. Pass <b>NULL</b> to this parameter to retrieve the required length for the value.

### -param pcbLength [in, out]

On input, a pointer to a variable containing the length of the <i>pValue</i> array, in bytes. On output, if the method succeeds, the variable contains the actual number of bytes written to <i>pValue</i> by the method.

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
<dt><b>NS_E_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
The object is not in a valid state, or no profile has been set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pwStreamNum</i> does not point to a valid stream number, or no data type was supplied.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A pointer supplied in a parameter was not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The method failed for an unspecified reason.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ASF_E_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">
The <i>pValue</i> array is too small to contain the attribute value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ASF_E_NOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
There is no attribute at <i>wIndex</i>.

</td>
</tr>
</table>

## -remarks

You should make two calls to <b>GetAttributeByIndex</b> for each attribute you want to retrieve. On the first call, pass <b>NULL</b> for <i>pwszName</i> and <i>pValue</i>. On return, the value pointed to by <i>pcchNameLen</i> is set to the number of wide characters, including the terminating <b>null</b> character, required to hold the attribute name, and the value pointed to by <i>pcbLength</i> is set to the number of bytes required to hold the attribute value. You can then create buffers of the appropriate size to receive <i>pwszName</i> and <i>pValue</i> and pass pointers to them on the second call.

Attributes in MP3 files cannot be stream-specific. When using this method with MP3 files, you must use zero for the stream number.

For a list of all the predefined attributes, see <a href="/windows/desktop/wmformat/attributes">Attributes</a>.

The objects of the Windows Media Format SDK perform type checking on some supported metadata attributes, but not all of them. You should ensure that any attributes you use are set using the data type specified in the <a href="/windows/desktop/wmformat/attributes">Attributes</a> section of this documentation. Likewise, you cannot assume that an attribute set by another application will use the correct data type.

## -see-also

<a href="/windows/desktop/wmformat/attributes">Attributes</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo">IWMHeaderInfo Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2">IWMHeaderInfo2</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3">IWMHeaderInfo3</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute">IWMHeaderInfo::SetAttribute</a>



<a href="/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_attr_datatype">WMT_ATTR_DATATYPE</a>