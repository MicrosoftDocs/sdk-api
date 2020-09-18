---
UID: NF:objidl.IDataObject.QueryGetData
title: IDataObject::QueryGetData (objidl.h)
description: Determines whether the data object is capable of rendering the data as specified. Objects attempting a paste or drop operation can call this method before calling IDataObject::GetData to get an indication of whether the operation may be successful.
helpviewer_keywords: ["IDataObject interface [COM]","QueryGetData method","IDataObject.QueryGetData","IDataObject::QueryGetData","QueryGetData","QueryGetData method [COM]","QueryGetData method [COM]","IDataObject interface","_ole_idataobject_querygetdata","com.idataobject_querygetdata","objidl/IDataObject::QueryGetData"]
old-location: com\idataobject_querygetdata.htm
tech.root: com
ms.assetid: 38a1bb4f-7762-4e74-a386-4ae05e59d15f
ms.date: 12/05/2018
ms.keywords: IDataObject interface [COM],QueryGetData method, IDataObject.QueryGetData, IDataObject::QueryGetData, QueryGetData, QueryGetData method [COM], QueryGetData method [COM],IDataObject interface, _ole_idataobject_querygetdata, com.idataobject_querygetdata, objidl/IDataObject::QueryGetData
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDataObject::QueryGetData
 - objidl/IDataObject::QueryGetData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - IDataObject.QueryGetData
---

# IDataObject::QueryGetData


## -description

Determines whether the data object is capable of rendering the data as specified. Objects attempting a paste or drop operation can call this method before calling <a href="/windows/desktop/api/objidl/nf-objidl-idataobject-getdata">IDataObject::GetData</a> to get an indication of whether the operation may be successful.

## -parameters

### -param pformatetc [in]

A pointer to the <a href="/windows/desktop/api/objidl/ns-objidl-formatetc">FORMATETC</a> structure defining the format, medium, and target device to use for the query.

## -returns

This method returns S_OK on success. Other possible values include the following

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DV_E_LINDEX</b></dt>
</dl>
</td>
<td width="60%">
Invalid value for <b>lindex</b>; currently, only -1 is supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DV_E_FORMATETC</b></dt>
</dl>
</td>
<td width="60%">
Invalid value for <i>pformatetc</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DV_E_TYMED</b></dt>
</dl>
</td>
<td width="60%">
The <b>tymed</b> value is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DV_E_DVASPECT</b></dt>
</dl>
</td>
<td width="60%">
The <b>dwAspect</b> value is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_NOTRUNNING</b></dt>
</dl>
</td>
<td width="60%">
The object application is not running.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error has occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwDirection</i> value is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is insufficient memory available for this operation.

</td>
</tr>
</table>

## -remarks

The client of a data object calls <b>QueryGetData</b> to determine whether passing the specified <a href="/windows/desktop/api/objidl/ns-objidl-formatetc">FORMATETC</a> structure to a subsequent call to <a href="/windows/desktop/api/objidl/nf-objidl-idataobject-getdata">IDataObject::GetData</a> is likely to be successful. A successful return from this method does not necessarily ensure the success of the subsequent paste or drop operation.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>