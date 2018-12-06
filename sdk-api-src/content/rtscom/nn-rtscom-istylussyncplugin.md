---
UID: NN:rtscom.IStylusSyncPlugin
title: IStylusSyncPlugin
author: windows-sdk-content
description: Represents a synchronous plug-in that can be added to the RealTimeStylus Class object's synchronous plug-in collection.
old-location: tablet\istylussyncplugin.htm
tech.root: tablet
ms.assetid: e3e02d5a-a004-49de-b2d8-86ccfc120481
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IStylusSyncPlugin, IStylusSyncPlugin interface [Tablet PC], IStylusSyncPlugin interface [Tablet PC],described, e3e02d5a-a004-49de-b2d8-86ccfc120481, rtscom/IStylusSyncPlugin, tablet.istylussyncplugin
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
req.lib: 
req.dll: RTSCom.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RTSCom.dll
api_name:
 - IStylusSyncPlugin
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IStylusSyncPlugin interface


## -description



Represents a synchronous plug-in that can be added to the <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> object's synchronous plug-in collection.




## -remarks



This is the synchronous version of <a href="https://msdn.microsoft.com/bbef5cdb-4112-4733-80bb-692b7a198605">IStylusPlugin Interface</a>. It provides for strong type checking in the synchronous plug-in collections.

This plug-in receives notifications of <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> events enabling you to do custom processing.

The dynamic renderer and gesture recognizer are examples of plug-ins which implement the <b>IStylusSyncPlugin</b> interface. The dynamic renderer implements the <b>IStylusSyncPlugin</b> interface in order to respond in a timely fashion to the stylus.

In some circumstances, such as when large numbers of gestures are subscribed to, the response time in the gesture recognizer becomes excessively slow. To avoid this problem, the gesture recognizer also implements the <a href="https://msdn.microsoft.com/bf961d70-2576-493b-a34d-c7c72b6c0234">IStylusAsyncPlugin</a> interface so it can be placed on the UI thread.




## -see-also




<a href="https://msdn.microsoft.com/938e1eb2-3dd4-4e21-9c46-9ef840172b05">DynamicRenderer Class</a>



<a href="https://msdn.microsoft.com/7cdaf3bf-7aae-4d36-af1c-0eb5a726f388">GestureRecognizer Class</a>



<a href="https://msdn.microsoft.com/bbef5cdb-4112-4733-80bb-692b7a198605">IStylusPlugin</a>



<a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a>
 

 

