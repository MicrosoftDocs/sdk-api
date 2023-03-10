---
UID: NF:oleidl.IOleObject.EnumVerbs
title: IOleObject::EnumVerbs (oleidl.h)
description: Exposes a pull-down menu listing the verbs available for an object in ascending order by verb number.
helpviewer_keywords: ["EnumVerbs","EnumVerbs method [COM]","EnumVerbs method [COM]","IOleObject interface","IOleObject interface [COM]","EnumVerbs method","IOleObject.EnumVerbs","IOleObject::EnumVerbs","_ole_ioleobject_enumverbs","com.ioleobject_enumverbs","oleidl/IOleObject::EnumVerbs"]
old-location: com\ioleobject_enumverbs.htm
tech.root: com
ms.assetid: c67770d0-e478-41dc-9028-1e0a6cb9e3c7
ms.date: 12/05/2018
ms.keywords: EnumVerbs, EnumVerbs method [COM], EnumVerbs method [COM],IOleObject interface, IOleObject interface [COM],EnumVerbs method, IOleObject.EnumVerbs, IOleObject::EnumVerbs, _ole_ioleobject_enumverbs, com.ioleobject_enumverbs, oleidl/IOleObject::EnumVerbs
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
 - IOleObject::EnumVerbs
 - oleidl/IOleObject::EnumVerbs
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
 - IOleObject.EnumVerbs
---

# IOleObject::EnumVerbs


## -description

Exposes a pull-down menu listing the verbs available for an object in ascending order by verb number.

## -parameters

### -param ppEnumOleVerb [out]

Address of <a href="/windows/desktop/api/oleidl/nn-oleidl-ienumoleverb">IEnumOLEVERB</a> pointer variable that receives the interface pointer to the new enumerator object. Each time an object receives a call to <b>IOleObject::EnumVerbs</b>, it must increase the reference count on <i>ppEnumOleVerb</i>. It is the caller's responsibility to call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> when it is done with <i>ppEnumOleVerb</i>. If an error occurs, <i>ppEnumOleVerb</i> must be set to <b>NULL</b>.

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
<dt><b>OLE_S_USEREG</b></dt>
</dl>
</td>
<td width="60%">
Delegate to the default handler to use the entries in the registry to provide the enumeration.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEOBJ_E_NOVERBS</b></dt>
</dl>
</td>
<td width="60%">
Object does not support any verbs.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleobject">IOleObject</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-doverb">IOleObject::DoVerb</a>



<a href="/windows/desktop/api/ole2/nf-ole2-oleregenumverbs">OleRegEnumVerbs</a>