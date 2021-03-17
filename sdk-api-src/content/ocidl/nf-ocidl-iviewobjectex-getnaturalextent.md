---
UID: NF:ocidl.IViewObjectEx.GetNaturalExtent
title: IViewObjectEx::GetNaturalExtent (ocidl.h)
description: Provides sizing hints from the container for the object to use as the user resizes it.
helpviewer_keywords: ["DVASPECT_CONTENT","DVASPECT_DOCPRINT","DVASPECT_ICON","DVASPECT_THUMBNAIL","GetNaturalExtent","GetNaturalExtent method [COM]","GetNaturalExtent method [COM]","IViewObjectEx interface","IViewObjectEx interface [COM]","GetNaturalExtent method","IViewObjectEx.GetNaturalExtent","IViewObjectEx::GetNaturalExtent","_ole_iviewobjectex_getnaturalextent","com.iviewobjectex_getnaturalextent","ocidl/IViewObjectEx::GetNaturalExtent"]
old-location: com\iviewobjectex_getnaturalextent.htm
tech.root: com
ms.assetid: 5759c482-2dea-4b94-956d-9560f72acbd5
ms.date: 12/05/2018
ms.keywords: DVASPECT_CONTENT, DVASPECT_DOCPRINT, DVASPECT_ICON, DVASPECT_THUMBNAIL, GetNaturalExtent, GetNaturalExtent method [COM], GetNaturalExtent method [COM],IViewObjectEx interface, IViewObjectEx interface [COM],GetNaturalExtent method, IViewObjectEx.GetNaturalExtent, IViewObjectEx::GetNaturalExtent, _ole_iviewobjectex_getnaturalextent, com.iviewobjectex_getnaturalextent, ocidl/IViewObjectEx::GetNaturalExtent
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
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
 - IViewObjectEx::GetNaturalExtent
 - ocidl/IViewObjectEx::GetNaturalExtent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IViewObjectEx.GetNaturalExtent
---

# IViewObjectEx::GetNaturalExtent


## -description

Provides sizing hints from the container for the object to use as the user resizes it.

## -parameters

### -param dwAspect [in]

The requested drawing aspect. It can be any of the following values, which are defined by the <a href="/windows/desktop/api/wtypes/ne-wtypes-dvaspect">DVASPECT</a> enumeration.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DVASPECT_CONTENT"></a><a id="dvaspect_content"></a><dl>
<dt><b>DVASPECT_CONTENT</b></dt>
</dl>
</td>
<td width="60%">
Provide a representation of the control so it can be displayed as an embedded object inside of a container. This value is typically specified for compound document objects. The presentation can be provided for the screen or printer.

</td>
</tr>
<tr>
<td width="40%"><a id="DVASPECT_DOCPRINT"></a><a id="dvaspect_docprint"></a><dl>
<dt><b>DVASPECT_DOCPRINT</b></dt>
</dl>
</td>
<td width="60%">
Provide a representation of the control on the screen as though it were printed to a printer using the <b>Print</b> command from the <b>File</b> menu. The described data may represent a sequence of pages.

</td>
</tr>
<tr>
<td width="40%"><a id="DVASPECT_ICON"></a><a id="dvaspect_icon"></a><dl>
<dt><b>DVASPECT_ICON</b></dt>
</dl>
</td>
<td width="60%">
Provide an iconic representation of the control.

</td>
</tr>
<tr>
<td width="40%"><a id="DVASPECT_THUMBNAIL"></a><a id="dvaspect_thumbnail"></a><dl>
<dt><b>DVASPECT_THUMBNAIL</b></dt>
</dl>
</td>
<td width="60%">
Provide a thumbnail representation of an object so it can be displayed in a browsing tool. The thumbnail is approximately a 120 by 120 pixel, 16-color (recommended) device-independent bitmap potentially wrapped in a metafile.

</td>
</tr>
</table>

### -param lindex [in]

