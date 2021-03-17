---
UID: NF:oleidl.IOleObject.GetExtent
title: IOleObject::GetExtent (oleidl.h)
description: Retrieves a running object's current display size.
helpviewer_keywords: ["GetExtent","GetExtent method [COM]","GetExtent method [COM]","IOleObject interface","IOleObject interface [COM]","GetExtent method","IOleObject.GetExtent","IOleObject::GetExtent","_ole_ioleobject_getextent","com.ioleobject_getextent","oleidl/IOleObject::GetExtent"]
old-location: com\ioleobject_getextent.htm
tech.root: com
ms.assetid: babaf55e-6c43-48d8-ad13-1333e29a3e1d
ms.date: 12/05/2018
ms.keywords: GetExtent, GetExtent method [COM], GetExtent method [COM],IOleObject interface, IOleObject interface [COM],GetExtent method, IOleObject.GetExtent, IOleObject::GetExtent, _ole_ioleobject_getextent, com.ioleobject_getextent, oleidl/IOleObject::GetExtent
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
 - IOleObject::GetExtent
 - oleidl/IOleObject::GetExtent
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
 - IOleObject.GetExtent
---

# IOleObject::GetExtent


## -description

Retrieves a running object's current display size.

## -parameters

### -param dwDrawAspect [in]

The aspect of the object whose limit is to be retrieved; the value is obtained from the enumerations <a href="/windows/desktop/api/wtypes/ne-wtypes-dvaspect">DVASPECT</a> and from <a href="/windows/desktop/api/ocidl/ne-ocidl-dvaspect2">DVASPECT2</a>. Note that newer objects and containers that support optimized drawing interfaces support the <b>DVASPECT2</b> enumeration values. Older objects and containers that do not support optimized drawing interfaces may not support <b>DVASPECT2</b>. The most common value for this method is DVASPECT_CONTENT, which specifies a full rendering of the object within its container.

### -param psizel [out]

Pointer to where the object's size is to be returned.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The supplied <i>dwDrawAspect</i> value is invalid.

</td>
</tr>
</table>

## -remarks

A container calls <b>IOleObject::GetExtent</b> on a running object to retrieve its current display size. If the container can accommodate that size, it will normally do so because the object, after all, knows what size it should be better than the container does. A container normally makes this call as part of initializing an object.

The display size returned by <b>IOleObject::GetExtent</b> may differ from the size last set by <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-setextent">IOleObject::SetExtent</a> because the latter method dictates the object's display space at the time the method is called but does not necessarily change the object's native size, as determined by its application.

If one of the new aspects is requested in <i>dwAspect</i>, this method can either fail or return the same rectangle as for the DVASPECT_CONTENT aspect.

<div class="alert"><b>Note</b>  This method must return the same size as DVASPECT_CONTENT for all the new aspects in <a href="/windows/desktop/api/ocidl/ne-ocidl-dvaspect2">DVASPECT2</a>. <a href="/windows/desktop/api/oleidl/nf-oleidl-iviewobject2-getextent">IViewObject2::GetExtent</a> must do the same thing.</div>
<div> </div>
<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Because a container can make this call only to a running object, the container must instead call <a href="/windows/desktop/api/oleidl/nf-oleidl-iviewobject2-getextent">IViewObject2::GetExtent</a> if it wants to get the display size of a loaded object from its cache.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
Implementation consists of filling the sizel structure with an object's height and width.

## -see-also

<a href="/windows/desktop/api/wtypes/ne-wtypes-dvaspect">DVASPECT</a>



<a href="/windows/desktop/api/ocidl/ne-ocidl-dvaspect2">DVASPECT2</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleobject">IOleObject</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-getextent">IOleObject::GetExtent</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-setextent">IOleObject::SetExtent</a>