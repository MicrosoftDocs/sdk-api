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

# IInkPicture::get_Cursors


## -description



Gets the collection of cursors that are available for use in the inking region. Each cursor corresponds to the tip of a pen or other ink input device.



This property is read-only.


## -parameters


## -remarks



Cursors are local to an <a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector</a> object.

Any new cursors that the <a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector</a> encounters are added to the returned collection of cursors, although the returned cursors are not necessarily returned in the order in which the <b>InkCollector</b> encounters them.

When a mouse is enabled as an input device on the <a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector</a> (when the <i>useMouse</i> parameter of the <a href="https://msdn.microsoft.com/30e8c0d3-6cae-476b-8fc5-f0d97b4b16f4">SetAllTabletsMode</a> method is <b>TRUE</b>), the mouse is added to the <a href="https://msdn.microsoft.com/3ae7dbc4-e5a2-4916-a1cc-651659a008fc">IInkCursors</a> collection after the <b>InkCollector</b> encounters any other cursor, such as a pen. This is because the pen also acts like a mouse.

<div class="alert"><b>Note</b>  The <a href="https://msdn.microsoft.com/e921e175-a2cf-45e6-bb81-dc82e384d3b1">CursorInRange</a> event is received for the mouse cursor after any other cursor, such as a pen, draws a stroke (which fires the <a href="https://msdn.microsoft.com/2829b65a-6120-402e-91e3-5587d1f456f9">Stroke</a> event).</div>
<div> </div>
The <a href="https://msdn.microsoft.com/3ae7dbc4-e5a2-4916-a1cc-651659a008fc">IInkCursors</a> collection is reset (count set to 0, containing no objects) when:

<ul>
<li>The tablet mode is changed (for example, from <a href="https://msdn.microsoft.com/b611a078-b38e-4f9b-834f-9a2aa9684931">SetSingleTabletIntegratedMode</a> to <a href="https://msdn.microsoft.com/30e8c0d3-6cae-476b-8fc5-f0d97b4b16f4">SetAllTabletsMode</a>).</li>
<li>The <a href="https://msdn.microsoft.com/b611a078-b38e-4f9b-834f-9a2aa9684931">SetSingleTabletIntegratedMode</a> method is called.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/3ae7dbc4-e5a2-4916-a1cc-651659a008fc">IInkCursors Interface</a>



<a href="tablet.iinkpicture">IInkPicture</a>



<a href="https://msdn.microsoft.com/1ced9779-dae5-4f9a-8a68-b2c0d041d5b4">InkPicture Control</a>



<a href="https://msdn.microsoft.com/a095dca7-4dc9-4661-8c78-0e357a57f982">MouseIcon Property</a>



<a href="https://msdn.microsoft.com/94536770-01ef-41c5-9217-0aa2ef9c36ac">MousePointer Property</a>



<a href="https://msdn.microsoft.com/30e8c0d3-6cae-476b-8fc5-f0d97b4b16f4">SetAllTabletsMode Method</a>



<a href="https://msdn.microsoft.com/b611a078-b38e-4f9b-834f-9a2aa9684931">SetSingleTabletIntegratedMode Method</a>
 

 

