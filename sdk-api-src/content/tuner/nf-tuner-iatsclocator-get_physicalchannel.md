---
UID: NF:tuner.IATSCLocator.get_PhysicalChannel
title: IATSCLocator::get_PhysicalChannel (tuner.h)
description: The get_PhysicalChannel method retrieves the physical channel.
helpviewer_keywords: ["IATSCLocator interface [Microsoft TV Technologies]","get_PhysicalChannel method","IATSCLocator.get_PhysicalChannel","IATSCLocator::get_PhysicalChannel","IATSCLocatorget_PhysicalChannel","get_PhysicalChannel","get_PhysicalChannel method [Microsoft TV Technologies]","get_PhysicalChannel method [Microsoft TV Technologies]","IATSCLocator interface","mstv.iatsclocator_get_physicalchannel","tuner/IATSCLocator::get_PhysicalChannel"]
old-location: mstv\iatsclocator_get_physicalchannel.htm
tech.root: mstv
ms.assetid: 7550bbb9-d9f7-4565-9c63-7179c0bdffa5
ms.date: 12/05/2018
ms.keywords: IATSCLocator interface [Microsoft TV Technologies],get_PhysicalChannel method, IATSCLocator.get_PhysicalChannel, IATSCLocator::get_PhysicalChannel, IATSCLocatorget_PhysicalChannel, get_PhysicalChannel, get_PhysicalChannel method [Microsoft TV Technologies], get_PhysicalChannel method [Microsoft TV Technologies],IATSCLocator interface, mstv.iatsclocator_get_physicalchannel, tuner/IATSCLocator::get_PhysicalChannel
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
 - IATSCLocator::get_PhysicalChannel
 - tuner/IATSCLocator::get_PhysicalChannel
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
 - IATSCLocator.get_PhysicalChannel
---

# IATSCLocator::get_PhysicalChannel


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_PhysicalChannel</b> method retrieves the physical channel.

## -parameters

### -param PhysicalChannel [out]

Receives the physical channel.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -remarks

This is a required property. A tuner cannot locate an ATSC transmission source without it.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iatsclocator">IATSCLocator Interface</a>