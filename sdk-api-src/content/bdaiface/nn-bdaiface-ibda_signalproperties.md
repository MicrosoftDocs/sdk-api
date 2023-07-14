---
UID: NN:bdaiface.IBDA_SignalProperties
title: IBDA_SignalProperties (bdaiface.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["IBDA_SignalProperties","IBDA_SignalProperties interface [Microsoft TV Technologies]","IBDA_SignalProperties interface [Microsoft TV Technologies]","described","IBDA_SignalPropertiesInterface","bdaiface/IBDA_SignalProperties","mstv.ibda_signalproperties"]
old-location: mstv\ibda_signalproperties.htm
tech.root: mstv
ms.assetid: fe88b628-7959-4d2f-981f-7de9126146f6
ms.date: 12/05/2018
ms.keywords: IBDA_SignalProperties, IBDA_SignalProperties interface [Microsoft TV Technologies], IBDA_SignalProperties interface [Microsoft TV Technologies],described, IBDA_SignalPropertiesInterface, bdaiface/IBDA_SignalProperties, mstv.ibda_signalproperties
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBDA_SignalProperties
 - bdaiface/IBDA_SignalProperties
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bdaiface.h
api_name:
 - IBDA_SignalProperties
---

# IBDA_SignalProperties interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        

The <b>IBDA_SignalProperties</b> interface is implemented by a BDA device filter. Through this interface, the network provider informs a BDA device filter about the current tuning request. The network provider calls the <b>PutXxx</b> methods in the interface at the time that the BDA device is registered with the network provider. Thereafter, the network provider calls these methods whenever the current tuning request is modified.

## -inheritance

The <b>IBDA_SignalProperties</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IBDA_SignalProperties</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDA_SignalProperties)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
