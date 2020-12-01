---
UID: NF:wmsdkidl.IWMHeaderInfo3.DeleteAttribute
title: IWMHeaderInfo3::DeleteAttribute (wmsdkidl.h)
description: The DeleteAttribute method removes an attribute from the file header.
helpviewer_keywords: ["DeleteAttribute","DeleteAttribute method [windows Media Format]","DeleteAttribute method [windows Media Format]","IWMHeaderInfo3 interface","IWMHeaderInfo3 interface [windows Media Format]","DeleteAttribute method","IWMHeaderInfo3.DeleteAttribute","IWMHeaderInfo3::DeleteAttribute","IWMHeaderInfo3DeleteAttribute","wmformat.iwmheaderinfo3_deleteattribute","wmsdkidl/IWMHeaderInfo3::DeleteAttribute"]
old-location: wmformat\iwmheaderinfo3_deleteattribute.htm
tech.root: wmformat
ms.assetid: a69da90f-c8c5-4bf7-a1d8-7031aa9d1704
ms.date: 12/05/2018
ms.keywords: DeleteAttribute, DeleteAttribute method [windows Media Format], DeleteAttribute method [windows Media Format],IWMHeaderInfo3 interface, IWMHeaderInfo3 interface [windows Media Format],DeleteAttribute method, IWMHeaderInfo3.DeleteAttribute, IWMHeaderInfo3::DeleteAttribute, IWMHeaderInfo3DeleteAttribute, wmformat.iwmheaderinfo3_deleteattribute, wmsdkidl/IWMHeaderInfo3::DeleteAttribute
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
 - IWMHeaderInfo3::DeleteAttribute
 - wmsdkidl/IWMHeaderInfo3::DeleteAttribute
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
 - IWMHeaderInfo3.DeleteAttribute
---

# IWMHeaderInfo3::DeleteAttribute


## -description

The <b>DeleteAttribute</b> method removes an attribute from the file header.

## -parameters

### -param wStreamNum [in]

<b>WORD</b> containing the stream number for which the attribute applies. Setting this value to zero indicates a file-level attribute.

### -param wIndex [in]

<b>WORD</b> containing the index of the attribute to be deleted.

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
<dt><b>NS_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
<i>wStreamNum</i> is not a valid stream number, or there is not an attribute at <i>wIndex</i>.

</td>
</tr>
</table>

## -remarks

You can use 0xFFFF for the stream number to specify an attribute using its global index. Global index values range from 0 to one less than the count of attributes received from a call to <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributecountex">IWMHeaderInfo3::GetAttributeCountEx</a> where the stream number was set to 0xFFFF.

When deleting multiple attributes, you should do so in descending order by index value. For convenience, this is the order in which index values are retrieved by <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices">IWMHeaderInfo3::GetAttributeIndices</a>.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3">IWMHeaderInfo3 Interface</a>