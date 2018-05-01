---
UID: NN:rtscom.IStylusAsyncPlugin
title: IStylusAsyncPlugin
author: windows-driver-content
description: Represents an asynchronous plug-in that can be added to the asynchronous plug-in collection of the RealTimeStylus Class object.
old-location: tablet\istylusasyncplugin.htm
old-project: tablet
ms.assetid: bf961d70-2576-493b-a34d-c7c72b6c0234
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: IStylusAsyncPlugin, IStylusAsyncPlugin interface [Tablet PC], IStylusAsyncPlugin interface [Tablet PC], described, bf961d70-2576-493b-a34d-c7c72b6c0234, rtscom/IStylusAsyncPlugin, tablet.istylusasyncplugin
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
-	IStylusAsyncPlugin
product: Windows
targetos: Windows
req.lib: 
req.dll: RTSCom.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IStylusAsyncPlugin interface


## -description



Represents an asynchronous plug-in that can be added to the asynchronous plug-in collection of the <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> object.




## -remarks



This is the asynchronous version of <a href="https://msdn.microsoft.com/bbef5cdb-4112-4733-80bb-692b7a198605">IStylusPlugin Interface</a>.

This plug-in receives notifications of <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> events enabling you to do custom processing.

The <a href="https://msdn.microsoft.com/7cdaf3bf-7aae-4d36-af1c-0eb5a726f388">GestureRecognizer Class</a> is an example of a plug-in that implements the <b>IStylusAsyncPlugin</b> interface in order to respond in a timely fashion to the stylus. In some circumstances, such as when large numbers of gestures are subscribed to, the response time in the gesture recognizer becomes excessively slow. To avoid this problem, the <b>GestureRecognizer Class</b> implements the <b>IStylusAsyncPlugin</b> interface so that it can be called asynchronously.




## -see-also




<a href="https://msdn.microsoft.com/938e1eb2-3dd4-4e21-9c46-9ef840172b05">DynamicRenderer Class</a>



<a href="https://msdn.microsoft.com/7cdaf3bf-7aae-4d36-af1c-0eb5a726f388">GestureRecognizer Class</a>



<a href="https://msdn.microsoft.com/bbef5cdb-4112-4733-80bb-692b7a198605">IStylusPlugin</a>



<a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a>



<a href="https://msdn.microsoft.com/fc0900b4-f08b-4a93-bbc0-d3db067d7917">RealTimeStylus Classes and Interfaces</a>
 

 

