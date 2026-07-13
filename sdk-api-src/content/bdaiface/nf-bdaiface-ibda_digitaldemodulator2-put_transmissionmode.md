---
UID: NF:bdaiface.IBDA_DigitalDemodulator2.put_TransmissionMode
title: IBDA_DigitalDemodulator2::put_TransmissionMode (bdaiface.h)
description: Sets the demodulator's transmission mode.
helpviewer_keywords: ["IBDA_DigitalDemodulator2 interface [Microsoft TV Technologies]","put_TransmissionMode method","IBDA_DigitalDemodulator2.put_TransmissionMode","IBDA_DigitalDemodulator2::put_TransmissionMode","bdaiface/IBDA_DigitalDemodulator2::put_TransmissionMode","mstv.ibda_digitaldemodulator2_put_transmissionmode","put_TransmissionMode","put_TransmissionMode method [Microsoft TV Technologies]","put_TransmissionMode method [Microsoft TV Technologies]","IBDA_DigitalDemodulator2 interface"]
old-location: mstv\ibda_digitaldemodulator2_put_transmissionmode.htm
tech.root: mstv
ms.assetid: e10c63a5-7025-49a7-9b2e-6043fabf2999
ms.date: 12/05/2018
ms.keywords: IBDA_DigitalDemodulator2 interface [Microsoft TV Technologies],put_TransmissionMode method, IBDA_DigitalDemodulator2.put_TransmissionMode, IBDA_DigitalDemodulator2::put_TransmissionMode, bdaiface/IBDA_DigitalDemodulator2::put_TransmissionMode, mstv.ibda_digitaldemodulator2_put_transmissionmode, put_TransmissionMode, put_TransmissionMode method [Microsoft TV Technologies], put_TransmissionMode method [Microsoft TV Technologies],IBDA_DigitalDemodulator2 interface
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
 - IBDA_DigitalDemodulator2::put_TransmissionMode
 - bdaiface/IBDA_DigitalDemodulator2::put_TransmissionMode
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
 - IBDA_DigitalDemodulator2.put_TransmissionMode
---

# IBDA_DigitalDemodulator2::put_TransmissionMode


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Sets the demodulator's transmission mode.

## -parameters

### -param pTransmissionMode [in]

Pointer to a variable that contains the transmission mode, specified as a member of the <a href="/previous-versions/windows/desktop/mstv/transmissionmode">TransmissionMode</a> enumeration.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_digitaldemodulator2">IBDA_DigitalDemodulator2</a>