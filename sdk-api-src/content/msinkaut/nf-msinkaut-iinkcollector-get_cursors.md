---
UID: NF:msinkaut.IInkCollector.get_Cursors
title: IInkCollector::get_Cursors (msinkaut.h)
description: Gets the collection of cursors that are available for use in the inking region. Each cursor corresponds to the tip of a pen or other ink input device. (IInkCollector.get_Cursors)
helpviewer_keywords: ["6a939fd0-1e0c-4df6-bcd0-b58fb7bac5e4","Cursors property [Tablet PC]","Cursors property [Tablet PC]","IInkCollector interface","IInkCollector interface [Tablet PC]","Cursors property","IInkCollector.Cursors","IInkCollector.get_Cursors","IInkCollector::Cursors","IInkCollector::get_Cursors","InkCollector.get_Cursors","get_Cursors","msinkaut/IInkCollector::Cursors","msinkaut/IInkCollector::get_Cursors","put_Cursors","tablet.inkcollector_cursors"]
old-location: tablet\inkcollector_cursors.htm
tech.root: tablet
ms.assetid: 6a939fd0-1e0c-4df6-bcd0-b58fb7bac5e4
ms.date: 12/05/2018
ms.keywords: 6a939fd0-1e0c-4df6-bcd0-b58fb7bac5e4, Cursors property [Tablet PC], Cursors property [Tablet PC],IInkCollector interface, IInkCollector interface [Tablet PC],Cursors property, IInkCollector.Cursors, IInkCollector.get_Cursors, IInkCollector::Cursors, IInkCollector::get_Cursors, InkCollector.get_Cursors, get_Cursors, msinkaut/IInkCollector::Cursors, msinkaut/IInkCollector::get_Cursors, put_Cursors, tablet.inkcollector_cursors
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
 - IInkCollector::get_Cursors
 - msinkaut/IInkCollector::get_Cursors
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
 - IInkCollector.Cursors
 - IInkCollector.get_Cursors
 - InkCollector.get_Cursors
---

# IInkCollector::get_Cursors


## -description

Gets the collection of cursors that are available for use in the inking region. Each cursor corresponds to the tip of a pen or other ink input device.



This property is read-only.

## -parameters

## -remarks

Cursors are local to an <a href="/windows/desktop/tablet/inkcollector-class">InkCollector</a> object.

Any new cursors that the <a href="/windows/desktop/tablet/inkcollector-class">InkCollector</a> encounters are added to the returned collection of cursors, although the returned cursors are not necessarily returned in the order in which the <b>InkCollector</b> encounters them.

When a mouse is enabled as an input device on the <a href="/windows/desktop/tablet/inkcollector-class">InkCollector</a> (when the <i>useMouse</i> parameter of the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setalltabletsmode">SetAllTabletsMode</a> method is <b>TRUE</b>), the mouse is added to the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursors">IInkCursors</a> collection after the <b>InkCollector</b> encounters any other cursor, such as a pen. This is because the pen also acts like a mouse.

<div class="alert"><b>Note</b>  The <a href="/windows/desktop/tablet/inkcollector-cursorinrange">CursorInRange</a> event is received for the mouse cursor after any other cursor, such as a pen, draws a stroke (which fires the <a href="/windows/desktop/tablet/inkcollector-stroke">Stroke</a> event).</div>
<div> </div>
The <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursors">IInkCursors</a> collection is reset (count set to 0, containing no objects) when:

<ul>
<li>The tablet mode is changed (for example, from <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setsingletabletintegratedmode">SetSingleTabletIntegratedMode</a> to <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setalltabletsmode">SetAllTabletsMode</a>).</li>
<li>The <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setsingletabletintegratedmode">SetSingleTabletIntegratedMode</a> method is called.</li>
</ul>

## -see-also

<a href="../msinkaut/nn-msinkaut-iinkcollector.md">IInkCollector</a>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursors">IInkCursors Interface</a>



<a href="/windows/desktop/tablet/inkcollector-class">InkCollector Class</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mouseicon">MouseIcon Property</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mousepointer">MousePointer Property</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setalltabletsmode">SetAllTabletsMode Method</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setsingletabletintegratedmode">SetSingleTabletIntegratedMode Method</a>
