---
UID: NF:msinkaut.IInkDisp.Load
title: IInkDisp::Load (msinkaut.h)
description: Populates a new InkDisp object with known binary data.
helpviewer_keywords: ["2e71e434-b055-4e45-b8fd-f9c1ac84d308","IInkDisp interface [Tablet PC]","Load method","IInkDisp.Load","IInkDisp::Load","Load","Load method [Tablet PC]","Load method [Tablet PC]","IInkDisp interface","msinkaut/IInkDisp::Load","tablet.inkdisp_load"]
old-location: tablet\inkdisp_load.htm
tech.root: tablet
ms.assetid: 2e71e434-b055-4e45-b8fd-f9c1ac84d308
ms.date: 12/05/2018
ms.keywords: 2e71e434-b055-4e45-b8fd-f9c1ac84d308, IInkDisp interface [Tablet PC],Load method, IInkDisp.Load, IInkDisp::Load, Load, Load method [Tablet PC], Load method [Tablet PC],IInkDisp interface, msinkaut/IInkDisp::Load, tablet.inkdisp_load
req.header: msinkaut.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: InkObj.dll
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInkDisp::Load
 - msinkaut/IInkDisp::Load
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkDisp.Load
---

# IInkDisp::Load


## -description

Populates a new <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object with known binary data.

## -parameters

### -param Data [in]

The stream that contains the ink data.

For more information about the VARIANT structure, see <a href="/windows/desktop/tablet/using-the-com-library">Using the COM Library</a>.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
VARIANT was not of correct type (byte array).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Cannot allocate memory for Stream.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected parameter or property type.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_EXCEPTION</b></dt>
</dl>
</td>
<td width="60%">
An exception occurred inside the method.

</td>
</tr>
</table>

## -remarks

You can load ink  only into a new, empty <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object - one that hasn't collected any strokes or doesn't have any attached properties. If you try to load ink into an <b>InkDisp</b> object that has collected strokes or attached properties, even if the strokes or properties have been deleted from the <b>InkDisp</b> object, an exception is thrown. This occurs because of how stroke IDs are assigned. A stroke is assigned a unique ID, and this ID is not reused, even if the stroke has been deleted from an Ink object. This means that, if an <b>InkDisp</b> object contained a stroke with an ID of 1 and you deleted the stroke and loaded another <b>InkDisp</b> object into this <b>InkDisp</b> object, stroke IDs would start at 2. This would be confusing and therefore is not allowed.

<div class="alert"><b>Note</b>  If you do attempt to load ink into an <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object that is not empty, all data in the <b>InkDisp</b> object, including any custom strokes or extended properties, is lost when you call <b>Load</b>.</div>
<div> </div>
The <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-save">Save</a> method allows you to persist the ink in an <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object in Graphics Interchange Format (GIF) format, which consists of an array of byte data (the tla_gif persistence format is specified in the <a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkpersistenceformat">InkPersistenceFormat</a> enumeration type). After you have the array of byte data, you can load the array of byte data into another <b>InkDisp</b> object. This means that you can load GIF-compatible byte array data into another <b>InkDisp</b> object in the same way as if you had called the <b>Save</b> method and received a byte array that was not in GIF format.

<div class="alert"><b>Note</b>  You cannot create an image, persist that image as a byte array, and then load that byte array into another <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object. This is because, after you load byte array data as a GIF, Tablet PC cannot control the format of that data. So, after you persist the image into a byte array again, you cannot call <b>Load</b> on that data.</div>
<div> </div>

## -see-also

<a href="../msinkaut/nn-msinkaut-iinkdisp.md">IInkDisp</a>



<a href="/windows/desktop/tablet/inkdisp-class">InkDisp Class</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-save">Save Method</a>
