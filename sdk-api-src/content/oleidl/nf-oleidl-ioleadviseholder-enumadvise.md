---
UID: NF:oleidl.IOleAdviseHolder.EnumAdvise
title: IOleAdviseHolder::EnumAdvise (oleidl.h)
description: Creates an enumerator that can be used to enumerate the advisory connections currently established for an object.
helpviewer_keywords: ["EnumAdvise","EnumAdvise method [COM]","EnumAdvise method [COM]","IOleAdviseHolder interface","IOleAdviseHolder interface [COM]","EnumAdvise method","IOleAdviseHolder.EnumAdvise","IOleAdviseHolder::EnumAdvise","_ole_ioleadviseholder_enumadvise","com.ioleadviseholder_enumadvise","oleidl/IOleAdviseHolder::EnumAdvise"]
old-location: com\ioleadviseholder_enumadvise.htm
tech.root: com
ms.assetid: 80a9ccd8-f89a-40c4-8b99-38536409cf26
ms.date: 12/05/2018
ms.keywords: EnumAdvise, EnumAdvise method [COM], EnumAdvise method [COM],IOleAdviseHolder interface, IOleAdviseHolder interface [COM],EnumAdvise method, IOleAdviseHolder.EnumAdvise, IOleAdviseHolder::EnumAdvise, _ole_ioleadviseholder_enumadvise, com.ioleadviseholder_enumadvise, oleidl/IOleAdviseHolder::EnumAdvise
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
 - IOleAdviseHolder::EnumAdvise
 - oleidl/IOleAdviseHolder::EnumAdvise
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
 - IOleAdviseHolder.EnumAdvise
---

# IOleAdviseHolder::EnumAdvise


## -description

Creates an enumerator that can be used to enumerate the advisory connections currently established for an object.

## -parameters

### -param ppenumAdvise [out]

A pointer to an <a href="/windows/desktop/api/objidl/nn-objidl-ienumstatdata">IEnumSTATDATA</a> pointer variable that receives the interface pointer to the new enumerator. If this parameter is <b>NULL</b>, there are presently no advisory connections on the object, or an error occurred. The advise holder is responsible for incrementing the reference count on the <b>IEnumSTATDATA</b> pointer this method supplies. It is the caller's responsibility to call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> when it is finished with the pointer.

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
The enumeration operation has failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleadviseholder-enumadvise">IOleAdviseHolder::EnumAdvise</a> is not implemented.

</td>
</tr>
</table>

## -remarks

<b>IOleAdviseHolder::EnumAdvise</b> creates an enumerator that can be used to enumerate an object's established advisory connections. The method supplies a pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-ienumstatdata">IEnumSTATDATA</a> interface on this enumerator. Advisory connection information for each connection is stored in the <a href="/windows/desktop/api/objidl/ns-objidl-statdata">STATDATA</a> structure, and the enumerator must be able to enumerate these structures.

For this method, the only relevant structure members are <b>pAdvise</b> and <b>dwConnection</b>. Other members contain data advisory information. When you call the enumeration methods, and while an enumeration is in progress, the effect of registering or revoking advisory connections on what is to be enumerated is undefined.

## -see-also

<a href="/windows/desktop/api/objidl/nf-objidl-idataadviseholder-enumadvise">IDataAdviseHolder::EnumAdvise</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleadviseholder">IOleAdviseHolder</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleadviseholder-advise">IOleAdviseHolder::Advise</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleadviseholder-unadvise">IOleAdviseHolder::Unadvise</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-enumadvise">IOleObject::EnumAdvise</a>



<a href="/windows/desktop/api/objidl/ns-objidl-statdata">STATDATA</a>