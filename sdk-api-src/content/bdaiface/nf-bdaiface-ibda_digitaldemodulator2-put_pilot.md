---
UID: NF:bdaiface.IBDA_DigitalDemodulator2.put_Pilot
title: IBDA_DigitalDemodulator2::put_Pilot (bdaiface.h)
description: Sets the current pilot mode for Digital Video Broadcasting-S2 (DVB-S2).
helpviewer_keywords: ["IBDA_DigitalDemodulator2 interface [Microsoft TV Technologies]","put_Pilot method","IBDA_DigitalDemodulator2.put_Pilot","IBDA_DigitalDemodulator2::put_Pilot","bdaiface/IBDA_DigitalDemodulator2::put_Pilot","mstv.ibda_digitaldemodulator2_put_pilot","put_Pilot","put_Pilot method [Microsoft TV Technologies]","put_Pilot method [Microsoft TV Technologies]","IBDA_DigitalDemodulator2 interface"]
old-location: mstv\ibda_digitaldemodulator2_put_pilot.htm
tech.root: mstv
ms.assetid: 05a29e8a-88f1-4e79-9f6c-ed3798b94c1f
ms.date: 12/05/2018
ms.keywords: IBDA_DigitalDemodulator2 interface [Microsoft TV Technologies],put_Pilot method, IBDA_DigitalDemodulator2.put_Pilot, IBDA_DigitalDemodulator2::put_Pilot, bdaiface/IBDA_DigitalDemodulator2::put_Pilot, mstv.ibda_digitaldemodulator2_put_pilot, put_Pilot, put_Pilot method [Microsoft TV Technologies], put_Pilot method [Microsoft TV Technologies],IBDA_DigitalDemodulator2 interface
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
 - IBDA_DigitalDemodulator2::put_Pilot
 - bdaiface/IBDA_DigitalDemodulator2::put_Pilot
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
 - IBDA_DigitalDemodulator2.put_Pilot
---

# IBDA_DigitalDemodulator2::put_Pilot


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Sets the current pilot mode for Digital Video Broadcasting-S2 (DVB-S2).

## -parameters

### -param pPilot [in]

Pointer to a variable that contains the pilot mode, specified as a member of the <a href="/previous-versions/windows/desktop/mstv/pilot">Pilot</a> enumeration.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_digitaldemodulator2">IBDA_DigitalDemodulator2</a>