---
UID: NF:oleidl.IViewObject2.GetExtent
title: IViewObject2::GetExtent (oleidl.h)
description: Retrieves the size that the specified view object will be drawn on the specified target device.
helpviewer_keywords: ["GetExtent","GetExtent method [COM]","GetExtent method [COM]","IViewObject2 interface","IViewObject2 interface [COM]","GetExtent method","IViewObject2.GetExtent","IViewObject2::GetExtent","_ole_iviewobject2_getextent","com.iviewobject2_getextent","oleidl/IViewObject2::GetExtent"]
old-location: com\iviewobject2_getextent.htm
tech.root: com
ms.assetid: 66eedee0-58b5-4676-93db-599ed19a02b6
ms.date: 12/05/2018
ms.keywords: GetExtent, GetExtent method [COM], GetExtent method [COM],IViewObject2 interface, IViewObject2 interface [COM],GetExtent method, IViewObject2.GetExtent, IViewObject2::GetExtent, _ole_iviewobject2_getextent, com.iviewobject2_getextent, oleidl/IViewObject2::GetExtent
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
req.dll: Adhocreportingexcelclient.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IViewObject2::GetExtent
 - oleidl/IViewObject2::GetExtent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - adhocreportingexcelclient.dll
api_name:
 - IViewObject2.GetExtent
---

# IViewObject2::GetExtent


## -description

Retrieves the size that the specified view object will be drawn on the specified target device.

## -parameters

### -param dwDrawAspect [in]

Requested view of the object whose size is of interest. Possible values are taken from the <a href="/windows/desktop/api/wtypes/ne-wtypes-dvaspect">DVASPECT</a> and <a href="/windows/desktop/api/ocidl/ne-ocidl-dvaspect2">DVASPECT2</a> enumerations. Note that newer objects and containers that support optimized drawing interfaces support the <b>DVASPECT2</b> enumeration values. Older objects and containers that do not support optimized drawing interfaces may not support <b>DVASPECT2</b>.

### -param lindex [in]

The portion of the object that is of interest. Currently, the only possible value is -1.

### -param ptd [in]

A pointer to the <a href="/windows/desktop/api/objidl/ns-objidl-dvtargetdevice">DVTARGETDEVICE</a> structure defining the target device for which the object's size should be returned.

### -param lpsizel [out]

A pointer to where the object's size is returned.

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
<dt><b>OLE_E_BLANK</b></dt>
</dl>
</td>
<td width="60%">
An appropriate cache is not available.

</td>
</tr>
</table>

## -remarks

The OLE-provided implementation of <b>IViewObject2::GetExtent</b> searches the cache for the size of the view object.

The <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-getextent">IOleObject::GetExtent</a> method in the <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleobject">IOleObject</a> interface provides some of the same information as <b>IViewObject2::GetExtent</b>.



This method must return the same size as DVASPECT_CONTENT for all the new aspects in <a href="/windows/desktop/api/ocidl/ne-ocidl-dvaspect2">DVASPECT2</a>. <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-getextent">IOleObject::GetExtent</a> must do the same thing.

If one of the new aspects is requested in <i>dwAspect</i>, this method can either fail or return the same rectangle as for the DVASPECT_CONTENT aspect.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
To prevent the object from being run if it isn't already running, you can call <b>IViewObject2::GetExtent</b> rather than <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-getextent">IOleObject::GetExtent</a> to determine the size of the presentation to be drawn.

## -see-also

<a href="/windows/desktop/api/wtypes/ne-wtypes-dvaspect">DVASPECT</a>



<a href="/windows/desktop/api/ocidl/ne-ocidl-dvaspect2">DVASPECT2</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-getextent">IOleObject::GetExtent</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-iviewobject">IViewObject</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-iviewobject2">IViewObject2</a>