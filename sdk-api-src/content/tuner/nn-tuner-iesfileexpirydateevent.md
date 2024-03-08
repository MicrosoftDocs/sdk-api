---
UID: NN:tuner.IESFileExpiryDateEvent
title: IESFileExpiryDateEvent (tuner.h)
description: Gets information from a FileExpiryDate event.
helpviewer_keywords: ["IESFileExpiryDateEvent","IESFileExpiryDateEvent interface [Microsoft TV Technologies]","IESFileExpiryDateEvent interface [Microsoft TV Technologies]","described","mstv.iesfileexpirydateevent","tuner/IESFileExpiryDateEvent"]
old-location: mstv\iesfileexpirydateevent.htm
tech.root: mstv
ms.assetid: 6c89a3ee-7d69-4cde-b1e5-b566fa1c2ca3
ms.date: 12/05/2018
ms.keywords: IESFileExpiryDateEvent, IESFileExpiryDateEvent interface [Microsoft TV Technologies], IESFileExpiryDateEvent interface [Microsoft TV Technologies],described, mstv.iesfileexpirydateevent, tuner/IESFileExpiryDateEvent
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
 - IESFileExpiryDateEvent
 - tuner/IESFileExpiryDateEvent
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
 - IESFileExpiryDateEvent
---

# IESFileExpiryDateEvent interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets information from a  <b>FileExpiryDate</b> event. A Protected Broadcast Driver Architecture (PBDA) media transform device (MTD) fires a <b>FileExpiryDate</b> event when it receives a new license for protected content that contains a new expiry date for that content.

## -inheritance

The <b>IESFileExpiryDateEvent</b> interface inherits from <b>IESEvent</b>. <b>IESFileExpiryDateEvent</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IESFileExpiryDateEvent)</code>.
