---
UID: NF:objidl.IDataObject.GetDataHere
title: IDataObject::GetDataHere (objidl.h)
description: Called by a data consumer to obtain data from a source data object. This method differs from the GetData method in that the caller must allocate and free the specified storage medium.
helpviewer_keywords: ["GetDataHere","GetDataHere method [COM]","GetDataHere method [COM]","IDataObject interface","IDataObject interface [COM]","GetDataHere method","IDataObject.GetDataHere","IDataObject::GetDataHere","_ole_idataobject_getdatahere","com.idataobject_getdatahere","objidl/IDataObject::GetDataHere"]
old-location: com\idataobject_getdatahere.htm
tech.root: com
ms.assetid: 802fc49a-21c2-4490-9b00-1359ce9c325f
ms.date: 12/05/2018
ms.keywords: GetDataHere, GetDataHere method [COM], GetDataHere method [COM],IDataObject interface, IDataObject interface [COM],GetDataHere method, IDataObject.GetDataHere, IDataObject::GetDataHere, _ole_idataobject_getdatahere, com.idataobject_getdatahere, objidl/IDataObject::GetDataHere
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
 - IDataObject::GetDataHere
 - objidl/IDataObject::GetDataHere
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
 - IDataObject.GetDataHere
---

# IDataObject::GetDataHere


## -description

Called by a data consumer to obtain data from a source data object. This method differs from the <a href="/windows/desktop/api/objidl/nf-objidl-idataobject-getdata">GetData</a> method in that the caller must allocate and free the specified storage medium.

## -parameters

### -param pformatetc [in]

A pointer to the <a href="/windows/desktop/api/objidl/ns-objidl-formatetc">FORMATETC</a> structure that defines the format, medium, and target device to use when passing the data. Only one medium can be specified in <b>tymed</b>, and only the following values are valid: TYMED_ISTORAGE, TYMED_ISTREAM, TYMED_HGLOBAL, or TYMED_FILE.

### -param pmedium [in, out]

A pointer to the <a href="/windows/win32/api/objidl/ns-objidl-ustgmedium-r1">STGMEDIUM</a> structure that defines the storage medium containing the data being transferred. The medium must be allocated by the caller and filled in by <b>GetDataHere</b>. The caller must also free the medium. The implementation of this method must always supply a value of <b>NULL</b> for the <b>punkForRelease</b> member of the <b>STGMEDIUM</b> structure to which this parameter points.

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
The <i>dwDirection</i> parameter is not valid.

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

The <b>GetDataHere</b> method is similar to <a href="/windows/desktop/api/objidl/nf-objidl-idataobject-getdata">IDataObject::GetData</a>, except that the caller must both allocate and free the medium specified in <i>pmedium</i>. <b>GetDataHere</b> renders the data described in a <a href="/windows/desktop/api/objidl/ns-objidl-formatetc">FORMATETC</a> structure and copies the data into that caller-provided <a href="/windows/win32/api/objidl/ns-objidl-ustgmedium-r1">STGMEDIUM</a> structure. For example, if the medium is TYMED_HGLOBAL, this method cannot resize the medium or allocate a new hGlobal.

Some media are not appropriate in a call to <b>GetDataHere</b>, including GDI types such as metafiles. The <b>GetDataHere</b> method cannot put data into a caller-provided metafile. In general, the only storage media it is necessary to support in this method are TYMED_ISTORAGE, TYMED_ISTREAM, and TYMED_FILE.

When the transfer medium is a stream, OLE makes assumptions about where the data is being returned and the position of the stream's seek pointer. In a <a href="/windows/desktop/api/objidl/nf-objidl-idataobject-getdata">GetData</a> call, the data returned is from stream position zero through just before the current seek pointer of the stream (that is, the position on exit). For <b>GetDataHere</b>, the data returned is from the stream position on entry through just before the position on exit.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>