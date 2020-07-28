---
UID: NF:msinkaut.IInkCollector.SetSingleTabletIntegratedMode
title: IInkCollector::SetSingleTabletIntegratedMode (msinkaut.h)
description: Allows the ink collector (InkCollector, InkOverlay, or InkPicture) to collect ink from only one tablet. Ink from other tablets is ignored by the ink collector.
helpviewer_keywords: ["96787996-c0fd-455f-952e-90ddc8640253","IInkCollector interface [Tablet PC]","SetSingleTabletIntegratedMode method","IInkCollector.SetSingleTabletIntegratedMode","IInkCollector::SetSingleTabletIntegratedMode","SetSingleTabletIntegratedMode","SetSingleTabletIntegratedMode method [Tablet PC]","SetSingleTabletIntegratedMode method [Tablet PC]","IInkCollector interface","msinkaut/IInkCollector::SetSingleTabletIntegratedMode","tablet.inkcollector_setsingletabletintegratedmode"]
old-location: tablet\inkcollector_setsingletabletintegratedmode.htm
tech.root: tablet
ms.assetid: 96787996-c0fd-455f-952e-90ddc8640253
ms.date: 12/05/2018
ms.keywords: 96787996-c0fd-455f-952e-90ddc8640253, IInkCollector interface [Tablet PC],SetSingleTabletIntegratedMode method, IInkCollector.SetSingleTabletIntegratedMode, IInkCollector::SetSingleTabletIntegratedMode, SetSingleTabletIntegratedMode, SetSingleTabletIntegratedMode method [Tablet PC], SetSingleTabletIntegratedMode method [Tablet PC],IInkCollector interface, msinkaut/IInkCollector::SetSingleTabletIntegratedMode, tablet.inkcollector_setsingletabletintegratedmode
f1_keywords:
- msinkaut/IInkCollector.SetSingleTabletIntegratedMode
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
api_name:
- IInkCollector.SetSingleTabletIntegratedMode
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkCollector::SetSingleTabletIntegratedMode


## -description



Allows the ink collector (<a href="https://docs.microsoft.com/windows/desktop/tablet/inkcollector-class">InkCollector</a>, <a href="https://docs.microsoft.com/windows/desktop/tablet/inkoverlay-class">InkOverlay</a>, or <a href="https://docs.microsoft.com/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a>) to collect ink from only one tablet. Ink from other tablets is ignored by the ink collector.




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
The tablet cannot change modes while the collector is enabled.

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
The tablet does not point to a compatible Ink object.

</td>
</tr>
</table>
 




## -remarks



To allow the ink collector to collect ink from all tablets, call the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setalltabletsmode">SetAllTabletsMode</a> method.

<div class="alert"><b>Note</b>  The ink collector object or control that collects ink must be disabled before calling this method. To disable the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkcollector-class">InkCollector</a> object or the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkoverlay-class">InkOverlay</a> object, set the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_enabled">Enabled</a> property to <b>FALSE</b>. To disable the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> control, set the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled">InkEnabled</a> property to <b>FALSE</b>. After calling the <b>SetSingleTabletIntegratedMode</b> method, re-enable the object or control by setting the <b>Enabled</b> (or <b>InkEnabled</b>) property to <b>TRUE</b>.</div>
<div> </div>
When this method is called, the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_cursors">Cursors</a> property of the ink collector is set to the empty collection.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_enabled">Enabled Property</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt846796(v=VS.85).aspx">IInkCollector</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet">IInkTablet Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/inkcollector-class">InkCollector Class</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms704832(v=vs.85)">InkTablets Collection</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setalltabletsmode">SetAllTabletsMode Method</a>
 

 

