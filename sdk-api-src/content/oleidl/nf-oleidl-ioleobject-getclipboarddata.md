---
UID: NF:oleidl.IOleObject.GetClipboardData
title: IOleObject::GetClipboardData (oleidl.h)
description: Retrieves a data object containing the current contents of the embedded object on which this method is called. Using the pointer to this data object, it is possible to create a new embedded object with the same data as the original.
helpviewer_keywords: ["GetClipboardData","GetClipboardData method [COM]","GetClipboardData method [COM]","IOleObject interface","IOleObject interface [COM]","GetClipboardData method","IOleObject.GetClipboardData","IOleObject::GetClipboardData","_ole_ioleobject_getclipboarddata","com.ioleobject_getclipboarddata","oleidl/IOleObject::GetClipboardData"]
old-location: com\ioleobject_getclipboarddata.htm
tech.root: com
ms.assetid: 49f6b26c-76e1-4519-920b-e05279f23112
ms.date: 12/05/2018
ms.keywords: GetClipboardData, GetClipboardData method [COM], GetClipboardData method [COM],IOleObject interface, IOleObject interface [COM],GetClipboardData method, IOleObject.GetClipboardData, IOleObject::GetClipboardData, _ole_ioleobject_getclipboarddata, com.ioleobject_getclipboarddata, oleidl/IOleObject::GetClipboardData
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
 - IOleObject::GetClipboardData
 - oleidl/IOleObject::GetClipboardData
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
 - IOleObject.GetClipboardData
---

# IOleObject::GetClipboardData


## -description

Retrieves a data object containing the current contents of the embedded object on which this method is called. Using the pointer to this data object, it is possible to create a new embedded object with the same data as the original.

## -parameters

### -param dwReserved [in]

This parameter is reserved and must be zero.

### -param ppDataObject [out]

Address of <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> pointer variable that receives the interface pointer to the data object. If an error occurs, <i>ppDataObject</i> must be set to <b>NULL</b>. Each time an object receives a call to <b>IOleObject::GetClipboardData</b>, it must increase the reference count on <i>ppDataObject</i>. It is the caller's responsibility to call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> when it is done with <i>ppDataObject</i>.

## -returns

This method returns S_OK on success. Other possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-getclipboarddata">GetClipboardData</a> is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_NOTRUNNING</b></dt>
</dl>
</td>
<td width="60%">
The object is not running.

</td>
</tr>
</table>

## -remarks

You can use the <b>IOleObject::GetClipboardData</b> method to convert a linked object to an embedded object, in which case the container application would call <b>IOleObject::GetClipboardData</b> and then pass the data received to <a href="/windows/desktop/api/ole2/nf-ole2-olecreatefromdata">OleCreateFromData</a>. This method returns a pointer to a data object that is identical to what would have been passed to the clipboard by a standard copy operation.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
If you want a stable snapshot of the current contents of an embedded object, call <b>IOleObject::GetClipboardData</b>. Should the data change, you will need to call the function again for an updated snapshot. If you want the caller to be informed of changes that occur to the data, call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a>, then call <a href="/windows/desktop/api/objidl/nf-objidl-idataobject-dadvise">IDataObject::DAdvise</a>.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
If you implement this function, you must return an <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> pointer for an object whose data will not change.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleobject">IOleObject</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-initfromdata">IOleObject::InitFromData</a>



<a href="/windows/desktop/api/ole2/nf-ole2-olecreatefromdata">OleCreateFromData</a>