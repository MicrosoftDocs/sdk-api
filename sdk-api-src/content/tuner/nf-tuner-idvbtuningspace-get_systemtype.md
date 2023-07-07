---
UID: NF:tuner.IDVBTuningSpace.get_SystemType
title: IDVBTuningSpace::get_SystemType (tuner.h)
description: The get_SystemType method retrieves the system type.
helpviewer_keywords: ["IDVBTuningSpace interface [Microsoft TV Technologies]","get_SystemType method","IDVBTuningSpace.get_SystemType","IDVBTuningSpace::get_SystemType","IDVBTuningSpaceget_SystemType","get_SystemType","get_SystemType method [Microsoft TV Technologies]","get_SystemType method [Microsoft TV Technologies]","IDVBTuningSpace interface","mstv.idvbtuningspace_get_systemtype","tuner/IDVBTuningSpace::get_SystemType"]
old-location: mstv\idvbtuningspace_get_systemtype.htm
tech.root: mstv
ms.assetid: 4e08d142-6ae3-4da7-ba3c-59fdf07a2f10
ms.date: 12/05/2018
ms.keywords: IDVBTuningSpace interface [Microsoft TV Technologies],get_SystemType method, IDVBTuningSpace.get_SystemType, IDVBTuningSpace::get_SystemType, IDVBTuningSpaceget_SystemType, get_SystemType, get_SystemType method [Microsoft TV Technologies], get_SystemType method [Microsoft TV Technologies],IDVBTuningSpace interface, mstv.idvbtuningspace_get_systemtype, tuner/IDVBTuningSpace::get_SystemType
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
 - IDVBTuningSpace::get_SystemType
 - tuner/IDVBTuningSpace::get_SystemType
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
 - IDVBTuningSpace.get_SystemType
---

# IDVBTuningSpace::get_SystemType


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_SystemType</b> method retrieves the system type.

## -parameters

### -param SysType [out]

Pointer to a variable of type <a href="/previous-versions/windows/desktop/mstv/dvbsystemtype">DVBSystemType</a> that receives the system type.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-idvbtuningspace">IDVBTuningSpace Interface</a>