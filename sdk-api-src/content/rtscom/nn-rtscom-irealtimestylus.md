---
UID: NN:rtscom.IRealTimeStylus
title: IRealTimeStylus (rtscom.h)
description: Handles the stylus packet data from a digitizer in real time.
helpviewer_keywords: ["IRealTimeStylus","IRealTimeStylus interface [Tablet PC]","IRealTimeStylus interface [Tablet PC]","described","bfd13012-decf-423a-bc1a-39fb9b0eb64e","rtscom/IRealTimeStylus","tablet.irealtimestylus"]
old-location: tablet\irealtimestylus.htm
tech.root: tablet
ms.assetid: bfd13012-decf-423a-bc1a-39fb9b0eb64e
ms.date: 12/05/2018
ms.keywords: IRealTimeStylus, IRealTimeStylus interface [Tablet PC], IRealTimeStylus interface [Tablet PC],described, bfd13012-decf-423a-bc1a-39fb9b0eb64e, rtscom/IRealTimeStylus, tablet.irealtimestylus
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
 - IRealTimeStylus
 - rtscom/IRealTimeStylus
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
 - IRealTimeStylus
---

# IRealTimeStylus interface


## -description

Handles the stylus packet data from a digitizer in real time.

## -inheritance

The <b>IRealTimeStylus</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRealTimeStylus</b> also has these types of members:

## -remarks

This interface is implemented by the <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a>.

Extensibility is provided through synchronous and asynchronous plug-in models, using the <a href="/windows/desktop/api/rtscom/nn-rtscom-istylussyncplugin">IStylusSyncPlugin</a> and <a href="/windows/desktop/api/rtscom/nn-rtscom-istylusasyncplugin">IStylusAsyncPlugin</a> interfaces respectively to conduct custom processing. Use asynchronous plug-ins for computationally intense operations to avoid blocking the packet stream.

We recommend that you do not use the <a href="/windows/desktop/api/rtscom/nn-rtscom-istylussyncplugin">IStylusSyncPlugin</a> interface implementations for CPU and time-intensive operations since this blocks the packet stream flow. These operations should be conducted in <a href="/windows/desktop/api/rtscom/nn-rtscom-istylusasyncplugin">IStylusAsyncPlugin</a> interface implementation classes which run on a different thread than the thread that maintains the packet stream flow.

<div class="alert"><b>Note</b>  The synchronous and asynchronous plug-in collections on the <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> can be modified without disabling and then re-enabling the <b>RealTimeStylus Class</b> object.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)">DynamicRenderer Class</a>



<a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a>



<a href="/windows/desktop/tablet/realtimestylus-classes-and-interfaces">RealTimeStylus Classes and Interfaces</a>



<a href="/windows/desktop/tablet/realtimestylus-reference">RealTimeStylus Reference</a>
