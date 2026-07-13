---
UID: NN:rtscom.IRealTimeStylusSynchronization
title: IRealTimeStylusSynchronization (rtscom.h)
description: Synchronizes access to the RealTimeStylus Class object.
helpviewer_keywords: ["IRealTimeStylusSynchronization","IRealTimeStylusSynchronization interface [Tablet PC]","IRealTimeStylusSynchronization interface [Tablet PC]","described","fe76386d-55b5-40a8-aa6f-b4a1ee8d9fbd","rtscom/IRealTimeStylusSynchronization","tablet.irealtimestylussynchronization"]
old-location: tablet\irealtimestylussynchronization.htm
tech.root: tablet
ms.assetid: fe76386d-55b5-40a8-aa6f-b4a1ee8d9fbd
ms.date: 12/05/2018
ms.keywords: IRealTimeStylusSynchronization, IRealTimeStylusSynchronization interface [Tablet PC], IRealTimeStylusSynchronization interface [Tablet PC],described, fe76386d-55b5-40a8-aa6f-b4a1ee8d9fbd, rtscom/IRealTimeStylusSynchronization, tablet.irealtimestylussynchronization
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
 - IRealTimeStylusSynchronization
 - rtscom/IRealTimeStylusSynchronization
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
 - IRealTimeStylusSynchronization
---

# IRealTimeStylusSynchronization interface


## -description

Synchronizes access to the <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object.

## -inheritance

The <b>IRealTimeStylusSynchronization</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRealTimeStylusSynchronization</b> also has these types of members:

## -remarks

Use locks when you must protect access to and modification of the plug-ins or properties of the <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus</a> object through the <b>IRealTimeStylusSynchronization Interface</b> interface.

Use the <a href="/windows/desktop/api/rtscom/ne-rtscom-realtimestyluslocktype">RealTimeStylusLockType Enumeration</a> enumeration to specify the lock.

## -see-also

<a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a>



<a href="/windows/desktop/tablet/realtimestylus-classes-and-interfaces">RealTimeStylus Classes and Interfaces</a>
