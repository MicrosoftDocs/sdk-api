---
UID: NF:objidl.IDataObject.GetData
title: IDataObject::GetData (objidl.h)
description: Called by a data consumer to obtain data from a source data object.
helpviewer_keywords: ["GetData","GetData method [COM]","GetData method [COM]","IDataObject interface","IDataObject interface [COM]","GetData method","IDataObject.GetData","IDataObject::GetData","_ole_idataobject_getdata","com.idataobject_getdata","objidl/IDataObject::GetData"]
old-location: com\idataobject_getdata.htm
tech.root: com
ms.assetid: 05118461-0438-4715-b2c2-fc2471ce38f0
ms.date: 12/05/2018
ms.keywords: GetData, GetData method [COM], GetData method [COM],IDataObject interface, IDataObject interface [COM],GetData method, IDataObject.GetData, IDataObject::GetData, _ole_idataobject_getdata, com.idataobject_getdata, objidl/IDataObject::GetData
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
 - IDataObject::GetData
 - objidl/IDataObject::GetData
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
 - IDataObject.GetData
---

# IDataObject::GetData


## -description

Called by a data consumer to obtain data from a source data object. The <b>GetData</b> method renders the data described in the specified <a href="/windows/desktop/api/objidl/ns-objidl-formatetc">FORMATETC</a> structure and transfers it through the specified <a href="/windows/win32/api/objidl/ns-objidl-ustgmedium-r1">STGMEDIUM</a> structure. The caller then assumes responsibility for releasing the <b>STGMEDIUM</b> structure.

## -parameters

### -param pformatetcIn [in]

A pointer to the <a href="/windows/desktop/api/objidl/ns-objidl-formatetc">FORMATETC</a> structure that defines the format, medium, and target device to use when passing the data. It is possible to specify more than one medium by using the Boolean OR operator, allowing the method to choose the best medium among those specified.

### -param pmedium [out]

A pointer to the <a href="/windows/win32/api/objidl/ns-objidl-ustgmedium-r1">STGMEDIUM</a> structure that indicates the storage medium containing the returned data through its tymed member, and the responsibility for releasing the medium through the value of its <b>pUnkForRelease</b> member. If <b>pUnkForRelease</b> is <b>NULL</b>, the receiver of the medium is responsible for releasing it; otherwise, <b>pUnkForRelease</b> points to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> on the appropriate object so its <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> method can be called. The medium must be allocated and filled in by <b>GetData</b>.

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
The value for <b>lindex</b> is not valid; currently, only -1 is supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DV_E_FORMATETC</b></dt>
</dl>
</td>
<td width="60%">
The value for <i>pformatetcIn</i> is not valid.

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
<dt><b>STG_E_MEDIUMFULL</b></dt>
</dl>
</td>
<td width="60%">
An error occurred when allocating the medium.

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

A data consumer calls <b>GetData</b> to retrieve data from a data object, conveyed through a storage medium (defined through the <a href="/windows/win32/api/objidl/ns-objidl-ustgmedium-r1">STGMEDIUM</a> structure).

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
You can specify more than one acceptable <b>tymed</b> medium with the Boolean OR operator. <b>GetData</b> must choose from the OR'd values the medium that best represents the data, do the allocation, and indicate responsibility for releasing the medium.

Data transferred across a stream extends from position zero of the stream pointer through to the position immediately before the current stream pointer (that is, the stream pointer position upon exit).

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
<b>GetData</b> must check all fields in the <a href="/windows/desktop/api/objidl/ns-objidl-formatetc">FORMATETC</a> structure. It is important that <b>GetData</b> render the requested aspect and, if possible, use the requested medium. If the data object cannot comply with the information specified in the <b>FORMATETC</b>, the method should return DV_E_FORMATETC. If an attempt to allocate the medium fails, the method should return STG_E_MEDIUMFULL. It is important to fill in all of the fields in the <a href="/windows/win32/api/objidl/ns-objidl-ustgmedium-r1">STGMEDIUM</a> structure.

Although the caller can specify more than one medium for returning the data, <b>GetData</b> can provide only one medium. If the initial transfer fails with the selected medium, this method can be implemented to try one of the other media specified before returning an error.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>