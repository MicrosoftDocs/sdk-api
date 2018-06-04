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

# IInkCursor interface


## -description



Represents general information about the tablet cursor.




## -remarks



An <b>IInkCursor</b> object represents the physical pen that the user holds. Physical pens may have multiple tips - such as normal and eraser ends - with each pen tip representing a different <b>IInkCursor</b> object. Some Tablet PCs allow multiple pens. Each cursor has an associated identifier that is unique on a system. For more information about how pens can be used with Tablet PC, see <a href="https://msdn.microsoft.com/8432617a-5ae7-44cb-a5f7-f3b2d8885846">Pen Input, Ink, and Recognition</a>.

A specific set of drawing attributes can be assigned to a known cursor, such as whether the pen color should be red or blue. A cursor also contains a collection of zero or more <a href="https://msdn.microsoft.com/06b91ab0-b2fb-4a09-8a2b-615da87ec4a2">IInkCursorButton</a> objects.

Cursors exist only within the scope of an <a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector</a> object, an <a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay</a> object, or an <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a> control. When one of these objects encounters a new cursor, the object fires its <a href="https://msdn.microsoft.com/d05b240c-ba64-4008-b25d-e06c052eb5b0">CursorInRange</a> event with the <i>newCursor</i> parameter set to <b>TRUE</b>. This allows you to set up properties in the application, such as drawing attributes, when the cursor is first encountered. The <a href="https://msdn.microsoft.com/6a939fd0-1e0c-4df6-bcd0-b58fb7bac5e4">Cursors</a> property contains the collection of cursors that the object or control has encountered.

An <b>IInkCursor</b> cannot be constructed explicitly. Instead, you obtain an <b>IInkCursor</b> from either events or the <a href="https://msdn.microsoft.com/6a939fd0-1e0c-4df6-bcd0-b58fb7bac5e4">Cursors</a> property of an <a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector</a> object, an <a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay</a> object, or an <a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture</a> control.

If you define a class that implements this interface, the new class will not interact correctly with the Tablet PC application programming interfaces (APIs).




## -see-also




<a href="https://msdn.microsoft.com/6a939fd0-1e0c-4df6-bcd0-b58fb7bac5e4">Cursors Property</a>



<a href="https://msdn.microsoft.com/06b91ab0-b2fb-4a09-8a2b-615da87ec4a2">IInkCursorButton Interface</a>



<a href="https://msdn.microsoft.com/3f695ab4-8174-402f-b7d6-810f149f5153">IInkCursorButtons Interface</a>



<b>IInkCursors Interface</b>



<a href="https://msdn.microsoft.com/9a945740-b191-41f5-8b3d-49b7e2d1e463">IInkTablet Interface</a>



<a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector Class</a>



<a href="https://msdn.microsoft.com/10ca7ae5-28dd-42a2-98d9-852d4de5869d">InkDrawingAttributes Class</a>



<a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay Class</a>



<a href="https://msdn.microsoft.com/e9fa6807-6e2a-44ec-9b8f-a560185e4367">InkPicture Control Reference</a>
 

 

