---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IInkOverlay::get_Cursors


## -description



Gets the collection of cursors that are available for use in the inking region. Each cursor corresponds to the tip of a pen or other ink input device.



This property is read-only.


## -parameters


## -remarks



Cursors are local to an <a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector</a> object.

Any new cursors that the <a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector</a> encounters are added to the returned collection of cursors, although the returned cursors are not necessarily returned in the order in which the <b>InkCollector</b> encounters them.

When a mouse is enabled as an input device on the <a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector</a> (when the <i>useMouse</i> parameter of the <a href="https://msdn.microsoft.com/cb41bc4c-c8fe-4cd6-8049-8cb44a2716a8">SetAllTabletsMode</a> method is <b>TRUE</b>), the mouse is added to the <a href="https://msdn.microsoft.com/3ae7dbc4-e5a2-4916-a1cc-651659a008fc">IInkCursors</a> collection after the <b>InkCollector</b> encounters any other cursor, such as a pen. This is because the pen also acts like a mouse.

<div class="alert"><b>Note</b>  The <a href="https://msdn.microsoft.com/d05b240c-ba64-4008-b25d-e06c052eb5b0">CursorInRange</a> event is received for the mouse cursor after any other cursor, such as a pen, draws a stroke (which fires the <a href="https://msdn.microsoft.com/eaa89dfe-6141-4205-845b-634321130e26">Stroke</a> event).</div>
<div> </div>
The <a href="https://msdn.microsoft.com/3ae7dbc4-e5a2-4916-a1cc-651659a008fc">IInkCursors</a> collection is reset (count set to 0, containing no objects) when:

<ul>
<li>The tablet mode is changed (for example, from <a href="https://msdn.microsoft.com/96787996-c0fd-455f-952e-90ddc8640253">SetSingleTabletIntegratedMode</a> to <a href="https://msdn.microsoft.com/cb41bc4c-c8fe-4cd6-8049-8cb44a2716a8">SetAllTabletsMode</a>).</li>
<li>The <a href="https://msdn.microsoft.com/96787996-c0fd-455f-952e-90ddc8640253">SetSingleTabletIntegratedMode</a> method is called.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/3ae7dbc4-e5a2-4916-a1cc-651659a008fc">IInkCursors Interface</a>



<a href="tablet.iinkoverlay">IInkOverlay</a>



<a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay Class</a>



<a href="https://msdn.microsoft.com/9c7f879a-1b6c-4bd0-8dc1-82f23ace57c4">MouseIcon Property</a>



<a href="https://msdn.microsoft.com/8876b0ef-1a61-481b-ac37-9e4d637f8097">MousePointer Property</a>



<a href="https://msdn.microsoft.com/cb41bc4c-c8fe-4cd6-8049-8cb44a2716a8">SetAllTabletsMode Method</a>



<a href="https://msdn.microsoft.com/96787996-c0fd-455f-952e-90ddc8640253">SetSingleTabletIntegratedMode Method</a>
 

 

