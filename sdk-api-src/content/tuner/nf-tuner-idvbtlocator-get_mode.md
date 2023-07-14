---
UID: NF:tuner.IDVBTLocator.get_Mode
title: IDVBTLocator::get_Mode (tuner.h)
description: The get_Mode method receives the transmission mode.
helpviewer_keywords: ["IDVBTLocator interface [Microsoft TV Technologies]","get_Mode method","IDVBTLocator.get_Mode","IDVBTLocator::get_Mode","IDVBTLocatorget_Mode","get_Mode","get_Mode method [Microsoft TV Technologies]","get_Mode method [Microsoft TV Technologies]","IDVBTLocator interface","mstv.idvbtlocator_get_mode","tuner/IDVBTLocator::get_Mode"]
old-location: mstv\idvbtlocator_get_mode.htm
tech.root: mstv
ms.assetid: 1896ca9d-fb43-49eb-88a7-c6217d468a2b
ms.date: 12/05/2018
ms.keywords: IDVBTLocator interface [Microsoft TV Technologies],get_Mode method, IDVBTLocator.get_Mode, IDVBTLocator::get_Mode, IDVBTLocatorget_Mode, get_Mode, get_Mode method [Microsoft TV Technologies], get_Mode method [Microsoft TV Technologies],IDVBTLocator interface, mstv.idvbtlocator_get_mode, tuner/IDVBTLocator::get_Mode
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
 - IDVBTLocator::get_Mode
 - tuner/IDVBTLocator::get_Mode
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
 - IDVBTLocator.get_Mode
---

# IDVBTLocator::get_Mode


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_Mode</b> method receives the transmission mode.

## -parameters

### -param mode [out]

Receives a member of the <a href="/previous-versions/windows/desktop/mstv/transmissionmode">TransmissionMode</a> enumeration.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-idvbtlocator">IDVBTLocator Interface</a>