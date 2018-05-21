---
UID: NF:rtscom.IRealTimeStylus.get_WindowInputRectangle
title: IRealTimeStylus::get_WindowInputRectangle
author: windows-driver-content
description: Gets or sets the window input rectangle for the RealTimeStylus Class object.
old-location: tablet\irealtimestylus_windowinputrectangle.htm
old-project: tablet
ms.assetid: e202be43-48c7-4fa4-b049-efdda3ef2ada
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: IRealTimeStylus interface [Tablet PC],WindowInputRectangle property, IRealTimeStylus.WindowInputRectangle, IRealTimeStylus.get_WindowInputRectangle, IRealTimeStylus.put_WindowInputRectangle, IRealTimeStylus::WindowInputRectangle, IRealTimeStylus::get_WindowInputRectangle, IRealTimeStylus::put_WindowInputRectangle, WindowInputRectangle property [Tablet PC], WindowInputRectangle property [Tablet PC],IRealTimeStylus interface, e202be43-48c7-4fa4-b049-efdda3ef2ada, get_WindowInputRectangle, rtscom/IRealTimeStylus::WindowInputRectangle, rtscom/IRealTimeStylus::get_WindowInputRectangle, rtscom/IRealTimeStylus::put_WindowInputRectangle, tablet.irealtimestylus_windowinputrectangle
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: rtscom.h
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
req.typenames: StylusQueue
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	RTSCom.dll
api_name:
-	IRealTimeStylus.WindowInputRectangle
-	IRealTimeStylus.get_WindowInputRectangle
-	IRealTimeStylus.put_WindowInputRectangle
-	IRealTimeStylus.get_WindowInputRectangle
-	IRealTimeStylus.put_WindowInputRectangle
product: Windows
targetos: Windows
req.lib: 
req.dll: RTSCom.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IRealTimeStylus::get_WindowInputRectangle


## -description



Gets or sets the window input rectangle for the <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> object.



This property is read/write.


## -parameters


## -remarks



Each <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> object receives tablet pen data for specific section of a window based on the defined window input rectangle for that <b>RealTimeStylus Class</b> object.

The default value is an empty window input rectangle, <b>IRealTimeStylus::WindowInputRectangle Property</b>, value. When the <b>IRealTimeStylus::WindowInputRectangle Property</b> value is empty, {0, 0, 0, 0}, the <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> object collects pen input over the entire window, even after the window is resized.

After the <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> object starts collecting pen data, it continues to collect the data until the pen is raised, even if the pen is moved outside of the input region.

Use either an attached <a href="https://msdn.microsoft.com/e3e02d5a-a004-49de-b2d8-86ccfc120481">IStylusSyncPlugin</a> object or the attached <a href="https://msdn.microsoft.com/bf961d70-2576-493b-a34d-c7c72b6c0234">IStylusAsyncPlugin</a> object to uniquely handle pen data that is collected outside of the input region.

The E_INVALIDOPERATION HRESULT is returned when you attempt to set this property on a child <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> object.




## -see-also




<a href="https://msdn.microsoft.com/bfd13012-decf-423a-bc1a-39fb9b0eb64e">IRealTimeStylus</a>



<a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a>



<a href="https://msdn.microsoft.com/a239b53c-7fc9-4211-962a-6cfbe0be4e4c">RealTimeStylus Reference</a>
 

 

