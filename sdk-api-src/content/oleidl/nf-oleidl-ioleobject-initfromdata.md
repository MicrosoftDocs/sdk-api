---
UID: NF:oleidl.IOleObject.InitFromData
title: IOleObject::InitFromData (oleidl.h)
description: Initializes a newly created object with data from a specified data object, which can reside either in the same container or on the Clipboard.
helpviewer_keywords: ["IOleObject interface [COM]","InitFromData method","IOleObject.InitFromData","IOleObject::InitFromData","InitFromData","InitFromData method [COM]","InitFromData method [COM]","IOleObject interface","_ole_ioleobject_initfromdata","com.ioleobject_initfromdata","oleidl/IOleObject::InitFromData"]
old-location: com\ioleobject_initfromdata.htm
tech.root: com
ms.assetid: 8bbda602-4421-4f79-a33a-63ded9a8bf90
ms.date: 12/05/2018
ms.keywords: IOleObject interface [COM],InitFromData method, IOleObject.InitFromData, IOleObject::InitFromData, InitFromData, InitFromData method [COM], InitFromData method [COM],IOleObject interface, _ole_ioleobject_initfromdata, com.ioleobject_initfromdata, oleidl/IOleObject::InitFromData
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.Idl
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
 - IOleObject::InitFromData
 - oleidl/IOleObject::InitFromData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
api_name:
 - IOleObject.InitFromData
---

# IOleObject::InitFromData


## -description

Initializes a newly created object with data from a specified data object, which can reside either in the same container or on the Clipboard.

## -parameters

### -param pDataObject [in]

Pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> interface on the data object from which the initialization data is to be obtained. This parameter can be <b>NULL</b>, which indicates that the caller wants to know if it is worthwhile trying to send data; that is, whether the container is capable of initializing an object from data passed to it. The data object to be passed can be based on either the current selection within the container document or on data transferred to the container from an external source.

### -param fCreation [in]

<b>TRUE</b> indicates the container is inserting a new object inside itself and initializing that object with data from the current selection; <b>FALSE</b> indicates a more general programmatic data transfer, most likely from a source other than the current selection.

### -param dwReserved [in]

This parameter is reserved and must be zero.

## -returns

This method returns S_OK if <i>pDataObject</i> is not <b>NULL</b>, the object successfully attempted to initialize itself from the provided data; if <i>pDataObject</i> is <b>NULL</b>, the object is able to attempt a successful initialization.. Other possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
If pDataObject is not <b>NULL</b>, the object made no attempt to initialize itself; if <i>pDataObject</i> is <b>NULL</b>, the object cannot attempt to initialize itself from the data provided.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The object does not support <i>InitFromData</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_NOTRUNNING</b></dt>
</dl>
</td>
<td width="60%">
The object is not running and therefore cannot perform the operation.

</td>
</tr>
</table>

## -remarks

This method enables a container document to insert within itself a new object whose content is based on a current data selection within the container. For example, a spreadsheet document may want to create a graph object based on data in a selected range of cells.

Using this method, a container can also replace the contents of an embedded object with data transferred from another source. This provides a convenient way of updating an embedded object.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Following initialization, the container should call <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-getmiscstatus">IOleObject::GetMiscStatus</a> to check the value of the OLEMISC_INSERTNOTREPLACE bit. If the bit is on, the new object inserts itself following the selected data. If the bit is off, the new object replaces the selected data.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
A container specifies whether to base a new object on the current selection by passing either <b>TRUE</b> or <b>FALSE</b> to the <i>fCreation</i> parameter.

If <i>fCreation</i> is <b>TRUE</b>, the container is attempting to create a new instance of an object, initializing it with the selected data specified by the data object.

If <i>fCreation</i> is <b>FALSE</b>, the caller is attempting to replace the object's current contents with that pointed to by <i>pDataObject</i>. The usual constraints that apply to an object during a paste operation should be applied here. For example, if the type of the data provided is unacceptable, the object should fail to initialize and return S_FALSE.

If the object returns S_FALSE, it cannot initialize itself from the provided data.

## -see-also

<a href="/windows/desktop/api/objidl/nf-objidl-idataobject-setdata">IDataObject::SetData</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleobject">IOleObject</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-getmiscstatus">IOleObject::GetMiscStatus</a>