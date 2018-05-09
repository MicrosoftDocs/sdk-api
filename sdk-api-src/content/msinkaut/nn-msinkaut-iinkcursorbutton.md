---
UID: NN:msinkaut.IInkCursorButton
title: IInkCursorButton
author: windows-driver-content
description: Represents general information about a button on a tablet pointing and selecting device.
old-location: tablet\iinkcursorbutton.htm
old-project: tablet
ms.assetid: 06b91ab0-b2fb-4a09-8a2b-615da87ec4a2
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: 06b91ab0-b2fb-4a09-8a2b-615da87ec4a2, IInkCursorButton, IInkCursorButton interface [Tablet PC], IInkCursorButton interface [Tablet PC],described, msinkaut/IInkCursorButton, tablet.iinkcursorbutton
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: TabletPropertyMetricUnit
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	InkObj.dll
-	InkObj.dll.dll
api_name:
-	IInkCursorButton
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IInkCursorButton interface


## -description



Represents general information about a button on a tablet pointing and selecting device.




## -remarks



An <a href="https://msdn.microsoft.com/39b365ad-1eb0-4183-8799-a3c3ecbd3f6e">IInkCursor</a> can contain zero to 32 associated buttons, and these buttons are provided to an application as <b>IInkCursorButton</b> objects. Examples of cursor buttons are:

<ul>
<li>The writing end of a pen</li>
<li>The inverted (or "eraser") end of a pen</li>
<li>The barrel of a pen</li>
<li>The button on a pen</li>
</ul>
A single pen cursor with no barrel may consist of two cursor buttons: the writing end and the inverted end. Each button can have a specific function, and an application must know which button, by identifier, is being used before it can accept input from the cursor. For example, an application must know the identifier of the inverted end of the pen before strokes can be erased.

If you define a class that implements this interface, the new class will not interact correctly with the Tablet PC application programming interfaces (APIs).




## -see-also




<a href="https://msdn.microsoft.com/21ea5b71-390e-448f-becc-1e3bb7015ed9">Buttons Property</a>



<a href="https://msdn.microsoft.com/39b365ad-1eb0-4183-8799-a3c3ecbd3f6e">IInkCursor Interface</a>



<a href="https://msdn.microsoft.com/3f695ab4-8174-402f-b7d6-810f149f5153">IInkCursorButtons Interface</a>
 

 

