---
UID: NN:tuner.IESOpenMmiEvent
title: IESOpenMmiEvent (tuner.h)
description: Gets information from an OpenMMI event.
helpviewer_keywords: ["IESOpenMmiEvent","IESOpenMmiEvent interface [Microsoft TV Technologies]","IESOpenMmiEvent interface [Microsoft TV Technologies]","described","mstv.iesopenmmievent","tuner/IESOpenMmiEvent"]
old-location: mstv\iesopenmmievent.htm
tech.root: mstv
ms.assetid: f54532e2-d1d1-4c6b-ae3d-9f50e0e61366
ms.date: 12/05/2018
ms.keywords: IESOpenMmiEvent, IESOpenMmiEvent interface [Microsoft TV Technologies], IESOpenMmiEvent interface [Microsoft TV Technologies],described, mstv.iesopenmmievent, tuner/IESOpenMmiEvent
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
 - IESOpenMmiEvent
 - tuner/IESOpenMmiEvent
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
 - IESOpenMmiEvent
---

# IESOpenMmiEvent interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets information from an  <b>OpenMMI</b> event. A Protected Broadcast Driver Architecture (PBDA) Media Transform Device (MTD) fires an  <b>OpenMMI</b> event when the device user tries to open an on-screen display, such as a dialog box. 

For more information about PBDA, download the specification from <a href="https://developer.microsoft.com/windows/hardware">this document</a>.

## -inheritance

The <b>IESOpenMmiEvent</b> interface inherits from <b>IESEvent</b>. <b>IESOpenMmiEvent</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IESOpenMmiEvent)</code>.
