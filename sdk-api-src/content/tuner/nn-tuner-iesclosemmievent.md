---
UID: NN:tuner.IESCloseMmiEvent
title: IESCloseMmiEvent (tuner.h)
description: Receives CloseMMI events from a Media Sink Device (MSD) device under the Protected Broadcast Driver Architecture (PBDA).
helpviewer_keywords: ["IESCloseMmiEvent","IESCloseMmiEvent interface [Microsoft TV Technologies]","IESCloseMmiEvent interface [Microsoft TV Technologies]","described","mstv.iesclosemmievent","tuner/IESCloseMmiEvent"]
old-location: mstv\iesclosemmievent.htm
tech.root: mstv
ms.assetid: c470fefb-61bb-4315-ad56-ef5bc90a4ac7
ms.date: 12/05/2018
ms.keywords: IESCloseMmiEvent, IESCloseMmiEvent interface [Microsoft TV Technologies], IESCloseMmiEvent interface [Microsoft TV Technologies],described, mstv.iesclosemmievent, tuner/IESCloseMmiEvent
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IESCloseMmiEvent
 - tuner/IESCloseMmiEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IESCloseMmiEvent
---

# IESCloseMmiEvent interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Receives <b>CloseMMI</b> events from a Media Sink Device (MSD) device under the Protected Broadcast Driver Architecture (PBDA).  The MSD is the device that receives protected content from a Media Transform Device (MTD). This event tells the MTD that the MSD trying to close a man-machine interface (MMI) display, such as a dialog box.

## -inheritance

The <b>IESCloseMmiEvent</b> interface inherits from <b>IESEvent</b>. <b>IESCloseMmiEvent</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IESCloseMmiEvent)</code>.
