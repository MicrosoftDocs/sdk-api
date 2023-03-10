---
UID: NF:oleidl.IOleObject.SetExtent
title: IOleObject::SetExtent (oleidl.h)
description: Informs an object of how much display space its container has assigned it.
helpviewer_keywords: ["IOleObject interface [COM]","SetExtent method","IOleObject.SetExtent","IOleObject::SetExtent","SetExtent","SetExtent method [COM]","SetExtent method [COM]","IOleObject interface","_ole_ioleobject_setextent","com.ioleobject_setextent","oleidl/IOleObject::SetExtent"]
old-location: com\ioleobject_setextent.htm
tech.root: com
ms.assetid: f1960095-7c9a-4058-aef1-f31e3d6e3509
ms.date: 12/05/2018
ms.keywords: IOleObject interface [COM],SetExtent method, IOleObject.SetExtent, IOleObject::SetExtent, SetExtent, SetExtent method [COM], SetExtent method [COM],IOleObject interface, _ole_ioleobject_setextent, com.ioleobject_setextent, oleidl/IOleObject::SetExtent
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
 - IOleObject::SetExtent
 - oleidl/IOleObject::SetExtent
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
 - IOleObject.SetExtent
---

# IOleObject::SetExtent


## -description

Informs an object of how much display space its container has assigned it.

## -parameters

### -param dwDrawAspect [in]

DWORD that describes which form, or "aspect," of an object is to be displayed. The object's container obtains this value from the enumeration <a href="/windows/desktop/api/wtypes/ne-wtypes-dvaspect">DVASPECT</a> (refer to the <a href="/windows/desktop/api/objidl/ns-objidl-formatetc">FORMATETC</a> enumeration). The most common aspect is DVASPECT_CONTENT, which specifies a full rendering of the object within its container. An object can also be rendered as an icon, a thumbnail version for display in a browsing tool, or a print version, which displays the object as it would be rendered using the <b>File Print</b> command.

### -param psizel [in]

Pointer to the size limit for the object.

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
<dt><b>OLE_E_NOTRUNNING</b></dt>
</dl>
</td>
<td width="60%">
The object is not running.

</td>
</tr>
</table>

## -remarks

A container calls <b>IOleObject::SetExtent</b> when it needs to dictate to an embedded object the size at which it will be displayed. Often, this call occurs in response to an end user resizing the object window. Upon receiving the call, the object, if possible, should recompose itself gracefully to fit the new window.

Whenever possible, a container seeks to display an object at its finest resolution, sometimes called the object's native size. All objects, however, have a default display size specified by their applications, and in the absence of other constraints, this is the size they will use to display themselves. Since an object knows its optimum display size better than does its container, the latter normally requests that size from a running object by calling <b>IOleObject::SetExtent</b>. Only in cases where the container cannot accommodate the value returned by the object does it override the object's preference by calling <b>IOleObject::SetExtent</b>.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
You can call <b>IOleObject::SetExtent</b> on an object only when the object is running. If a container resizes an object while an object is not running, the container should keep track of the object's new size but defer calling <b>IOleObject::SetExtent</b> until a user activates the object. If the OLEMISC_RECOMPOSEONRESIZE bit is set on an object, its container should force the object to run before calling <b>IOleObject::SetExtent</b>.

As noted above, a container may want to delegate responsibility for setting the size of an object's display site to the object itself, by calling <b>IOleObject::SetExtent</b>.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
You may want to implement this method so that your object rescales itself to match as closely as possible the maximum space available to it in its container.

If an object's size is fixed, that is, if it cannot be set by its container, <b>IOleObject::SetExtent</b> should return E_FAIL. This is always the case with linked objects, whose sizes are set by their link sources, not by their containers.

## -see-also

<a href="/windows/desktop/api/objidl/nf-objidl-iadvisesink-onviewchange">IAdviseSink::OnViewChange</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleobject">IOleObject</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-getextent">IOleObject::GetExtent</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-iviewobject2-getextent">IViewObject2::GetExtent</a>