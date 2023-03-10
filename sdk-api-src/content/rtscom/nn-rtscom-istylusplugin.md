---
UID: NN:rtscom.IStylusPlugin
title: IStylusPlugin (rtscom.h)
description: Receives notifications of RealTimeStylus Class events to enable you to perform custom processing based on those events.
helpviewer_keywords: ["IStylusPlugin","IStylusPlugin interface [Tablet PC]","IStylusPlugin interface [Tablet PC]","described","bbef5cdb-4112-4733-80bb-692b7a198605","rtscom/IStylusPlugin","tablet.istylusplugin"]
old-location: tablet\istylusplugin.htm
tech.root: tablet
ms.assetid: bbef5cdb-4112-4733-80bb-692b7a198605
ms.date: 12/05/2018
ms.keywords: IStylusPlugin, IStylusPlugin interface [Tablet PC], IStylusPlugin interface [Tablet PC],described, bbef5cdb-4112-4733-80bb-692b7a198605, rtscom/IStylusPlugin, tablet.istylusplugin
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
 - IStylusPlugin
 - rtscom/IStylusPlugin
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
 - IStylusPlugin
---

# IStylusPlugin interface


## -description

Receives notifications of <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> events to enable you to perform custom processing based on those events.

## -inheritance

The <b>IStylusPlugin</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IStylusPlugin</b> also has these types of members:

## -remarks

Both the <a href="/windows/desktop/api/rtscom/nn-rtscom-istylussyncplugin">IStylusSyncPlugin</a> and <a href="/windows/desktop/api/rtscom/nn-rtscom-istylusasyncplugin">IStylusAsyncPlugin</a> interfaces derive from this interface and can be added to <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> plug-in collections.

## -see-also

<a href="/windows/desktop/api/rtscom/nn-rtscom-istylussyncplugin">IStylusSyncPlugin</a>



<a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a>
