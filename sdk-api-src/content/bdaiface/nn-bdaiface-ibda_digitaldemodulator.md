---
UID: NN:bdaiface.IBDA_DigitalDemodulator
title: IBDA_DigitalDemodulator (bdaiface.h)
description: The IBDA_DigitalDemodulator interface is exposed on BDA device filters, specifically demodulators, that are not capable of automatically detecting the characteristics of a signal.
helpviewer_keywords: ["IBDA_DigitalDemodulator","IBDA_DigitalDemodulator interface [Microsoft TV Technologies]","IBDA_DigitalDemodulator interface [Microsoft TV Technologies]","described","IBDA_DigitalDemodulatorInterface","bdaiface/IBDA_DigitalDemodulator","mstv.ibda_digitaldemodulator"]
old-location: mstv\ibda_digitaldemodulator.htm
tech.root: mstv
ms.assetid: 13ecd348-dc2b-4e80-9875-927f4ed55c95
ms.date: 12/05/2018
ms.keywords: IBDA_DigitalDemodulator, IBDA_DigitalDemodulator interface [Microsoft TV Technologies], IBDA_DigitalDemodulator interface [Microsoft TV Technologies],described, IBDA_DigitalDemodulatorInterface, bdaiface/IBDA_DigitalDemodulator, mstv.ibda_digitaldemodulator
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
 - IBDA_DigitalDemodulator
 - bdaiface/IBDA_DigitalDemodulator
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdaiface.h
api_name:
 - IBDA_DigitalDemodulator
---

# IBDA_DigitalDemodulator interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>IBDA_DigitalDemodulator</b> interface is exposed on BDA device filters, specifically demodulators, that are not capable of automatically detecting the characteristics of a signal. A Network Provider calls these methods on the filter to provide the demodulator with the information it needs to acquire a particular signal. The Network Provider obtains these values from the <a href="/previous-versions/windows/desktop/legacy/dd695081(v=vs.85)">Locator</a> object associated with the tune request or tuning space.

<b>OCUR Devices: </b>This interface supports OpenCable Unidirectional Cable Receiver (OCUR) devices. See <a href="/previous-versions/windows/desktop/mstv/ocur-devices">OCUR Devices</a>.

## -inheritance

The <b>IBDA_DigitalDemodulator</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IBDA_DigitalDemodulator</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDA_DigitalDemodulator)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
