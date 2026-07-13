---
UID: NF:oleidl.IOleObject.Update
title: IOleObject::Update (oleidl.h)
description: Updates an object handler's or link object's data or view caches.
helpviewer_keywords: ["IOleObject interface [COM]","Update method","IOleObject.Update","IOleObject::Update","Update","Update method [COM]","Update method [COM]","IOleObject interface","_ole_ioleobject_update","com.ioleobject_update","oleidl/IOleObject::Update"]
old-location: com\ioleobject_update.htm
tech.root: com
ms.assetid: 1743f99b-4c3b-47be-b77b-1d3378a44903
ms.date: 12/05/2018
ms.keywords: IOleObject interface [COM],Update method, IOleObject.Update, IOleObject::Update, Update, Update method [COM], Update method [COM],IOleObject interface, _ole_ioleobject_update, com.ioleobject_update, oleidl/IOleObject::Update
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
 - IOleObject::Update
 - oleidl/IOleObject::Update
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
 - IOleObject.Update
---

# IOleObject::Update


## -description

Updates an object handler's or link object's data or view caches.



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
<dt><b>OLE_E_CANT_BINDTOSOURCE</b></dt>
</dl>
</td>
<td width="60%">
Cannot run object to get updated data. The object is for some reason unavailable to the caller.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CACHE_E_NOCACHE_UPDATED</b></dt>
</dl>
</td>
<td width="60%">
No caches were updated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CACHE_S_SOMECACHES_NOTUPDATED</b></dt>
</dl>
</td>
<td width="60%">
Some caches were not updated.

</td>
</tr>
</table>

## -remarks

The <b>Update</b> method provides a way for containers to keep data updated in their linked and embedded objects. A link object can become out-of-date if the link source has been updated. An embedded object that contains links to other objects can also become out of date. An embedded object that does not contain links cannot become out of date because its data is not linked to another source.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
When a container calls a link object's <b>IOleObject::Update</b> method, the link object finds the link source and gets a new presentation from it. This process may also involve running one or more object applications, which could be time-consuming.

When a container calls an embedded object's <b>IOleObject::Update</b> method, it is requesting the object to update all link objects it may contain. In response, the object handler recursively calls <b>IOleObject::Update</b> for each of its own linked objects, running each one as needed.

## -see-also

<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleobject">IOleObject</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-isuptodate">IOleObject::IsUpToDate</a>
