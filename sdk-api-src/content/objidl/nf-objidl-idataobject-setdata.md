---
UID: NF:objidl.IDataObject.SetData
title: IDataObject::SetData (objidl.h)
description: Called by an object containing a data source to transfer data to the object that implements this method.
helpviewer_keywords: ["IDataObject interface [COM]","SetData method","IDataObject.SetData","IDataObject::SetData","SetData","SetData method [COM]","SetData method [COM]","IDataObject interface","_ole_idataobject_setdata","com.idataobject_setdata","objidl/IDataObject::SetData"]
old-location: com\idataobject_setdata.htm
tech.root: com
ms.assetid: 7430d12c-ab07-4a9c-a845-4743818afbc7
ms.date: 12/05/2018
ms.keywords: IDataObject interface [COM],SetData method, IDataObject.SetData, IDataObject::SetData, SetData, SetData method [COM], SetData method [COM],IDataObject interface, _ole_idataobject_setdata, com.idataobject_setdata, objidl/IDataObject::SetData
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
 - IDataObject::SetData
 - objidl/IDataObject::SetData
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
 - IDataObject.SetData
---

# IDataObject::SetData


## -description

Called by an object containing a data source to transfer data to the object that implements this method.

## -parameters

### -param pformatetc [in]

A pointer to the <a href="/windows/desktop/api/objidl/ns-objidl-formatetc">FORMATETC</a> structure defining the format used by the data object when interpreting the data contained in the storage medium.

### -param pmedium [in]

A pointer to the <a href="/windows/win32/api/objidl/ns-objidl-ustgmedium-r1">STGMEDIUM</a> structure defining the storage medium in which the data is being passed.

### -param fRelease [in]

If <b>TRUE</b>, the data object called, which implements <b>SetData</b>, owns the storage medium after the call returns. This means it must free the medium after it has been used by calling the <a href="/windows/desktop/api/ole2/nf-ole2-releasestgmedium">ReleaseStgMedium</a> function. If <b>FALSE</b>, the caller retains ownership of the storage medium and the data object called uses the storage medium for the duration of the call only.

## -returns

This method returns S_OK on success. Other possible values include the following.

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
The value for <i>pformatetc</i> is not valid.

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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The operation failed.

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
There was insufficient memory available for this operation.

</td>
</tr>
</table>

## -remarks

<b>SetData</b> allows another object to attempt to send data to the implementing data object. A data object implements this method if it supports receiving data from another object. If it does not support this, it should be implemented to return E_NOTIMPL.

The caller allocates the storage medium indicated by the <i>pmedium</i> parameter, in which the data is passed. The data object called does not take ownership of the data until it has successfully received it and no error code is returned. The value of the <i>fRelease</i> parameter indicates the ownership of the medium after the call returns. <b>FALSE</b> indicates the caller still owns the medium, and the data object only has the use of it during the call; <b>TRUE</b> indicates that the data object now owns it and must release it when it is no longer needed.

The type of medium specified in the <i>pformatetc</i> and <i>pmedium</i> parameters must be the same. For example, one cannot be a global handle and the other a stream.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>