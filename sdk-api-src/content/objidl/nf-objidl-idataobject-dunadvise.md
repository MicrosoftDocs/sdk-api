---
UID: NF:objidl.IDataObject.DUnadvise
title: IDataObject::DUnadvise (objidl.h)
description: Destroys a notification connection that had been previously set up.
helpviewer_keywords: ["DUnadvise","DUnadvise method [COM]","DUnadvise method [COM]","IDataObject interface","IDataObject interface [COM]","DUnadvise method","IDataObject.DUnadvise","IDataObject::DUnadvise","_ole_idataobject_dunadvise","com.idataobject_dunadvise","objidl/IDataObject::DUnadvise"]
old-location: com\idataobject_dunadvise.htm
tech.root: com
ms.assetid: bb9ae4c5-8655-4553-9a1c-ce52c6c86299
ms.date: 12/05/2018
ms.keywords: DUnadvise, DUnadvise method [COM], DUnadvise method [COM],IDataObject interface, IDataObject interface [COM],DUnadvise method, IDataObject.DUnadvise, IDataObject::DUnadvise, _ole_idataobject_dunadvise, com.idataobject_dunadvise, objidl/IDataObject::DUnadvise
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
 - IDataObject::DUnadvise
 - objidl/IDataObject::DUnadvise
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
 - IDataObject.DUnadvise
---

# IDataObject::DUnadvise


## -description

Destroys a notification connection that had been previously set up.

## -parameters

### -param dwConnection [in]

A token that specifies the connection to be removed. Use the value returned by <a href="/windows/desktop/api/objidl/nf-objidl-idataobject-dadvise">IDataObject::DAdvise</a> when the connection was originally established.

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
<dt><b>OLE_E_NOCONNECTION</b></dt>
</dl>
</td>
<td width="60%">
The specified value for <i>dwConnection</i> is not a valid connection.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_ADVISENOTSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
This <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> implementation does not support notification.

</td>
</tr>
</table>

## -remarks

This methods destroys a notification created with a call to the <a href="/windows/desktop/api/objidl/nf-objidl-idataobject-dadvise">IDataObject::DAdvise</a> method.

If the advisory connection being deleted was initially set up by delegating the <a href="/windows/desktop/api/objidl/nf-objidl-idataobject-dadvise">IDataObject::DAdvise</a> call to <a href="/windows/desktop/api/objidl/nf-objidl-idataadviseholder-advise">IDataAdviseHolder::Advise</a>, you must delegate this call to <a href="/windows/desktop/api/objidl/nf-objidl-idataadviseholder-unadvise">IDataAdviseHolder::Unadvise</a> to delete it.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>