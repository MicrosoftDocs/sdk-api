---
UID: NF:tuner.IDVBTuningSpace.put_SystemType
title: IDVBTuningSpace::put_SystemType (tuner.h)
description: The put_SystemType method sets the system type.
helpviewer_keywords: ["IDVBTuningSpace interface [Microsoft TV Technologies]","put_SystemType method","IDVBTuningSpace.put_SystemType","IDVBTuningSpace::put_SystemType","IDVBTuningSpaceput_SystemType","mstv.idvbtuningspace_put_systemtype","put_SystemType","put_SystemType method [Microsoft TV Technologies]","put_SystemType method [Microsoft TV Technologies]","IDVBTuningSpace interface","tuner/IDVBTuningSpace::put_SystemType"]
old-location: mstv\idvbtuningspace_put_systemtype.htm
tech.root: mstv
ms.assetid: 559f882a-4d1c-4fe1-af21-b3ad7ccd3ff2
ms.date: 12/05/2018
ms.keywords: IDVBTuningSpace interface [Microsoft TV Technologies],put_SystemType method, IDVBTuningSpace.put_SystemType, IDVBTuningSpace::put_SystemType, IDVBTuningSpaceput_SystemType, mstv.idvbtuningspace_put_systemtype, put_SystemType, put_SystemType method [Microsoft TV Technologies], put_SystemType method [Microsoft TV Technologies],IDVBTuningSpace interface, tuner/IDVBTuningSpace::put_SystemType
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
 - IDVBTuningSpace::put_SystemType
 - tuner/IDVBTuningSpace::put_SystemType
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
 - IDVBTuningSpace.put_SystemType
---

# IDVBTuningSpace::put_SystemType


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_SystemType</b> method sets the system type.

## -parameters

### -param SysType [in]

Variable of type <a href="/previous-versions/windows/desktop/mstv/dvbsystemtype">DVBSystemType</a> that specifies the system type.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-idvbtuningspace">IDVBTuningSpace Interface</a>