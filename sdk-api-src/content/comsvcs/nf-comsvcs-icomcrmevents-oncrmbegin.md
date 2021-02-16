---
UID: NF:comsvcs.IComCRMEvents.OnCRMBegin
title: IComCRMEvents::OnCRMBegin (comsvcs.h)
description: Generated when a CRM clerk is starting, either due to a client registering a compensator or during recovery.
helpviewer_keywords: ["IComCRMEvents interface [COM+]","OnCRMBegin method","IComCRMEvents.OnCRMBegin","IComCRMEvents::OnCRMBegin","OnCRMBegin","OnCRMBegin method [COM+]","OnCRMBegin method [COM+]","IComCRMEvents interface","_dtc_IComCRMEvents_OnCRMBegin","comsvcs/IComCRMEvents::OnCRMBegin","cos.icomcrmevents_oncrmbegin"]
old-location: cos\icomcrmevents_oncrmbegin.htm
tech.root: cos
ms.assetid: 8975cb5e-024f-40bf-acd7-c5af0abd88a0
ms.date: 12/05/2018
ms.keywords: IComCRMEvents interface [COM+],OnCRMBegin method, IComCRMEvents.OnCRMBegin, IComCRMEvents::OnCRMBegin, OnCRMBegin, OnCRMBegin method [COM+], OnCRMBegin method [COM+],IComCRMEvents interface, _dtc_IComCRMEvents_OnCRMBegin, comsvcs/IComCRMEvents::OnCRMBegin, cos.icomcrmevents_oncrmbegin
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IComCRMEvents::OnCRMBegin
 - comsvcs/IComCRMEvents::OnCRMBegin
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IComCRMEvents.OnCRMBegin
---

# IComCRMEvents::OnCRMBegin


## -description

Generated when a CRM clerk is starting, either due to a client registering a compensator or during recovery.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.

### -param guidClerkCLSID [in]

The identifier of the CRM clerk.

### -param guidActivity [in]

The activity identifier (NULL if recovery).

### -param guidTx [in]

The identifier of the Transaction Unit Of Work (UOW).

### -param szProgIdCompensator [in]

The ProgID of the CRM compensator.

### -param szDescription [in]

The description (blank if recovery).

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomcrmevents">IComCRMEvents</a>