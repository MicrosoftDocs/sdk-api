---
UID: NF:comsvcs.IComCRMEvents.OnCRMForget
title: IComCRMEvents::OnCRMForget (comsvcs.h)
description: Generated when a CRM clerk receives a request to forget a log record, either from the CRM worker or from the CRM compensator.
helpviewer_keywords: ["IComCRMEvents interface [COM+]","OnCRMForget method","IComCRMEvents.OnCRMForget","IComCRMEvents::OnCRMForget","OnCRMForget","OnCRMForget method [COM+]","OnCRMForget method [COM+]","IComCRMEvents interface","_dtc_IComCRMEvents_OnCRMForget","comsvcs/IComCRMEvents::OnCRMForget","cos.icomcrmevents_oncrmforget"]
old-location: cos\icomcrmevents_oncrmforget.htm
tech.root: cos
ms.assetid: 2e6c5bb1-aa99-434a-9376-c853b1fb1d12
ms.date: 12/05/2018
ms.keywords: IComCRMEvents interface [COM+],OnCRMForget method, IComCRMEvents.OnCRMForget, IComCRMEvents::OnCRMForget, OnCRMForget, OnCRMForget method [COM+], OnCRMForget method [COM+],IComCRMEvents interface, _dtc_IComCRMEvents_OnCRMForget, comsvcs/IComCRMEvents::OnCRMForget, cos.icomcrmevents_oncrmforget
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
 - IComCRMEvents::OnCRMForget
 - comsvcs/IComCRMEvents::OnCRMForget
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
 - IComCRMEvents.OnCRMForget
---

# IComCRMEvents::OnCRMForget


## -description

Generated when a CRM clerk receives a request to forget a log record, either from the CRM worker or from the CRM compensator.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.

### -param guidClerkCLSID [in]

The identifier of the CRM clerk.

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomcrmevents">IComCRMEvents</a>