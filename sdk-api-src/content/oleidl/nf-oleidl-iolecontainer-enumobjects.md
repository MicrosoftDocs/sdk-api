---
UID: NF:oleidl.IOleContainer.EnumObjects
title: IOleContainer::EnumObjects (oleidl.h)
description: Enumerates the objects in the current container.
helpviewer_keywords: ["EnumObjects","EnumObjects method [COM]","EnumObjects method [COM]","IOleContainer interface","IOleContainer interface [COM]","EnumObjects method","IOleContainer.EnumObjects","IOleContainer::EnumObjects","_ole_iolecontainer_enumobjects","com.iolecontainer_enumobjects","oleidl/IOleContainer::EnumObjects"]
old-location: com\iolecontainer_enumobjects.htm
tech.root: com
ms.assetid: 7d825c71-506c-4fd3-ab48-6006f2858d05
ms.date: 12/05/2018
ms.keywords: EnumObjects, EnumObjects method [COM], EnumObjects method [COM],IOleContainer interface, IOleContainer interface [COM],EnumObjects method, IOleContainer.EnumObjects, IOleContainer::EnumObjects, _ole_iolecontainer_enumobjects, com.iolecontainer_enumobjects, oleidl/IOleContainer::EnumObjects
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
 - IOleContainer::EnumObjects
 - oleidl/IOleContainer::EnumObjects
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
 - IOleContainer.EnumObjects
---

# IOleContainer::EnumObjects


## -description

Enumerates the objects in the current container.

## -parameters

### -param grfFlags [in]

Specifies which objects in a container are to be enumerated, as defined in the enumeration <a href="/windows/desktop/api/oleidl/ne-oleidl-olecontf">OLECONTF</a>.

### -param ppenum [out]

A pointer to an <a href="/windows/desktop/api/objidl/nn-objidl-ienumunknown">IEnumUnknown</a> pointer variable that receives the interface pointer to the enumerator object. Each time a container receives a successful call to <b>EnumObjects</b>, it must increase the reference count on the <i>ppenum</i> pointer the method returns. It is the caller's responsibility to call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> when it is done with the pointer. If an error is returned, the implementation must set <i>ppenum</i> to <b>NULL</b>.

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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Object enumeration not supported.

</td>
</tr>
</table>

## -remarks

A container should implement <b>EnumObjects</b> to enable programmatic clients to find out what objects it holds. This method, however, is not called in standard linking scenarios.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-ienumunknown">IEnumUnknown</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-iolecontainer">IOleContainer</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleitemcontainer">IOleItemContainer</a>



<a href="/windows/desktop/api/oleidl/ne-oleidl-olecontf">OLECONTF</a>