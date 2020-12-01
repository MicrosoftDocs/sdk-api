---
UID: NF:comsvcs.IComCRMEvents.OnCRMRecoveryStart
title: IComCRMEvents::OnCRMRecoveryStart (comsvcs.h)
description: Generated when CRM recovery has started.
helpviewer_keywords: ["IComCRMEvents interface [COM+]","OnCRMRecoveryStart method","IComCRMEvents.OnCRMRecoveryStart","IComCRMEvents::OnCRMRecoveryStart","OnCRMRecoveryStart","OnCRMRecoveryStart method [COM+]","OnCRMRecoveryStart method [COM+]","IComCRMEvents interface","_dtc_IComCRMEvents_OnCRMRecoveryStart","comsvcs/IComCRMEvents::OnCRMRecoveryStart","cos.icomcrmevents_oncrmrecoverystart"]
old-location: cos\icomcrmevents_oncrmrecoverystart.htm
tech.root: cos
ms.assetid: ac958f4b-1af4-4cfc-8fb4-92e89fdba771
ms.date: 12/05/2018
ms.keywords: IComCRMEvents interface [COM+],OnCRMRecoveryStart method, IComCRMEvents.OnCRMRecoveryStart, IComCRMEvents::OnCRMRecoveryStart, OnCRMRecoveryStart, OnCRMRecoveryStart method [COM+], OnCRMRecoveryStart method [COM+],IComCRMEvents interface, _dtc_IComCRMEvents_OnCRMRecoveryStart, comsvcs/IComCRMEvents::OnCRMRecoveryStart, cos.icomcrmevents_oncrmrecoverystart
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
 - IComCRMEvents::OnCRMRecoveryStart
 - comsvcs/IComCRMEvents::OnCRMRecoveryStart
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
 - IComCRMEvents.OnCRMRecoveryStart
---

# IComCRMEvents::OnCRMRecoveryStart


## -description

Generated when CRM recovery has started.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.

### -param guidApp [in]

The globally unique identifier (GUID) of the application.

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomcrmevents">IComCRMEvents</a>