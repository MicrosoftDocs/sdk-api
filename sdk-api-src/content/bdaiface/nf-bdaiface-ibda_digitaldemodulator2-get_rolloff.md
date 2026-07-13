---
UID: NF:bdaiface.IBDA_DigitalDemodulator2.get_RollOff
title: IBDA_DigitalDemodulator2::get_RollOff (bdaiface.h)
description: Gets the demodulator's roll-off factor.
helpviewer_keywords: ["IBDA_DigitalDemodulator2 interface [Microsoft TV Technologies]","get_RollOff method","IBDA_DigitalDemodulator2.get_RollOff","IBDA_DigitalDemodulator2::get_RollOff","bdaiface/IBDA_DigitalDemodulator2::get_RollOff","get_RollOff","get_RollOff method [Microsoft TV Technologies]","get_RollOff method [Microsoft TV Technologies]","IBDA_DigitalDemodulator2 interface","mstv.ibda_digitaldemodulator2_get_rolloff"]
old-location: mstv\ibda_digitaldemodulator2_get_rolloff.htm
tech.root: mstv
ms.assetid: 4b1cd08a-50fd-48e9-9e97-8460e6c990c1
ms.date: 12/05/2018
ms.keywords: IBDA_DigitalDemodulator2 interface [Microsoft TV Technologies],get_RollOff method, IBDA_DigitalDemodulator2.get_RollOff, IBDA_DigitalDemodulator2::get_RollOff, bdaiface/IBDA_DigitalDemodulator2::get_RollOff, get_RollOff, get_RollOff method [Microsoft TV Technologies], get_RollOff method [Microsoft TV Technologies],IBDA_DigitalDemodulator2 interface, mstv.ibda_digitaldemodulator2_get_rolloff
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bdaiface.idl
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
 - IBDA_DigitalDemodulator2::get_RollOff
 - bdaiface/IBDA_DigitalDemodulator2::get_RollOff
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
 - IBDA_DigitalDemodulator2.get_RollOff
---

# IBDA_DigitalDemodulator2::get_RollOff


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the demodulator's roll-off factor.

## -parameters

### -param pRollOff [in, out]

Receives the roll-off factor, specified as a member of the <a href="/previous-versions/windows/desktop/mstv/rolloff">RollOff</a> enumeration.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_digitaldemodulator2">IBDA_DigitalDemodulator2</a>