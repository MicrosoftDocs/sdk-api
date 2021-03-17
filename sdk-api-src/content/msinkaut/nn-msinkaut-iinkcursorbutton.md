---
UID: NN:msinkaut.IInkCursorButton
title: IInkCursorButton (msinkaut.h)
description: Represents general information about a button on a tablet pointing and selecting device.
helpviewer_keywords: ["06b91ab0-b2fb-4a09-8a2b-615da87ec4a2","IInkCursorButton","IInkCursorButton interface [Tablet PC]","IInkCursorButton interface [Tablet PC]","described","msinkaut/IInkCursorButton","tablet.iinkcursorbutton"]
old-location: tablet\iinkcursorbutton.htm
tech.root: tablet
ms.assetid: 06b91ab0-b2fb-4a09-8a2b-615da87ec4a2
ms.date: 12/05/2018
ms.keywords: 06b91ab0-b2fb-4a09-8a2b-615da87ec4a2, IInkCursorButton, IInkCursorButton interface [Tablet PC], IInkCursorButton interface [Tablet PC],described, msinkaut/IInkCursorButton, tablet.iinkcursorbutton
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
 - IInkCursorButton
 - msinkaut/IInkCursorButton
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
 - IInkCursorButton
---

# IInkCursorButton interface


## -description

Represents general information about a button on a tablet pointing and selecting device.

## -remarks

An <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor">IInkCursor</a> can contain zero to 32 associated buttons, and these buttons are provided to an application as <b>IInkCursorButton</b> objects. Examples of cursor buttons are:

<ul>
<li>The writing end of a pen</li>
<li>The inverted (or "eraser") end of a pen</li>
<li>The barrel of a pen</li>
<li>The button on a pen</li>
</ul>
A single pen cursor with no barrel may consist of two cursor buttons: the writing end and the inverted end. Each button can have a specific function, and an application must know which button, by identifier, is being used before it can accept input from the cursor. For example, an application must know the identifier of the inverted end of the pen before strokes can be erased.

If you define a class that implements this interface, the new class will not interact correctly with the Tablet PC application programming interfaces (APIs).

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_buttons">Buttons Property</a>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor">IInkCursor Interface</a>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbuttons">IInkCursorButtons Interface</a>