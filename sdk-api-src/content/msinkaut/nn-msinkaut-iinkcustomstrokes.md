---
UID: NN:msinkaut.IInkCustomStrokes
title: IInkCustomStrokes (msinkaut.h)
description: Contains a collection of user-defined InkStrokes collections.
helpviewer_keywords: ["0b4eb5d6-ccf0-46c1-ae02-a393e67b817e","IInkCustomStrokes","IInkCustomStrokes interface [Tablet PC]","IInkCustomStrokes interface [Tablet PC]","described","msinkaut/IInkCustomStrokes","tablet.iinkcustomstrokes"]
old-location: tablet\iinkcustomstrokes.htm
tech.root: tablet
ms.assetid: 0b4eb5d6-ccf0-46c1-ae02-a393e67b817e
ms.date: 12/05/2018
ms.keywords: 0b4eb5d6-ccf0-46c1-ae02-a393e67b817e, IInkCustomStrokes, IInkCustomStrokes interface [Tablet PC], IInkCustomStrokes interface [Tablet PC],described, msinkaut/IInkCustomStrokes, tablet.iinkcustomstrokes
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
 - IInkCustomStrokes
 - msinkaut/IInkCustomStrokes
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
 - IInkCustomStrokes
 - IInkCustomStrokes._NewEnum
---

# IInkCustomStrokes interface


## -description

Contains a collection of user-defined <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collections.

## -inheritance

The <b>IInkCustomStrokes</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IInkCustomStrokes</b> also has these types of members:

## -remarks

The custom strokes are essentially named <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collections that are persisted and recalled for later use.

You use a collection of custom strokes to store strokes that have the same meaning or that are related in some way. Examples of strokes that you may want to persist include:

<ul>
<li>All the strokes drawn by the same cursor (pen)</li>
<li>The strokes in an <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object that correspond to a word or paragraph</li>
<li>All the strokes that intersect a known region</li>
</ul>
For example, suppose you want to draw with two different cursors and keep separate the set of strokes that you draw with each cursor. You could recognize the strokes drawn with the first cursor and attach an <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult">IInkRecognitionResult</a> object to that collection of strokes. To persist the recognition result, add the strokes to the <b>CustomStrokes</b> collection of the <a href="/windows/desktop/tablet/inkdisp-class">InkDisp</a> object. You can later access the first collection of strokes by getting the persisted <b>CustomStrokes</b> collection from the <b>InkDisp</b> object.

Each <b>IInkCustomStrokes</b> collection is referenced by name.

<b>IInkCustomStrokes</b> collections are references to ink data, not the actual data itself.

For more information about collections in COM, see <a href="/windows/desktop/tablet/using-the-com-library">Using the COM Library</a>.

If you define a class that implements this interface, the new class will not interact correctly with the Tablet PC application programming interfaces (APIs).

## -see-also

<a href="/windows/desktop/tablet/inkdisp-class">InkDisp Class</a>



<a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes Collection</a>
