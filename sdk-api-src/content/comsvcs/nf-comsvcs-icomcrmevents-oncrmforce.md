---
UID: NF:comsvcs.IComCRMEvents.OnCRMForce
title: IComCRMEvents::OnCRMForce (comsvcs.h)
description: Generated when a CRM clerk receives a request to force log records to disk, either from the CRM worker or from the CRM compensator.
helpviewer_keywords: ["IComCRMEvents interface [COM+]","OnCRMForce method","IComCRMEvents.OnCRMForce","IComCRMEvents::OnCRMForce","OnCRMForce","OnCRMForce method [COM+]","OnCRMForce method [COM+]","IComCRMEvents interface","_dtc_IComCRMEvents_OnCRMForce","comsvcs/IComCRMEvents::OnCRMForce","cos.icomcrmevents_oncrmforce"]
old-location: cos\icomcrmevents_oncrmforce.htm
tech.root: cos
ms.assetid: 92f2088b-4d74-4d33-9953-0f5229f6303c
ms.date: 12/05/2018
ms.keywords: IComCRMEvents interface [COM+],OnCRMForce method, IComCRMEvents.OnCRMForce, IComCRMEvents::OnCRMForce, OnCRMForce, OnCRMForce method [COM+], OnCRMForce method [COM+],IComCRMEvents interface, _dtc_IComCRMEvents_OnCRMForce, comsvcs/IComCRMEvents::OnCRMForce, cos.icomcrmevents_oncrmforce
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
 - IComCRMEvents::OnCRMForce
 - comsvcs/IComCRMEvents::OnCRMForce
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
 - IComCRMEvents.OnCRMForce
---

# IComCRMEvents::OnCRMForce


## -description

Generated when a CRM clerk receives a request to force log records to disk, either from the CRM worker or from the CRM compensator.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.

### -param guidClerkCLSID [in]

The identifier of the CRM clerk.

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomcrmevents">IComCRMEvents</a>