---
UID: NN:msinkaut.IInkCursors
title: IInkCursors (msinkaut.h)
description: Represents a collection of IInkCursor objects.
helpviewer_keywords: ["3ae7dbc4-e5a2-4916-a1cc-651659a008fc","IInkCursors","IInkCursors interface [Tablet PC]","IInkCursors interface [Tablet PC]","described","msinkaut/IInkCursors","tablet.iinkcursors"]
old-location: tablet\iinkcursors.htm
tech.root: tablet
ms.assetid: 3ae7dbc4-e5a2-4916-a1cc-651659a008fc
ms.date: 12/05/2018
ms.keywords: 3ae7dbc4-e5a2-4916-a1cc-651659a008fc, IInkCursors, IInkCursors interface [Tablet PC], IInkCursors interface [Tablet PC],described, msinkaut/IInkCursors, tablet.iinkcursors
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
 - IInkCursors
 - msinkaut/IInkCursors
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
 - IInkCursors
 - IInkCursors._NewEnum
---

# IInkCursors interface


## -description

Represents a collection of <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor">IInkCursor</a> objects.

## -inheritance

The <b>IInkCursors</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IInkCursors</b> also has these types of members:

## -remarks

A cursor becomes part of the cursors collection of an <a href="/windows/desktop/tablet/inkcollector-class">InkCollector</a> object, <a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay</a> object, or the <a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture</a> control when it comes within range of the object. Each time a new cursor comes within range, it is added to the object's cursors collection. The cursors collection exists only during the lifetime of that object.

For example, if a pen is used to draw ink on an <a href="/windows/desktop/tablet/inkcollector-class">InkCollector</a> object, it becomes part of the <b>InkCollector</b> object's <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_cursors">Cursors</a> property. If a mouse is then used for input on the same <b>InkCollector</b> object, it is also added to the collection.

You can use this collection to enumerate over all of the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor">IInkCursor</a> objects on a known <a href="/windows/desktop/tablet/inkcollector-class">InkCollector</a> object.

For more information about collections in COM, see <a href="/windows/desktop/tablet/using-the-com-library">Using the COM Library</a>.

If you define a class that implements this interface, the new class will not interact correctly with the Tablet PC application programming interfaces (APIs).

## -see-also

<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor">IInkCursor Interface</a>



<a href="/windows/desktop/tablet/inkcollector-class">InkCollector Class</a>



<a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay Class</a>



<a href="/windows/desktop/tablet/inkpicture-control-reference">InkPicture Control Reference</a>
