---
UID: NF:bdaiface.IBDA_DigitalDemodulator2.get_GuardInterval
title: IBDA_DigitalDemodulator2::get_GuardInterval (bdaiface.h)
description: Gets the demodulator's guard interval.
helpviewer_keywords: ["IBDA_DigitalDemodulator2 interface [Microsoft TV Technologies]","get_GuardInterval method","IBDA_DigitalDemodulator2.get_GuardInterval","IBDA_DigitalDemodulator2::get_GuardInterval","bdaiface/IBDA_DigitalDemodulator2::get_GuardInterval","get_GuardInterval","get_GuardInterval method [Microsoft TV Technologies]","get_GuardInterval method [Microsoft TV Technologies]","IBDA_DigitalDemodulator2 interface","mstv.ibda_digitaldemodulator2_get_guardinterval"]
old-location: mstv\ibda_digitaldemodulator2_get_guardinterval.htm
tech.root: mstv
ms.assetid: e122fac7-bad8-4fbf-bf7d-ffbfad75a5d8
ms.date: 12/05/2018
ms.keywords: IBDA_DigitalDemodulator2 interface [Microsoft TV Technologies],get_GuardInterval method, IBDA_DigitalDemodulator2.get_GuardInterval, IBDA_DigitalDemodulator2::get_GuardInterval, bdaiface/IBDA_DigitalDemodulator2::get_GuardInterval, get_GuardInterval, get_GuardInterval method [Microsoft TV Technologies], get_GuardInterval method [Microsoft TV Technologies],IBDA_DigitalDemodulator2 interface, mstv.ibda_digitaldemodulator2_get_guardinterval
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
 - IBDA_DigitalDemodulator2::get_GuardInterval
 - bdaiface/IBDA_DigitalDemodulator2::get_GuardInterval
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
 - IBDA_DigitalDemodulator2.get_GuardInterval
---

# IBDA_DigitalDemodulator2::get_GuardInterval


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the demodulator's guard interval.

## -parameters

### -param pGuardInterval [in, out]

Receives the guard interval, specified as a member of the <a href="/previous-versions/windows/desktop/mstv/guardinterval">GuardInterval</a> enumeration.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_digitaldemodulator2">IBDA_DigitalDemodulator2</a>