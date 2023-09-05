---
UID: NF:tuner.IATSCLocator.put_PhysicalChannel
title: IATSCLocator::put_PhysicalChannel (tuner.h)
description: The put_PhysicalChannel method sets the physical channel.
helpviewer_keywords: ["IATSCLocator interface [Microsoft TV Technologies]","put_PhysicalChannel method","IATSCLocator.put_PhysicalChannel","IATSCLocator::put_PhysicalChannel","IATSCLocatorput_PhysicalChannel","mstv.iatsclocator_put_physicalchannel","put_PhysicalChannel","put_PhysicalChannel method [Microsoft TV Technologies]","put_PhysicalChannel method [Microsoft TV Technologies]","IATSCLocator interface","tuner/IATSCLocator::put_PhysicalChannel"]
old-location: mstv\iatsclocator_put_physicalchannel.htm
tech.root: mstv
ms.assetid: 0699e4ef-7ebb-4515-9894-1592f07607ed
ms.date: 12/05/2018
ms.keywords: IATSCLocator interface [Microsoft TV Technologies],put_PhysicalChannel method, IATSCLocator.put_PhysicalChannel, IATSCLocator::put_PhysicalChannel, IATSCLocatorput_PhysicalChannel, mstv.iatsclocator_put_physicalchannel, put_PhysicalChannel, put_PhysicalChannel method [Microsoft TV Technologies], put_PhysicalChannel method [Microsoft TV Technologies],IATSCLocator interface, tuner/IATSCLocator::put_PhysicalChannel
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
 - IATSCLocator::put_PhysicalChannel
 - tuner/IATSCLocator::put_PhysicalChannel
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
 - IATSCLocator.put_PhysicalChannel
---

# IATSCLocator::put_PhysicalChannel


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_PhysicalChannel</b> method sets the physical channel.

## -parameters

### -param PhysicalChannel [in]

The physical channel.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -remarks

This is a required property. A tuner cannot locate an ATSC transmission source without it.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iatsclocator">IATSCLocator Interface</a>