---
UID: NF:msinkaut.IInkPicture.get_Cursors
title: IInkPicture::get_Cursors (msinkaut.h)
description: Gets the collection of cursors that are available for use in the inking region. Each cursor corresponds to the tip of a pen or other ink input device.
helpviewer_keywords: ["Cursors property [Tablet PC]","Cursors property [Tablet PC]","IInkPicture interface","IInkPicture interface [Tablet PC]","Cursors property","IInkPicture.Cursors","IInkPicture.get_Cursors","IInkPicture::Cursors","IInkPicture::get_Cursors","InkPicture.get_Cursors","get_Cursors","msinkaut/IInkPicture::Cursors","msinkaut/IInkPicture::get_Cursors","tablet.inkpicture_cursors"]
old-location: tablet\inkpicture_cursors.htm
tech.root: tablet
ms.assetid: 815f4895-d418-4336-9420-2405bcd5cfb3
ms.date: 12/05/2018
ms.keywords: Cursors property [Tablet PC], Cursors property [Tablet PC],IInkPicture interface, IInkPicture interface [Tablet PC],Cursors property, IInkPicture.Cursors, IInkPicture.get_Cursors, IInkPicture::Cursors, IInkPicture::get_Cursors, InkPicture.get_Cursors, get_Cursors, msinkaut/IInkPicture::Cursors, msinkaut/IInkPicture::get_Cursors, tablet.inkpicture_cursors
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
 - IInkPicture::get_Cursors
 - msinkaut/IInkPicture::get_Cursors
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
 - IInkPicture.Cursors
 - IInkPicture.get_Cursors
 - InkPicture.get_Cursors
---

# IInkPicture::get_Cursors


## -description

Gets the collection of cursors that are available for use in the inking region. Each cursor corresponds to the tip of a pen or other ink input device.



This property is read-only.

## -parameters

## -remarks

Cursors are local to an <a href="/windows/desktop/tablet/inkcollector-class">InkCollector</a> object.

Any new cursors that the <a href="/windows/desktop/tablet/inkcollector-class">InkCollector</a> encounters are added to the returned collection of cursors, although the returned cursors are not necessarily returned in the order in which the <b>InkCollector</b> encounters them.

When a mouse is enabled as an input device on the <a href="/windows/desktop/tablet/inkcollector-class">InkCollector</a> (when the <i>useMouse</i> parameter of the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setalltabletsmode">SetAllTabletsMode</a> method is <b>TRUE</b>), the mouse is added to the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursors">IInkCursors</a> collection after the <b>InkCollector</b> encounters any other cursor, such as a pen. This is because the pen also acts like a mouse.

<div class="alert"><b>Note</b>  The <a href="/windows/desktop/tablet/inkpicture-cursorinrange">CursorInRange</a> event is received for the mouse cursor after any other cursor, such as a pen, draws a stroke (which fires the <a href="/windows/desktop/tablet/inkpicture-stroke">Stroke</a> event).</div>
<div> </div>
The <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursors">IInkCursors</a> collection is reset (count set to 0, containing no objects) when:

<ul>
<li>The tablet mode is changed (for example, from <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setsingletabletintegratedmode">SetSingleTabletIntegratedMode</a> to <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setalltabletsmode">SetAllTabletsMode</a>).</li>
<li>The <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setsingletabletintegratedmode">SetSingleTabletIntegratedMode</a> method is called.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursors">IInkCursors Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt846800(v=VS.85).aspx">IInkPicture</a>



<a href="/windows/desktop/tablet/inkpicture-control">InkPicture Control</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_mouseicon">MouseIcon Property</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_mousepointer">MousePointer Property</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setalltabletsmode">SetAllTabletsMode Method</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setsingletabletintegratedmode">SetSingleTabletIntegratedMode Method</a>