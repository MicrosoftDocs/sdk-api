---
UID: NN:rtscom.IStylusSyncPlugin
title: IStylusSyncPlugin (rtscom.h)
description: Represents a synchronous plug-in that can be added to the RealTimeStylus Class object's synchronous plug-in collection.
helpviewer_keywords: ["IStylusSyncPlugin","IStylusSyncPlugin interface [Tablet PC]","IStylusSyncPlugin interface [Tablet PC]","described","e3e02d5a-a004-49de-b2d8-86ccfc120481","rtscom/IStylusSyncPlugin","tablet.istylussyncplugin"]
old-location: tablet\istylussyncplugin.htm
tech.root: tablet
ms.assetid: e3e02d5a-a004-49de-b2d8-86ccfc120481
ms.date: 12/05/2018
ms.keywords: IStylusSyncPlugin, IStylusSyncPlugin interface [Tablet PC], IStylusSyncPlugin interface [Tablet PC],described, e3e02d5a-a004-49de-b2d8-86ccfc120481, rtscom/IStylusSyncPlugin, tablet.istylussyncplugin
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
 - IStylusSyncPlugin
 - rtscom/IStylusSyncPlugin
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
 - IStylusSyncPlugin
---

# IStylusSyncPlugin interface


## -description

Represents a synchronous plug-in that can be added to the <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object's synchronous plug-in collection.

## -remarks

This is the synchronous version of <a href="/windows/desktop/api/rtscom/nn-rtscom-istylusplugin">IStylusPlugin Interface</a>. It provides for strong type checking in the synchronous plug-in collections.

This plug-in receives notifications of <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> events enabling you to do custom processing.

The dynamic renderer and gesture recognizer are examples of plug-ins which implement the <b>IStylusSyncPlugin</b> interface. The dynamic renderer implements the <b>IStylusSyncPlugin</b> interface in order to respond in a timely fashion to the stylus.

In some circumstances, such as when large numbers of gestures are subscribed to, the response time in the gesture recognizer becomes excessively slow. To avoid this problem, the gesture recognizer also implements the <a href="/windows/desktop/api/rtscom/nn-rtscom-istylusasyncplugin">IStylusAsyncPlugin</a> interface so it can be placed on the UI thread.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)">DynamicRenderer Class</a>



<a href="/windows/desktop/tablet/gesturerecognizer-class">GestureRecognizer Class</a>



<a href="/windows/desktop/api/rtscom/nn-rtscom-istylusplugin">IStylusPlugin</a>



<a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a>