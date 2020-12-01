---
UID: NF:objidl.IDataObject.EnumFormatEtc
title: IDataObject::EnumFormatEtc (objidl.h)
description: Creates an object to enumerate the formats supported by a data object.
helpviewer_keywords: ["EnumFormatEtc","EnumFormatEtc method [COM]","EnumFormatEtc method [COM]","IDataObject interface","IDataObject interface [COM]","EnumFormatEtc method","IDataObject.EnumFormatEtc","IDataObject::EnumFormatEtc","_ole_idataobject_enumformatetc","com.idataobject_enumformatetc","objidl/IDataObject::EnumFormatEtc"]
old-location: com\idataobject_enumformatetc.htm
tech.root: com
ms.assetid: 657a7394-4481-4e0c-912d-40a9348caf16
ms.date: 12/05/2018
ms.keywords: EnumFormatEtc, EnumFormatEtc method [COM], EnumFormatEtc method [COM],IDataObject interface, IDataObject interface [COM],EnumFormatEtc method, IDataObject.EnumFormatEtc, IDataObject::EnumFormatEtc, _ole_idataobject_enumformatetc, com.idataobject_enumformatetc, objidl/IDataObject::EnumFormatEtc
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
 - IDataObject::EnumFormatEtc
 - objidl/IDataObject::EnumFormatEtc
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
 - IDataObject.EnumFormatEtc
---

# IDataObject::EnumFormatEtc


## -description

Creates an object to enumerate the formats supported by a data object.

## -parameters

### -param dwDirection [in]

The direction of the data.  Possible values come from the <a href="/windows/desktop/api/objidl/ne-objidl-datadir">DATADIR</a> enumeration.

The value DATADIR_GET enumerates the formats that can be passed in to a call to <a href="/windows/desktop/api/objidl/nf-objidl-idataobject-getdata">IDataObject::GetData</a>. The value DATADIR_SET enumerates those formats that can be passed in to a call to <a href="/windows/desktop/api/objidl/nf-objidl-idataobject-setdata">IDataObject::SetData</a>.

### -param ppenumFormatEtc [out]

A pointer to an <a href="/windows/desktop/api/objidl/nn-objidl-ienumformatetc">IEnumFORMATETC</a> pointer variable that receives the interface pointer to the new enumerator object.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The supplied <i>dwDirection</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory available for this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The direction specified by <i>dwDirection</i> is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_S_USEREG</b></dt>
</dl>
</td>
<td width="60%">
Requests that OLE enumerate the formats from the registry.

</td>
</tr>
</table>

## -remarks

<b>EnumFormatEtc</b> creates an enumerator object that can be used to determine all of the ways the data object can describe data in a <a href="/windows/desktop/api/objidl/ns-objidl-formatetc">FORMATETC</a> structure, and provides a pointer to its <a href="/windows/desktop/api/objidl/nn-objidl-ienumformatetc">IEnumFORMATETC</a> interface. This is one of the standard enumerator interfaces.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Having obtained the pointer, the caller can enumerate the <a href="/windows/desktop/api/objidl/ns-objidl-formatetc">FORMATETC</a> structures by calling the enumeration methods of <a href="/windows/desktop/api/objidl/nn-objidl-ienumformatetc">IEnumFORMATETC</a>. Because the formats can change over time, there is no guarantee that an enumerated format is currently supported because the formats can change over time. Accordingly, applications should treat the enumeration as a hint of the format types that can be passed. The caller is responsible for calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> when it is finished with the enumerator.

<b>EnumFormatEtc</b> is called when one of the following actions occurs:

<ul>
<li>An application calls <a href="/windows/desktop/api/ole2/nf-ole2-olesetclipboard">OleSetClipboard</a>. OLE must determine what data to place on the clipboard and whether it is necessary to put OLE 1 compatibility formats on the clipboard.</li>
<li>Data is being pasted from the clipboard or dropped. An application uses the first acceptable format.
</li>
<li>The <b>Paste Special</b> dialog box is displayed. The target application builds the list of formats from the <a href="/windows/desktop/api/objidl/ns-objidl-formatetc">FORMATETC</a> entries.</li>
</ul>
<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
Formats can be registered statically in the registry or dynamically during object initialization. If an object has an unchanging list of formats and these formats are registered in the registry, OLE provides an implementation of a <a href="/windows/desktop/api/objidl/ns-objidl-formatetc">FORMATETC</a> enumeration object that can enumerate formats registered under a specific CLSID in the registry. A pointer to its <a href="/windows/desktop/api/objidl/nn-objidl-ienumformatetc">IEnumFORMATETC</a> interface is available through a call to the helper function <a href="/windows/desktop/api/ole2/nf-ole2-oleregenumformatetc">OleRegEnumFormatEtc</a>. In this situation, therefore, you can implement the <b>EnumFormatEtc</b> method simply with a call to this function.

EXE applications can effectively do the same thing by implementing the method to return the value OLE_S_USEREG. This return value instructs the default object handler to call <a href="/windows/desktop/api/ole2/nf-ole2-oleregenumformatetc">OleRegEnumFormatEtc</a>. Object applications that are implemented as DLL object applications cannot return OLE_S_USEREG, so must call <b>OleRegEnumFormatEtc</b> directly.

Private formats can be enumerated for OLE 1 objects, if they are registered with the RequestDataFormats or SetDataFormats keys in the registry. Also, private formats can be enumerated for OLE objects (all versions after OLE 1), if they are registered with the GetDataFormats or SetDataFormats keys.

For OLE 1 objects whose servers do not have RequestDataFormats or SetDataFormats information registered in the registry, a call to <b>EnumFormatEtc</b> passing DATADIR_GET only enumerates the native and metafile formats, regardless of whether they support these formats or others. Calling <b>EnumFormatEtc</b> passing DATADIR_SET on such objects only enumerates native, regardless of whether the object supports being set with other formats.

The <a href="/windows/desktop/api/objidl/ns-objidl-formatetc">FORMATETC</a> structure returned by the enumeration usually indicates a <b>NULL</b> target device (ptd). This is appropriate because, unlike the other members of <b>FORMATETC</b>, the target device does not participate in the object's decision as to whether it can accept or provide the data in either a SetData or GetData call.

The <b>tymed</b> member of <a href="/windows/desktop/api/objidl/ns-objidl-formatetc">FORMATETC</a> often indicates that more than one kind of storage medium is acceptable. You should always mask and test for this by using a Boolean OR operator.

## -see-also

<a href="/windows/desktop/api/objidl/ns-objidl-formatetc">FORMATETC</a>



<a href="/windows/desktop/api/objidl/nf-objidl-idataobject-getdata">IDataObject::GetData</a>



<a href="/windows/desktop/api/objidl/nf-objidl-idataobject-setdata">IDataObject::SetData</a>



<a href="/windows/desktop/api/objidl/nn-objidl-ienumformatetc">IEnumFORMATETC</a>



<a href="/windows/desktop/api/ole2/nf-ole2-oleregenumformatetc">OleRegEnumFormatEtc</a>