---
UID: NF:oleidl.IViewObject.GetColorSet
title: IViewObject::GetColorSet (oleidl.h)
description: Returns the logical palette that the object will use for drawing in its IViewObject::Draw method with the corresponding parameters.
helpviewer_keywords: ["GetColorSet","GetColorSet method [COM]","GetColorSet method [COM]","IViewObject interface","IViewObject interface [COM]","GetColorSet method","IViewObject.GetColorSet","IViewObject::GetColorSet","_ole_iviewobject_getcolorset","com.iviewobject_getcolorset","oleidl/IViewObject::GetColorSet"]
old-location: com\iviewobject_getcolorset.htm
tech.root: com
ms.assetid: 68454266-ca31-44ec-8847-4d47001d9849
ms.date: 12/05/2018
ms.keywords: GetColorSet, GetColorSet method [COM], GetColorSet method [COM],IViewObject interface, IViewObject interface [COM],GetColorSet method, IViewObject.GetColorSet, IViewObject::GetColorSet, _ole_iviewobject_getcolorset, com.iviewobject_getcolorset, oleidl/IViewObject::GetColorSet
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
 - IViewObject::GetColorSet
 - oleidl/IViewObject::GetColorSet
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
 - IViewObject.GetColorSet
---

# IViewObject::GetColorSet


## -description

Returns the logical palette that the object will use for drawing in its <a href="/windows/desktop/api/oleidl/nf-oleidl-iviewobject-draw">IViewObject::Draw</a> method with the corresponding parameters.

## -parameters

### -param dwDrawAspect [in]

Specifies how the object is to be represented. Representations include content, an icon, a thumbnail, or a printed document. Valid values are taken from the enumeration <a href="/windows/desktop/api/wtypes/ne-wtypes-dvaspect">DVASPECT</a>. See the <b>DVASPECT</b> enumeration for more information.

### -param lindex [in]

Portion of the object that is of interest for the draw operation. Its interpretation varies with <i>dwDrawAspect</i>. See the <a href="/windows/desktop/api/wtypes/ne-wtypes-dvaspect">DVASPECT</a> enumeration for more information.

### -param pvAspect [in]

Pointer to additional information about the view of the object specified in <i>dwDrawAspect</i>. Since none of the current aspects support additional information, <i>pvAspect</i> must always be <b>NULL</b>.

### -param ptd [in]

Pointer to the <a href="/windows/desktop/api/objidl/ns-objidl-dvtargetdevice">DVTARGETDEVICE</a> structure that describes the device for which the object is to be rendered. If <b>NULL</b>, the view should be rendered for the default target device (typically the display). A value other than <b>NULL</b> is interpreted in conjunction with <i>hicTargetDev</i> and <i>hdcDraw</i>. For example, if <i>hdcDraw</i> specifies a printer as the device context, ptd points to a structure describing that printer device. The data may actually be printed if <i>hicTargetDev</i> is a valid value or it may be displayed in print preview mode if <i>hicTargetDev</i> is <b>NULL</b>.

### -param hicTargetDev [in]

Information context for the target device indicated by the <i>ptd</i> parameter from which the object can extract device metrics and test the device's capabilities. If <i>ptd</i> is <b>NULL</b>, the object should ignore the <i>hicTargetDev</i> parameter.

### -param ppColorSet [out]

Address of LOGPALETTE pointer variable that receives a pointer to the LOGPALETTE structure. The LOGPALETTE structure contains the set of colors that would be used if <a href="/windows/desktop/api/oleidl/nf-oleidl-iviewobject-draw">IViewObject::Draw</a> were called with the same parameters for <i>dwAspect</i>, <i>lindex</i>, <i>pvAspect</i>, <i>ptd</i>, and <i>hicTargetDev</i>. If <i>ppColorSet</i> is <b>NULL</b>, the object does not use a palette.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Set of colors is empty or the object will not give out the information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_BLANK</b></dt>
</dl>
</td>
<td width="60%">
No presentation data for object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DV_E_LINDEX</b></dt>
</dl>
</td>
<td width="60%">
Invalid value for <i>lindex</i>; currently only -1 is supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DV_E_DVASPECT</b></dt>
</dl>
</td>
<td width="60%">
Invalid value for <i>dwAspect</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more of the supplied parameter values is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory available for this operation.

</td>
</tr>
</table>

## -remarks

The <b>IViewObject::GetColorSet</b> method recursively queries any nested objects and returns a color set that represents the union of all colors requested. The color set eventually percolates to the top-level container that owns the window frame. This container can call <b>IViewObject::GetColorSet</b> on each of its embedded objects to obtain all the colors needed to draw the embedded objects. The container can use the color sets obtained in conjunction with other colors it needs for itself to set the overall color palette.

The OLE-provided implementation of <b>IViewObject::GetColorSet</b> looks at the data it has on hand to draw the picture. If CF_DIB is the drawing format, the palette found in the bitmap is used. For a regular bitmap, no color information is returned. If the drawing format is a metafile, the object handler enumerates the metafile looking for a CreatePalette metafile record. If one is found, the handler uses it as the color set.

## -see-also

<a href="/windows/desktop/api/wtypes/ne-wtypes-dvaspect">DVASPECT</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-iviewobject">IViewObject</a>