---
UID: NF:wmsdkidl.IWMHeaderInfo3.GetAttributeByIndexEx
title: IWMHeaderInfo3::GetAttributeByIndexEx (wmsdkidl.h)
description: The GetAttributeByIndexEx method retrieves the value of an attribute specified by the attribute index.
helpviewer_keywords: ["GetAttributeByIndexEx","GetAttributeByIndexEx method [windows Media Format]","GetAttributeByIndexEx method [windows Media Format]","IWMHeaderInfo3 interface","IWMHeaderInfo3 interface [windows Media Format]","GetAttributeByIndexEx method","IWMHeaderInfo3.GetAttributeByIndexEx","IWMHeaderInfo3::GetAttributeByIndexEx","IWMHeaderInfo3GetAttributeByIndexEx","wmformat.iwmheaderinfo3_getattributebyindexex","wmsdkidl/IWMHeaderInfo3::GetAttributeByIndexEx"]
old-location: wmformat\iwmheaderinfo3_getattributebyindexex.htm
tech.root: wmformat
ms.assetid: c20f4c79-f5b3-45d9-ad70-5fb9745bbf1b
ms.date: 4/26/2023
ms.keywords: GetAttributeByIndexEx, GetAttributeByIndexEx method [windows Media Format], GetAttributeByIndexEx method [windows Media Format],IWMHeaderInfo3 interface, IWMHeaderInfo3 interface [windows Media Format],GetAttributeByIndexEx method, IWMHeaderInfo3.GetAttributeByIndexEx, IWMHeaderInfo3::GetAttributeByIndexEx, IWMHeaderInfo3GetAttributeByIndexEx, wmformat.iwmheaderinfo3_getattributebyindexex, wmsdkidl/IWMHeaderInfo3::GetAttributeByIndexEx
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
 - IWMHeaderInfo3::GetAttributeByIndexEx
 - wmsdkidl/IWMHeaderInfo3::GetAttributeByIndexEx
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
 - IWMHeaderInfo3.GetAttributeByIndexEx
---

# IWMHeaderInfo3::GetAttributeByIndexEx


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetAttributeByIndexEx</b> method retrieves the value of an attribute specified by the attribute index. You can use this method in conjunction with the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributecountex">GetAttributeCountEx</a> method to retrieve all of the attributes associated with a particular stream number.

## -parameters

### -param wStreamNum [in]

<b>WORD</b> containing the stream number to which the attribute applies. Set to zero to retrieve a file-level attribute.

### -param wIndex [in]

<b>WORD</b> containing the index of the attribute to be retrieved.

### -param pwszName [out]

Pointer to a wide-character <b>null</b>-terminated string containing the attribute name. Pass <b>NULL</b> to retrieve the size of the string, which will be returned in <i>pwNameLen</i>.

### -param pwNameLen [in, out]

Pointer to a <b>WORD</b> containing the size of <i>pwszName</i>, in wide characters. This size includes the terminating <b>null</b> character. Attribute names are limited to 1024 wide characters.

### -param pType [out]

Type of data used for the attribute. For more information about the types of data supported, see <a href="/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_attr_datatype">WMT_ATTR_DATATYPE</a>.

### -param pwLangIndex [out]

Pointer to a <b>WORD</b> containing the language index of the language associated with the attribute. This is the index of the language in the language list for the file.

### -param pValue [out]

Pointer to an array of bytes containing the attribute value. Pass <b>NULL</b> to retrieve the size of the attribute value, which will be returned in <i>pdwDataLength</i>.

### -param pdwDataLength [in, out]

Pointer to a <b>DWORD</b> containing the length, in bytes, of the attribute value pointed to by <i>pValue</i>.

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
<dt><b>NS_E_SDK_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">
The size specified for the name or value is too small.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALID_REQUEST</b></dt>
</dl>
</td>
<td width="60%">
<i>wStreamNum</i> is not a valid stream number, or there is no attribute at <i>wIndex</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A pointer is not valid.

</td>
</tr>
</table>

## -remarks

You can use 0xFFFF for the stream number to specify an attribute using its global index. Global index values range from 0 to one less than the count of attributes received from a call to <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributecountex">IWMHeaderInfo3::GetAttributeCountEx</a> where the stream number was set to 0xFFFF.

The objects of the Windows Media Format SDK perform type checking on some supported metadata attributes, but not all of them. You should ensure that any attributes you use are set using the data type specified in the <a href="/windows/desktop/wmformat/attributes">Attributes</a> section of this documentation. Likewise, you cannot assume that an attribute set by another application will use the correct data type.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3">IWMHeaderInfo3 Interface</a>