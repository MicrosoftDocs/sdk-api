---
UID: NF:oleidl.IOleObject.Unadvise
title: IOleObject::Unadvise (oleidl.h)
description: Deletes a previously established advisory connection. (IOleObject.Unadvise)
helpviewer_keywords: ["IOleObject interface [COM]","Unadvise method","IOleObject.Unadvise","IOleObject::Unadvise","Unadvise","Unadvise method [COM]","Unadvise method [COM]","IOleObject interface","_ole_ioleobject_unadvise","com.ioleobject_unadvise","oleidl/IOleObject::Unadvise"]
old-location: com\ioleobject_unadvise.htm
tech.root: com
ms.assetid: e3d63a75-30b0-4fe5-9a1d-c70820583765
ms.date: 12/05/2018
ms.keywords: IOleObject interface [COM],Unadvise method, IOleObject.Unadvise, IOleObject::Unadvise, Unadvise, Unadvise method [COM], Unadvise method [COM],IOleObject interface, _ole_ioleobject_unadvise, com.ioleobject_unadvise, oleidl/IOleObject::Unadvise
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
 - IOleObject::Unadvise
 - oleidl/IOleObject::Unadvise
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
 - IOleObject.Unadvise
---

# IOleObject::Unadvise


## -description

Deletes a previously established advisory connection.

## -parameters

### -param dwConnection [in]

Contains a token of nonzero value, which was previously returned from <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-advise">IOleObject::Advise</a> through its <i>pdwConnection</i> parameter.

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
<dt><b>OLE_E_NOCONNECTION</b></dt>
</dl>
</td>
<td width="60%">
dwConnection does not represent a valid advisory connection.

</td>
</tr>
</table>

## -remarks

Normally, containers call <b>IOleObject::Unadvise</b> at shutdown or when an object is deleted. In certain cases, containers can call this method on objects that are running but not currently visible as a way of reducing the overhead of maintaining multiple advisory connections. The easiest way to implement this method is to delegate the call to <b>IOleObject::Unadvise</b>.

## -see-also

<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleadviseholder-unadvise">IOleAdviseHolder::Unadvise</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleobject">IOleObject</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-advise">IOleObject::Advise</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-enumadvise">IOleObject::EnumAdvise</a>
