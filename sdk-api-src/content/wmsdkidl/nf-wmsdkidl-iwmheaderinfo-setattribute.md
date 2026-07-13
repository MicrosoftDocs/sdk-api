---
UID: NF:wmsdkidl.IWMHeaderInfo.SetAttribute
title: IWMHeaderInfo::SetAttribute (wmsdkidl.h)
description: The SetAttribute method sets a descriptive attribute that is stored in the header section of the ASF file. This method is replaced by IWMHeaderInfo3::AddAttribute, and should not be used.
helpviewer_keywords: ["IWMHeaderInfo interface [windows Media Format]","SetAttribute method","IWMHeaderInfo.SetAttribute","IWMHeaderInfo2 interface [windows Media Format]","SetAttribute method","IWMHeaderInfo2::SetAttribute","IWMHeaderInfo3 interface [windows Media Format]","SetAttribute method","IWMHeaderInfo3::SetAttribute","IWMHeaderInfo::SetAttribute","IWMHeaderInfoSetAttribute","SetAttribute","SetAttribute method [windows Media Format]","SetAttribute method [windows Media Format]","IWMHeaderInfo interface","SetAttribute method [windows Media Format]","IWMHeaderInfo2 interface","SetAttribute method [windows Media Format]","IWMHeaderInfo3 interface","wmformat.iwmheaderinfo_setattribute","wmsdkidl/IWMHeaderInfo2::SetAttribute","wmsdkidl/IWMHeaderInfo3::SetAttribute","wmsdkidl/IWMHeaderInfo::SetAttribute"]
old-location: wmformat\iwmheaderinfo_setattribute.htm
tech.root: wmformat
ms.assetid: 174969a2-4fe2-477b-9990-051d23bf8a29
ms.date: 4/26/2023
ms.keywords: IWMHeaderInfo interface [windows Media Format],SetAttribute method, IWMHeaderInfo.SetAttribute, IWMHeaderInfo2 interface [windows Media Format],SetAttribute method, IWMHeaderInfo2::SetAttribute, IWMHeaderInfo3 interface [windows Media Format],SetAttribute method, IWMHeaderInfo3::SetAttribute, IWMHeaderInfo::SetAttribute, IWMHeaderInfoSetAttribute, SetAttribute, SetAttribute method [windows Media Format], SetAttribute method [windows Media Format],IWMHeaderInfo interface, SetAttribute method [windows Media Format],IWMHeaderInfo2 interface, SetAttribute method [windows Media Format],IWMHeaderInfo3 interface, wmformat.iwmheaderinfo_setattribute, wmsdkidl/IWMHeaderInfo2::SetAttribute, wmsdkidl/IWMHeaderInfo3::SetAttribute, wmsdkidl/IWMHeaderInfo::SetAttribute
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
 - IWMHeaderInfo::SetAttribute
 - wmsdkidl/IWMHeaderInfo::SetAttribute
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
 - IWMHeaderInfo.SetAttribute
 - IWMHeaderInfo2.SetAttribute
 - IWMHeaderInfo3.SetAttribute
---

# IWMHeaderInfo::SetAttribute


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>SetAttribute</b> method sets a descriptive attribute that is stored in the header section of the ASF file. This method is replaced by <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute">IWMHeaderInfo3::AddAttribute</a>, and should not be used.

## -parameters

### -param wStreamNum [in]

<b>WORD</b> containing the stream number. To set a file-level attribute, pass zero.

### -param pszName [in]

Pointer to a wide-character null-terminated string containing the name of the attribute. Attribute names are limited to 1024 wide characters.

### -param Type [in]

A value from the <b>WMT_ATTR_DATATYPE</b> enumeration type.

### -param pValue [in]

Pointer to a byte array containing the value of the attribute.

### -param cbLength [in]

The size of <i>pValue</i>, in bytes.

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
A parameter does not contain a valid value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Not implemented.

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
<dt><b>NS_E_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
The object is not in a configurable state, or no profile has been set.

</td>
</tr>
</table>

## -remarks

Refer to the <a href="/windows/desktop/wmformat/attributes">Attributes</a> section for a list of predefined attributes. For predefined attributes, the <i>Type</i> parameter must match the data type defined for that attribute. For custom attributes, you can specify any type except WMT_TYPE_GUID, but the buffer size (given by <i>cbLength</i>) must match the type. See <a href="/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_attr_datatype">WMT_ATTR_DATATYPE</a> for more information.

The <b>IWMHeaderInfo</b> interface does not support the WMT_TYPE_GUID data type. To use this data type, you must use the methods of the <b>IWMHeaderInfo3</b> interface.

Attributes in MP3 files cannot be specific to a particular stream. For MP3 files, always set the stream number to zero. When setting attributes for MP3 files, the metadata editor will automatically insert a byte-order mark in accordance with the Unicode specification. If you manually insert a byte-order mark, this method will not fail, but the value will then have two marks, which can cause problems when reading the attribute.

This method does not support attributes with values larger than 64 kilobytes. To include large attributes in your file, use the methods of the <b>IWMHeaderInfo3</b> interface.

The writer object supports this method only before the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting">IWMWriter::BeginWriting</a> method has been called. The reader and synchronous reader objects do not support this method.

Before you can use this method through the <b>IWMHeaderInfo</b> interface of a writer object to set <a href="/windows/desktop/wmformat/wmformat-glossary">DRM</a> attributes, you must set a profile for the writer to use.

The objects of the Windows Media Format SDK perform type checking on some supported metadata attributes, but not all of them. You should ensure that any attributes you use are set using the data type specified in the <a href="/windows/desktop/wmformat/attributes">Attributes</a> section of this documentation. Likewise, you cannot assume that an attribute set by another application will use the correct data type.

## -see-also

<a href="/windows/desktop/wmformat/attributes">Attributes</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo">IWMHeaderInfo Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2">IWMHeaderInfo2</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3">IWMHeaderInfo3 Interface</a>



<a href="/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyindex">IWMHeaderInfo::GetAttributeByIndex</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname">IWMHeaderInfo::GetAttributeByName</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributecount">IWMHeaderInfo::GetAttributeCount</a>



<a href="/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_attr_datatype">WMT_ATTR_DATATYPE</a>