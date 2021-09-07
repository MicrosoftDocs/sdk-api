---
UID: NN:rtscom.IRealTimeStylus2
title: IRealTimeStylus2 (rtscom.h)
description: Extends the IRealTimeStylus interface.
helpviewer_keywords: ["IRealTimeStylus2","IRealTimeStylus2 interface [Tablet PC]","IRealTimeStylus2 interface [Tablet PC]","described","d4b55c1d-f8cc-4aed-86a3-b5935d127c2d","rtscom/IRealTimeStylus2","tablet.irealtimestylus2"]
old-location: tablet\irealtimestylus2.htm
tech.root: tablet
ms.assetid: d4b55c1d-f8cc-4aed-86a3-b5935d127c2d
ms.date: 12/05/2018
ms.keywords: IRealTimeStylus2, IRealTimeStylus2 interface [Tablet PC], IRealTimeStylus2 interface [Tablet PC],described, d4b55c1d-f8cc-4aed-86a3-b5935d127c2d, rtscom/IRealTimeStylus2, tablet.irealtimestylus2
req.header: rtscom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IRealTimeStylus2
 - rtscom/IRealTimeStylus2
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
 - IRealTimeStylus2
---

# IRealTimeStylus2 interface


## -description

Extends the <a href="/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus">IRealTimeStylus</a> interface.

## -inheritance

The <b>IRealTimeStylus2</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRealTimeStylus2</b> also has these types of members:

## -remarks

This interface only exists in the Windows Vista <a href="/windows/desktop/tablet/realtimestylus-classes-and-interfaces">RealTimeStylus</a>. Flick notification is received via a <a href="/windows/desktop/api/rtscom/nf-rtscom-istylusplugin-systemevent">IStylusPlugin::SystemEvent Method</a> plugin notification with event id equal to <b>ISG_Flick</b>. To obtain flick data look at the <b>SYSTEM_EVENT_DATA</b> struct: <i>xPos</i>/<i>yPos</i> contains the flick start location in Tablet coordinates, <i>wKey</i> contains the direction (a value where 90 is down, 180 is left, 270 is up), and <i>dwButtonState</i> contains the same data obtained from the <i>wParam</i> for the <a href="/windows/desktop/tablet/wm-tablet-flick-message">WM_TABLET_FLICK Message</a>.

## -see-also

<a href="/windows/desktop/tablet/flicks-api-reference">Flicks API Reference</a>



<a href="/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus">IRealTimeStylus</a>
