---
UID: NF:tuner.IDVBTuningSpace2.put_NetworkID
title: IDVBTuningSpace2::put_NetworkID (tuner.h)
description: The put_NetworkID method sets the Network ID of the DVB system.
helpviewer_keywords: ["IDVBTuningSpace2 interface [Microsoft TV Technologies]","put_NetworkID method","IDVBTuningSpace2.put_NetworkID","IDVBTuningSpace2::put_NetworkID","IDVBTuningSpace2put_NetworkID","mstv.idvbtuningspace2_put_networkid","put_NetworkID","put_NetworkID method [Microsoft TV Technologies]","put_NetworkID method [Microsoft TV Technologies]","IDVBTuningSpace2 interface","tuner/IDVBTuningSpace2::put_NetworkID"]
old-location: mstv\idvbtuningspace2_put_networkid.htm
tech.root: mstv
ms.assetid: 4f307629-710d-4992-b407-311774aa544a
ms.date: 12/05/2018
ms.keywords: IDVBTuningSpace2 interface [Microsoft TV Technologies],put_NetworkID method, IDVBTuningSpace2.put_NetworkID, IDVBTuningSpace2::put_NetworkID, IDVBTuningSpace2put_NetworkID, mstv.idvbtuningspace2_put_networkid, put_NetworkID, put_NetworkID method [Microsoft TV Technologies], put_NetworkID method [Microsoft TV Technologies],IDVBTuningSpace2 interface, tuner/IDVBTuningSpace2::put_NetworkID
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
 - IDVBTuningSpace2::put_NetworkID
 - tuner/IDVBTuningSpace2::put_NetworkID
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
 - IDVBTuningSpace2.put_NetworkID
---

# IDVBTuningSpace2::put_NetworkID


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_NetworkID</b> method sets the Network ID of the DVB system.

## -parameters

### -param NetworkID [in]

Specifies the <i>NetworkID</i> as a <b>long</b> integer.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-idvbtuningspace2">IDVBTuningSpace2 Interface</a>