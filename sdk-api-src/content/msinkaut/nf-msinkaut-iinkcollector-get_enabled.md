---
UID: NF:msinkaut.IInkCollector.get_Enabled
title: IInkCollector::get_Enabled (msinkaut.h)
description: Gets or sets a value that specifies whether the InkCollector object collects pen input (in-air packets, cursor in range events, and so on). (Get)
helpviewer_keywords: ["Enabled property [Tablet PC]","Enabled property [Tablet PC]","IInkCollector interface","IInkCollector interface [Tablet PC]","Enabled property","IInkCollector.Enabled","IInkCollector.get_Enabled","IInkCollector.put_Enabled","IInkCollector::Enabled","IInkCollector::get_Enabled","IInkCollector::put_Enabled","InkCollector.get_Enabled","InkCollector.put_Enabled","ab55a399-1990-4cfc-a4ab-834a5db8d7a9","get_Enabled","msinkaut/IInkCollector::Enabled","msinkaut/IInkCollector::get_Enabled","msinkaut/IInkCollector::put_Enabled","put_Enabled","tablet.inkcollector_enabled"]
old-location: tablet\inkcollector_enabled.htm
tech.root: tablet
ms.assetid: ab55a399-1990-4cfc-a4ab-834a5db8d7a9
ms.date: 12/05/2018
ms.keywords: Enabled property [Tablet PC], Enabled property [Tablet PC],IInkCollector interface, IInkCollector interface [Tablet PC],Enabled property, IInkCollector.Enabled, IInkCollector.get_Enabled, IInkCollector.put_Enabled, IInkCollector::Enabled, IInkCollector::get_Enabled, IInkCollector::put_Enabled, InkCollector.get_Enabled, InkCollector.put_Enabled, ab55a399-1990-4cfc-a4ab-834a5db8d7a9, get_Enabled, msinkaut/IInkCollector::Enabled, msinkaut/IInkCollector::get_Enabled, msinkaut/IInkCollector::put_Enabled, put_Enabled, tablet.inkcollector_enabled
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
 - IInkCollector::get_Enabled
 - msinkaut/IInkCollector::get_Enabled
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
 - IInkCollector.Enabled
 - IInkCollector.get_Enabled
 - IInkCollector.put_Enabled
 - put_Enabled
 - IInkCollector.put_Enabled
 - InkCollector.get_Enabled
 - InkCollector.put_Enabled
---

# IInkCollector::get_Enabled


## -description

Gets or sets  a value that specifies whether the <a href="/windows/desktop/tablet/inkcollector-class">InkCollector</a> object collects pen input (in-air packets, cursor in range events, and so on).



This property is read/write.

## -parameters

## -remarks

If an enabled object's window input rectangle (set in the constructor or with the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setwindowinputrectangle">SetWindowInputRectangle</a> method) of an enabled object overlaps the window input rectangle of another enabled object, the E_INK_OVERLAPPING_INPUT_RECT error is returned. Overlap can occur without an error as long as only one of the input rectangles is enabled at any known time.

While an object is not enabled, you receive no events.

When a container control has its <b>Enabled</b> property set to <b>FALSE</b>, all of its contained controls are disabled as well.

You cannot set the <b>Enabled</b> property to <b>FALSE</b> while the object is collecting ink (<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectingink">CollectingInk</a> property is <b>TRUE</b>).

We recommend that you set <b>Enabled</b> set to <b>FALSE</b> when the application shuts down.

<div class="alert"><b>Note</b>  Setting this property within certain message handlers can result in the underlying function being re-entered, causing unexpected results. Take care to avoid a reentrant call when handling any of the following messages: <b>WM_ACTIVATE</b>, <b>WM_ACTIVATEAPP</b>, <b>WM_NCACTIVATE</b>, <b>WM_PAINT</b>; <b>WM_SYSCOMMAND</b> if <i>wParam</i> is set to SC_HOTKEY or SC_TASKLIST; and <b>WM_SYSKEYDOWN</b> (when processing Alt-Tab or Alt-Esc key combinations). This is an issue with single-threaded apartment model applications.</div>
<div> </div>
This property must be set to <b>FALSE</b> before setting or calling specific properties and methods of the object. If you try to change the specified properties or methods, an error occurs. The following properties and methods cannot be set or called unless the <b>Enabled</b> property is first set to <b>FALSE</b>:

Properties

<ul>
<li>
<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_attachmode">AttachMode</a>
</li>
<li>
<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_hwnd">hWnd</a>
</li>
<li>
<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink">Ink</a>
</li>
<li>
<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_marginx">MarginX</a>
</li>
<li>
<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_marginy">MarginY</a>
</li>
</ul>
Methods

<ul>
<li>
<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setalltabletsmode">SetAllTabletsMode</a>
</li>
<li>
<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setsingletabletintegratedmode">SetSingleTabletIntegratedMode</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_attachmode">AttachMode Property</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectingink">CollectingInk Property</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode">CollectionMode Property [InkCollector Class]</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode">EditingMode Property [InkOverlay Class]</a>



<a href="../msinkaut/nn-msinkaut-iinkcollector.md">IInkCollector</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink">Ink Property [InkCollector/InkOverLay Class]</a>



<a href="/windows/desktop/tablet/inkcollector-class">InkCollector Class</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_marginx">MarginX Property</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_marginy">MarginY Property</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setalltabletsmode">SetAllTabletsMode Method</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setsingletabletintegratedmode">SetSingleTabletIntegratedMode Method</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setwindowinputrectangle">SetWindowInputRectangle Method</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_hwnd">hWnd Property</a>
