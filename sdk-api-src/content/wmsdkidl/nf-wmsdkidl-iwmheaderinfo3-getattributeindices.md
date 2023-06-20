---
UID: NF:wmsdkidl.IWMHeaderInfo3.GetAttributeIndices
title: IWMHeaderInfo3::GetAttributeIndices (wmsdkidl.h)
description: The GetAttributeIndices method retrieves a list of valid attribute indices within specified parameters.
helpviewer_keywords: ["GetAttributeIndices","GetAttributeIndices method [windows Media Format]","GetAttributeIndices method [windows Media Format]","IWMHeaderInfo3 interface","IWMHeaderInfo3 interface [windows Media Format]","GetAttributeIndices method","IWMHeaderInfo3.GetAttributeIndices","IWMHeaderInfo3::GetAttributeIndices","IWMHeaderInfo3GetAttributeIndices","wmformat.iwmheaderinfo3_getattributeindices","wmsdkidl/IWMHeaderInfo3::GetAttributeIndices"]
old-location: wmformat\iwmheaderinfo3_getattributeindices.htm
tech.root: wmformat
ms.assetid: 15c8f0c2-f2d4-441a-b6a9-774da820d03c
ms.date: 4/26/2023
ms.keywords: GetAttributeIndices, GetAttributeIndices method [windows Media Format], GetAttributeIndices method [windows Media Format],IWMHeaderInfo3 interface, IWMHeaderInfo3 interface [windows Media Format],GetAttributeIndices method, IWMHeaderInfo3.GetAttributeIndices, IWMHeaderInfo3::GetAttributeIndices, IWMHeaderInfo3GetAttributeIndices, wmformat.iwmheaderinfo3_getattributeindices, wmsdkidl/IWMHeaderInfo3::GetAttributeIndices
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
 - IWMHeaderInfo3::GetAttributeIndices
 - wmsdkidl/IWMHeaderInfo3::GetAttributeIndices
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
 - IWMHeaderInfo3.GetAttributeIndices
---

# IWMHeaderInfo3::GetAttributeIndices


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetAttributeIndices</b> method retrieves a list of valid attribute indices within specified parameters. You can retrieve indices for all attributes with the same name or for all attributes in a specified language. The indices found are for a single specific stream. Alternatively, you can retrieve the specified indices for the entire file.

## -parameters

### -param wStreamNum [in]

<b>WORD</b> containing the stream number for which to retrieve attribute indices. Passing zero retrieves indices for file-level attributes. Passing 0xFFFF retrieves indices for all appropriate attributes, regardless of their association to streams.

### -param pwszName [in]

Pointer to a wide-character null-terminated string containing the attribute name for which you want to retrieve indices. Pass NULL to retrieve indices for attributes based on language. Attribute names are limited to 1024 wide characters.

### -param pwLangIndex [in]

Pointer to a <b>WORD</b> containing the language index of the language for which to retrieve attribute indices. Pass NULL to retrieve indices for attributes by name.

### -param pwIndices [out]

Pointer to a <b>WORD</b> array containing the indices that meet the criteria described by the input parameters. Pass NULL to retrieve the size of the array, which will be returned in <i>pwCount</i>.

### -param pwCount [in, out]

On output, pointer to a <b>WORD</b> containing the number of elements in the <i>pwIndices</i> array.

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
The size specified in <i>pwCount</i> is too small.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALID_REQUEST</b></dt>
</dl>
</td>
<td width="60%">
<i>wStreamNum</i> is not a valid stream number, <i>pwLangIndex</i> is not a valid language index, or <i>pwszName</i> is not a valid name.

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

You must make two calls to <b>GetAttributeIndices</b> for each set of indices retrieved. On the first call, pass NULL as <i>pwIndices</i>. On return, the variable pointed to by <i>pwCount</i> is set to the number of elements required for the array of indices. Then allocate memory for the array and make the second call, passing a pointer to the array as <i>pwIndices</i>.

If you use 0xFFFF for the stream number, the index values returned will be global indices. Only use a global index for calls to other methods of the IWMHeaderInfo3 interface if you will also be using 0xFFFF for the stream number. The global index value for an attribute will be different than the value used when specifying a specific stream number (or stream 0 for file-level attributes).

Index values obtained by using this method are given in descending order by index. This is to aid in deleting attributes, which should always be done in descending order.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3">IWMHeaderInfo3 Interface</a>