---
UID: NF:objidl.IDataAdviseHolder.Unadvise
title: IDataAdviseHolder::Unadvise (objidl.h)
description: Removes a connection between a data object and an advisory sink that was set up through a previous call to IDataAdviseHolder::Advise. This method is typically called in the implementation of IDataObject::DUnadvise.
helpviewer_keywords: ["IDataAdviseHolder interface [COM]","Unadvise method","IDataAdviseHolder.Unadvise","IDataAdviseHolder::Unadvise","Unadvise","Unadvise method [COM]","Unadvise method [COM]","IDataAdviseHolder interface","_ole_idataadviseholder_unadvise","com.idataadviseholder_unadvise","objidl/IDataAdviseHolder::Unadvise"]
old-location: com\idataadviseholder_unadvise.htm
tech.root: com
ms.assetid: baeb29fd-1dd2-4320-911d-b271b2250184
ms.date: 12/05/2018
ms.keywords: IDataAdviseHolder interface [COM],Unadvise method, IDataAdviseHolder.Unadvise, IDataAdviseHolder::Unadvise, Unadvise, Unadvise method [COM], Unadvise method [COM],IDataAdviseHolder interface, _ole_idataadviseholder_unadvise, com.idataadviseholder_unadvise, objidl/IDataAdviseHolder::Unadvise
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
 - IDataAdviseHolder::Unadvise
 - objidl/IDataAdviseHolder::Unadvise
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
 - IDataAdviseHolder.Unadvise
---

# IDataAdviseHolder::Unadvise


## -description

Removes a connection between a data object and an advisory sink that was set up through a previous call to <a href="/windows/desktop/api/objidl/nf-objidl-idataadviseholder-advise">IDataAdviseHolder::Advise</a>. This method is typically called in the implementation of <a href="/windows/desktop/api/objidl/nf-objidl-idataobject-dunadvise">IDataObject::DUnadvise</a>.

## -parameters

### -param dwConnection [in]

A token that specifies the connection to be removed. This value was returned by <a href="/windows/desktop/api/objidl/nf-objidl-idataadviseholder-advise">IDataAdviseHolder::Advise</a> when the connection was originally established.

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
The <i>dwConnection</i> parameter does not specify a valid connection.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-idataadviseholder">IDataAdviseHolder</a>



<a href="/windows/desktop/api/objidl/nf-objidl-idataobject-dunadvise">IDataObject::DUnadvise</a>