---
UID: NN:msinkaut.IInkCursor
title: IInkCursor (msinkaut.h)
description: Represents general information about the tablet cursor.
helpviewer_keywords: ["39b365ad-1eb0-4183-8799-a3c3ecbd3f6e","IInkCursor","IInkCursor interface [Tablet PC]","IInkCursor interface [Tablet PC]","described","msinkaut/IInkCursor","tablet.iinkcursor"]
old-location: tablet\iinkcursor.htm
tech.root: tablet
ms.assetid: 39b365ad-1eb0-4183-8799-a3c3ecbd3f6e
ms.date: 12/05/2018
ms.keywords: 39b365ad-1eb0-4183-8799-a3c3ecbd3f6e, IInkCursor, IInkCursor interface [Tablet PC], IInkCursor interface [Tablet PC],described, msinkaut/IInkCursor, tablet.iinkcursor
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
 - IInkCursor
 - msinkaut/IInkCursor
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
 - IInkCursor
---

# IInkCursor interface


## -description

Represents general information about the tablet cursor.

## -remarks

An <b>IInkCursor</b> object represents the physical pen that the user holds. Physical pens may have multiple tips - such as normal and eraser ends - with each pen tip representing a different <b>IInkCursor</b> object. Some Tablet PCs allow multiple pens. Each cursor has an associated identifier that is unique on a system. For more information about how pens can be used with Tablet PC, see <a href="/windows/desktop/tablet/pen-input--ink--and-recognition">Pen Input, Ink, and Recognition</a>.

A specific set of drawing attributes can be assigned to a known cursor, such as whether the pen color should be red or blue. A cursor also contains a collection of zero or more <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton">IInkCursorButton</a> objects.

Cursors exist only within the scope of an <a href="/windows/desktop/tablet/inkcollector-class">InkCollector</a> object, an <a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay</a> object, or an <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> control. When one of these objects encounters a new cursor, the object fires its <a href="/windows/desktop/tablet/inkcollector-cursorinrange">CursorInRange</a> event with the <i>newCursor</i> parameter set to <b>TRUE</b>. This allows you to set up properties in the application, such as drawing attributes, when the cursor is first encountered. The <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_cursors">Cursors</a> property contains the collection of cursors that the object or control has encountered.

An <b>IInkCursor</b> cannot be constructed explicitly. Instead, you obtain an <b>IInkCursor</b> from either events or the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_cursors">Cursors</a> property of an <a href="/windows/desktop/tablet/inkcollector-class">InkCollector</a> object, an <a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay</a> object, or an <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> control.

If you define a class that implements this interface, the new class will not interact correctly with the Tablet PC application programming interfaces (APIs).

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_cursors">Cursors Property</a>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton">IInkCursorButton Interface</a>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbuttons">IInkCursorButtons Interface</a>



<b>IInkCursors Interface</b>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet">IInkTablet Interface</a>



<a href="/windows/desktop/tablet/inkcollector-class">InkCollector Class</a>



<a href="/windows/desktop/tablet/inkdrawingattributes-class">InkDrawingAttributes Class</a>



<a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay Class</a>



<a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture Control Reference</a>