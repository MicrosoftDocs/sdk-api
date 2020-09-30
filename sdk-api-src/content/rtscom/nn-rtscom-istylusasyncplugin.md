---
UID: NN:rtscom.IStylusAsyncPlugin
title: IStylusAsyncPlugin (rtscom.h)
description: Represents an asynchronous plug-in that can be added to the asynchronous plug-in collection of the RealTimeStylus Class object.
helpviewer_keywords: ["IStylusAsyncPlugin","IStylusAsyncPlugin interface [Tablet PC]","IStylusAsyncPlugin interface [Tablet PC]","described","bf961d70-2576-493b-a34d-c7c72b6c0234","rtscom/IStylusAsyncPlugin","tablet.istylusasyncplugin"]
old-location: tablet\istylusasyncplugin.htm
tech.root: tablet
ms.assetid: bf961d70-2576-493b-a34d-c7c72b6c0234
ms.date: 12/05/2018
ms.keywords: IStylusAsyncPlugin, IStylusAsyncPlugin interface [Tablet PC], IStylusAsyncPlugin interface [Tablet PC],described, bf961d70-2576-493b-a34d-c7c72b6c0234, rtscom/IStylusAsyncPlugin, tablet.istylusasyncplugin
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IStylusAsyncPlugin
 - rtscom/IStylusAsyncPlugin
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RTSCom.dll
api_name:
 - IStylusAsyncPlugin
---

# IStylusAsyncPlugin interface


## -description

Represents an asynchronous plug-in that can be added to the asynchronous plug-in collection of the <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object.

## -remarks

This is the asynchronous version of <a href="/windows/desktop/api/rtscom/nn-rtscom-istylusplugin">IStylusPlugin Interface</a>.

This plug-in receives notifications of <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> events enabling you to do custom processing.

The <a href="/windows/desktop/tablet/gesturerecognizer-class">GestureRecognizer Class</a> is an example of a plug-in that implements the <b>IStylusAsyncPlugin</b> interface in order to respond in a timely fashion to the stylus. In some circumstances, such as when large numbers of gestures are subscribed to, the response time in the gesture recognizer becomes excessively slow. To avoid this problem, the <b>GestureRecognizer Class</b> implements the <b>IStylusAsyncPlugin</b> interface so that it can be called asynchronously.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)">DynamicRenderer Class</a>



<a href="/windows/desktop/tablet/gesturerecognizer-class">GestureRecognizer Class</a>



<a href="/windows/desktop/api/rtscom/nn-rtscom-istylusplugin">IStylusPlugin</a>



<a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a>



<a href="/windows/desktop/tablet/realtimestylus-classes-and-interfaces">RealTimeStylus Classes and Interfaces</a>