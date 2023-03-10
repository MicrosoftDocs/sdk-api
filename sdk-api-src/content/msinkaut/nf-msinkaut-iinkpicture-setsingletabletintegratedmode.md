---
UID: NF:msinkaut.IInkPicture.SetSingleTabletIntegratedMode
title: IInkPicture::SetSingleTabletIntegratedMode (msinkaut.h)
description: Allows the ink collector (InkCollector, InkOverlay, or InkPicture) to collect ink from only one tablet. Ink from other tablets is ignored by the ink collector. (IInkPicture.SetSingleTabletIntegratedMode)
helpviewer_keywords: ["96787996-c0fd-455f-952e-90ddc8640253","IInkPicture interface [Tablet PC]","SetSingleTabletIntegratedMode method","IInkPicture.SetSingleTabletIntegratedMode","IInkPicture::SetSingleTabletIntegratedMode","SetSingleTabletIntegratedMode","SetSingleTabletIntegratedMode method [Tablet PC]","SetSingleTabletIntegratedMode method [Tablet PC]","IInkPicture interface","msinkaut/IInkPicture::SetSingleTabletIntegratedMode","tablet.inkpicture_setsingletabletintegratedmode"]
old-location: tablet\inkpicture_setsingletabletintegratedmode.htm
tech.root: tablet
ms.assetid: b611a078-b38e-4f9b-834f-9a2aa9684931
ms.date: 12/05/2018
ms.keywords: 96787996-c0fd-455f-952e-90ddc8640253, IInkPicture interface [Tablet PC],SetSingleTabletIntegratedMode method, IInkPicture.SetSingleTabletIntegratedMode, IInkPicture::SetSingleTabletIntegratedMode, SetSingleTabletIntegratedMode, SetSingleTabletIntegratedMode method [Tablet PC], SetSingleTabletIntegratedMode method [Tablet PC],IInkPicture interface, msinkaut/IInkPicture::SetSingleTabletIntegratedMode, tablet.inkpicture_setsingletabletintegratedmode
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
 - IInkPicture::SetSingleTabletIntegratedMode
 - msinkaut/IInkPicture::SetSingleTabletIntegratedMode
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
 - IInkPicture.SetSingleTabletIntegratedMode
---

# IInkPicture::SetSingleTabletIntegratedMode


## -description

Allows the ink collector (<a href="/windows/desktop/tablet/inkcollector-class">InkCollector</a>, <a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay</a>, or <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a>) to collect ink from only one tablet. Ink from other tablets is ignored by the ink collector.

## -parameters

### -param Tablet [in]

The tablet on which ink is collected, or drawn.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A parameter contained an invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_COLLECTOR_ENABLED</b></dt>
</dl>
</td>
<td width="60%">
Cannot change modes while the collector is enabled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_EXCEPTION</b></dt>
</dl>
</td>
<td width="60%">
An exception occurred while processing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_INCOMPATIBLE_OBJECT</b></dt>
</dl>
</td>
<td width="60%">
<i>tablet</i> does not point to a compatible Ink object.

</td>
</tr>
</table>

## -remarks

To allow the ink collector to collect ink from all tablets, call the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setalltabletsmode">SetAllTabletsMode</a> method.

<div class="alert"><b>Note</b>  The ink collector object or control that collects ink must be disabled before calling this method. To disable the <a href="/windows/desktop/tablet/inkcollector-class">InkCollector</a> object or the <a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay</a> object, set the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_enabled">Enabled</a> property to <b>FALSE</b>. To disable the <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> control, set the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled">InkEnabled</a> property to <b>FALSE</b>. After calling the <b>SetSingleTabletIntegratedMode</b> method, re-enable the object or control by setting the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_enabled">Enabled</a> (or <b>InkEnabled</b>) property to <b>TRUE</b>.</div>
<div> </div>
When this method is called, the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_cursors">Cursors</a> property of the ink collector is set to the empty collection.

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_enabled">Enabled Property</a>



<a href="../msinkaut/nn-msinkaut-iinkpicture.md">IInkPicture</a>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet">IInkTablet Interface</a>



<a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a>



<a href="/previous-versions/windows/desktop/legacy/ms704832(v=vs.85)">InkTablets Collection</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setalltabletsmode">SetAllTabletsMode Method</a>