Indicates the portion of the object that is of interest for the draw operation. Its interpretation varies depending on the value in the <i>dwAspect</i> parameter. See the <a href="/windows/desktop/api/wtypes/ne-wtypes-dvaspect">DVASPECT</a> enumeration for more information.

### -param ptd [in]

Pointer to the target device structure that describes the device for which the object is to be rendered. If <b>NULL</b>, the view should be rendered for the default target device (typically the display). A value other than <b>NULL</b> is interpreted in conjunction with <i>hicTargetDev</i> and <b>hdcDraw</b>. For example, if <b>hdcDraw</b> specifies a printer as the device context, the <i>ptd</i> parameter points to a structure describing that printer device. The data may actually be printed if <i>hicTargetDev</i> is a valid value or it may be displayed in print preview mode if <i>hicTargetDev</i> is <b>NULL</b>.

### -param hicTargetDev [in]

Specifies the information context for the target device indicated by the ptd parameter from which the object can extract device metrics and test the device's capabilities. If <i>ptd</i> is <b>NULL</b>; the object should ignore the value in the <i>hicTargetDev</i> parameter.

### -param pExtentInfo [in]

Pointer to <a href="/windows/win32/api/ocidl/ns-ocidl-dvextentinfo">DVEXTENTINFO</a> structure that specifies the sizing data.

### -param pSizel [out]

Pointer to sizing data returned by the object. The returned sizing data is set to -1 for any dimension that was not adjusted. That is if <b>cx</b> is -1 then the width was not adjusted, if <b>cy</b> is -1 then the height was not adjusted. If E_FAIL is returned indicating no size was adjusted then <i>pSizel</i> may be <b>NULL</b>.

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
This method is not implemented for the specified <i>dwAspect</i>, or the size was not adjusted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
This method was not implemented.

</td>
</tr>
</table>

## -remarks

There are two general approaches to sizing a control. The first approach gives the control responsibility for sizing itself; the second approach gives the container responsibility for sizing the control. The first approach is called autosizing. There are two alternatives involved in the second approach: content sizing and integral sizing.

The <b>IViewObjectEx::GetNaturalExtent</b> method supports both content and integral sizing. In content sizing, the container passes the <a href="/windows/win32/api/ocidl/ns-ocidl-dvextentinfo">DVEXTENTINFO</a> structure to the object into which the object returns a suggested size. In integral sizing, the container passes a preferred size to the object in <b>DVEXTENTINFO</b>, and the object actually adjusts its height. Integral sizing is used when the user rubberbands a new size in design mode.

Autosizing typically occurs with objects such as the Label control which resizes if the autosize property was enabled and the associated text changed. Autosizing is handled differently depending on the state of the object.

If the object is inactive, the following occurs:

<ol>
<li>The object calls <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleclientsite-requestnewobjectlayout">IOleClientSite::RequestNewObjectLayout</a>.</li>
<li>The container calls <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-getextent">IOleObject::GetExtent</a> and retrieves the new extents.</li>
<li>The container calls <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-setextent">IOleObject::SetExtent</a> and adjusts the new extents.</li>
</ol>
If the object is active, the following occurs:

<ol>
<li>The object calls <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplacesite-onposrectchange">IOleInPlaceSite::OnPosRectChange</a> to specify that it requires resizing.</li>
<li>The container calls <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceobject-setobjectrects">IOleInPlaceObject::SetObjectRects</a> and specifies the new size.</li>
</ol>

## -see-also

<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleclientsite-requestnewobjectlayout">IOleClientSite::RequestNewObjectLayout</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceobject-setobjectrects">IOleInPlaceObject::SetObjectRects</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplacesite-onposrectchange">IOleInPlaceSite::OnPosRectChange</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-getextent">IOleObject::GetExtent</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-setextent">IOleObject::SetExtent</a>



<a href="/windows/desktop/api/ocidl/nn-ocidl-iviewobjectex">IViewObjectEx</a>