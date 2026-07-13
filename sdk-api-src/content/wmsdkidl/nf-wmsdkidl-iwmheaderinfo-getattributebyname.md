---
UID: NF:wmsdkidl.IWMHeaderInfo.GetAttributeByName
title: IWMHeaderInfo::GetAttributeByName (wmsdkidl.h)
description: The GetAttributeByName method returns a descriptive attribute that is stored in the header section of the ASF file.
helpviewer_keywords: ["GetAttributeByName","GetAttributeByName method [windows Media Format]","GetAttributeByName method [windows Media Format]","IWMHeaderInfo interface","GetAttributeByName method [windows Media Format]","IWMHeaderInfo2 interface","GetAttributeByName method [windows Media Format]","IWMHeaderInfo3 interface","IWMHeaderInfo interface [windows Media Format]","GetAttributeByName method","IWMHeaderInfo.GetAttributeByName","IWMHeaderInfo2 interface [windows Media Format]","GetAttributeByName method","IWMHeaderInfo2::GetAttributeByName","IWMHeaderInfo3 interface [windows Media Format]","GetAttributeByName method","IWMHeaderInfo3::GetAttributeByName","IWMHeaderInfo::GetAttributeByName","IWMHeaderInfoGetAttributeByName","wmformat.iwmheaderinfo_getattributebyname","wmsdkidl/IWMHeaderInfo2::GetAttributeByName","wmsdkidl/IWMHeaderInfo3::GetAttributeByName","wmsdkidl/IWMHeaderInfo::GetAttributeByName"]
old-location: wmformat\iwmheaderinfo_getattributebyname.htm
tech.root: wmformat
ms.assetid: 8941b989-f052-4e61-a64a-06748947fcf4
ms.date: 4/26/2023
ms.keywords: GetAttributeByName, GetAttributeByName method [windows Media Format], GetAttributeByName method [windows Media Format],IWMHeaderInfo interface, GetAttributeByName method [windows Media Format],IWMHeaderInfo2 interface, GetAttributeByName method [windows Media Format],IWMHeaderInfo3 interface, IWMHeaderInfo interface [windows Media Format],GetAttributeByName method, IWMHeaderInfo.GetAttributeByName, IWMHeaderInfo2 interface [windows Media Format],GetAttributeByName method, IWMHeaderInfo2::GetAttributeByName, IWMHeaderInfo3 interface [windows Media Format],GetAttributeByName method, IWMHeaderInfo3::GetAttributeByName, IWMHeaderInfo::GetAttributeByName, IWMHeaderInfoGetAttributeByName, wmformat.iwmheaderinfo_getattributebyname, wmsdkidl/IWMHeaderInfo2::GetAttributeByName, wmsdkidl/IWMHeaderInfo3::GetAttributeByName, wmsdkidl/IWMHeaderInfo::GetAttributeByName
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
 - IWMHeaderInfo::GetAttributeByName
 - wmsdkidl/IWMHeaderInfo::GetAttributeByName
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
 - IWMHeaderInfo.GetAttributeByName
 - IWMHeaderInfo2.GetAttributeByName
 - IWMHeaderInfo3.GetAttributeByName
---

# IWMHeaderInfo::GetAttributeByName


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetAttributeByName</b> method returns a descriptive attribute that is stored in the header section of the ASF file. Now that attribute names can be duplicated in a file, this method is obsolete. To find attributes of a particular name, use <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices">IWMHeaderInfo3::GetAttributeIndices</a>.

## -parameters

### -param pwStreamNum [in, out]

Pointer to a <b>WORD</b> containing the stream number, or zero to indicate any stream. Although this parameter is a pointer, the method does not change the value.

### -param pszName [in]

Pointer to a <b>null</b>-terminated string containing the name of the attribute. Attribute names are limited to 1024 wide characters.

### -param pType [out]

Pointer to a variable that receives a value from the <a href="/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_attr_datatype">WMT_ATTR_DATATYPE</a> enumeration type. The returned value specifies the data type of the attribute.

### -param pValue [out]

Pointer to a byte array that receives the value of the attribute. The caller must allocate the array. To determine the required array size, set this parameter to <b>NULL</b> and check the value returned in the <i>pcbLength</i> parameter.

### -param pcbLength [in, out]

On input, the length of the <i>pValue</i> array, in bytes. On output, if the method succeeds, the actual number of bytes that were written to <i>pValue</i>.

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
<dt><b>ASF_E_NOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified attribute is not defined in this file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pwStreamNum</i> is not a valid stream number, <i>pszName</i> does not point to a wide-character string, or another parameter does not contain a valid value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A parameter is not a valid pointer.

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

Typically, an application should call this method twice for each attribute that it retrieves. On the first call, set the <i>pValue</i> parameter to <b>NULL</b>. The <i>pcbLength</i> parameter receives the buffer size needed to hold the attribute value. Then, allocate a sufficient byte array and call the method again, passing the address of the array in the <i>pType</i> parameter. The method fills the buffer with the value of the attribute. Coerce the buffer to the data type indicated by the value returned in <i>pType</i>.

If the file does not contain the specified attribute, the method might return ASF_E_NOTFOUND. The method can also succeed but return the value zero for <i>pcbLength</i>.

The objects of the Windows Media Format SDK perform type checking on some supported metadata attributes, but not all of them. You should ensure that any attributes you use are set using the data type specified in the <a href="/windows/desktop/wmformat/attributes">Attributes</a> section of this documentation. Likewise, you cannot assume that an attribute set by another application will use the correct data type.

Attributes in MP3 files cannot be specific to a particular stream. For MP3 files, always set the stream number to zero.

For a list of all the predefined attributes, see <a href="/windows/desktop/wmformat/attributes">Attributes</a>.


#### Examples

The following example code shows how to retrieve the "Title" attribute.


```cpp

HRESULT hr;
IWMHeaderInfo *pInfo;
WORD wStreamNum = 0;
WMT_ATTR_DATATYPE Type;
WORD cbLength;
//
// First, retrieve the length of the string, and allocate memory.
//
hr = pInfo->GetAttributeByName( &wStreamNum, L"Title", 
                                &Type, NULL, &cbLength );
if( FAILED( hr ) )
{
    return( hr );
}
WCHAR *pwszTitle = (WCHAR *) new BYTE[ cbLength ];
if( !pwszTitle )
{
    return( E_OUTOFMEMORY );
}
//
// Now, retrieve the string itself.
//
hr = pInfo->GetAttributeByName( &wStreamNum, L"Title", &Type, 
                                (BYTE *) pwszTitle, &cbLength );
if( FAILED( hr ) )
{
    return( hr );
}

```

## -see-also

<a href="/windows/desktop/wmformat/attributes">Attributes</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo">IWMHeaderInfo Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2">IWMHeaderInfo2</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3">IWMHeaderInfo3</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute">IWMHeaderInfo::SetAttribute</a>



<a href="/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_attr_datatype">WMT_ATTR_DATATYPE</a>