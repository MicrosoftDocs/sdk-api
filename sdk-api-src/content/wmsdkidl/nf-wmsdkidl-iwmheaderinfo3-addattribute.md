---
UID: NF:wmsdkidl.IWMHeaderInfo3.AddAttribute
title: IWMHeaderInfo3::AddAttribute (wmsdkidl.h)
description: The AddAttribute method adds a metadata attribute. To change the value of an existing attribute, use the IWMHeaderInfo3::ModifyAttribute method.
helpviewer_keywords: ["AddAttribute","AddAttribute method [windows Media Format]","AddAttribute method [windows Media Format]","IWMHeaderInfo3 interface","IWMHeaderInfo3 interface [windows Media Format]","AddAttribute method","IWMHeaderInfo3.AddAttribute","IWMHeaderInfo3::AddAttribute","IWMHeaderInfo3AddAttribute","wmformat.iwmheaderinfo3_addattribute","wmsdkidl/IWMHeaderInfo3::AddAttribute"]
old-location: wmformat\iwmheaderinfo3_addattribute.htm
tech.root: wmformat
ms.assetid: 15ecb34d-f70d-43a3-b369-2d9c2532945e
ms.date: 4/26/2023
ms.keywords: AddAttribute, AddAttribute method [windows Media Format], AddAttribute method [windows Media Format],IWMHeaderInfo3 interface, IWMHeaderInfo3 interface [windows Media Format],AddAttribute method, IWMHeaderInfo3.AddAttribute, IWMHeaderInfo3::AddAttribute, IWMHeaderInfo3AddAttribute, wmformat.iwmheaderinfo3_addattribute, wmsdkidl/IWMHeaderInfo3::AddAttribute
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
 - IWMHeaderInfo3::AddAttribute
 - wmsdkidl/IWMHeaderInfo3::AddAttribute
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
 - IWMHeaderInfo3.AddAttribute
---

# IWMHeaderInfo3::AddAttribute


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>AddAttribute</b> method adds a metadata attribute. To change the value of an existing attribute, use the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-modifyattribute">IWMHeaderInfo3::ModifyAttribute</a> method.

## -parameters

### -param wStreamNum [in]

<b>WORD</b> containing the stream number of the stream to which the attribute applies. Setting this value to zero indicates an attribute that applies to the entire file.

### -param pszName [in]

Pointer to a wide-character null-terminated string containing the name of the attribute. Attribute names are limited to 1024 wide characters.

### -param pwIndex [out]

Pointer to a <b>WORD</b>. On successful completion of the method, this value is set to the index assigned to the new attribute.

### -param Type [in]

Type of data used for the new attribute. For more information about the types of data supported, see <a href="/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_attr_datatype">WMT_ATTR_DATATYPE</a>.

### -param wLangIndex [in]

<b>WORD</b> containing the language index of the language to be associated with the new attribute. This is the index of the language in the language list for the file. Setting this value to zero indicates that the default language will be used. A default language is created and set according to the regional settings on the computer running your application.

### -param pValue [in]

Pointer to an array of bytes containing the attribute value.

### -param dwLength [in]

<b>DWORD</b> containing the length of the attribute value, in bytes.

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
An illegal parameter combination, data type, or attribute name was used.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The method is not implemented on a reader object.

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
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_SDK_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">
The size specified by <i>dwLength</i> is too small.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALID_REQUEST</b></dt>
</dl>
</td>
<td width="60%">
<i>wStreamNum</i> is not a valid stream number.

</td>
</tr>
</table>

## -remarks

This method appends a null character to the end of the string passed in <i>pwszName</i> if one is not present. In this case, the buffer needed to retrieve the attribute name will be two bytes larger than the input buffer.

When setting attributes for MP3 files, the metadata editor automatically inserts a byte-order mark in accordance with the Unicode specification. If you manually insert a byte-order mark, this method will not fail, but the value will then have two marks, which can cause problems when reading the attribute.

The objects of the Windows Media Format SDK perform type checking on some supported metadata attributes, but not all of them. You should ensure that any attributes you use are set using the data type specified in the <a href="/windows/desktop/wmformat/attributes">Attributes</a> section of this documentation. Likewise, you cannot assume that an attribute set by another application will use the correct data type.

<div class="alert"><b>Note</b>  Be careful to use the correct type representations of values. For example, when setting WM/MediaClassPrimaryID or WM/MediaClassSecondaryID attributes the values need to be represented as GUIDs converted to a byte array instead of strings converted to a byte array.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3">IWMHeaderInfo3 Interface</a>