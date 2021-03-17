---
UID: NF:comsvcs.IComCRMEvents.OnCRMAbort
title: IComCRMEvents::OnCRMAbort (comsvcs.h)
description: Generated when CRM clerk receives an abort notification to pass on to the CRM compensator.
helpviewer_keywords: ["IComCRMEvents interface [COM+]","OnCRMAbort method","IComCRMEvents.OnCRMAbort","IComCRMEvents::OnCRMAbort","OnCRMAbort","OnCRMAbort method [COM+]","OnCRMAbort method [COM+]","IComCRMEvents interface","_dtc_IComCRMEvents_OnCRMAbort","comsvcs/IComCRMEvents::OnCRMAbort","cos.icomcrmevents_oncrmabort"]
old-location: cos\icomcrmevents_oncrmabort.htm
tech.root: cos
ms.assetid: 9def1696-8bc7-4294-a848-ff8ad2632ed6
ms.date: 12/05/2018
ms.keywords: IComCRMEvents interface [COM+],OnCRMAbort method, IComCRMEvents.OnCRMAbort, IComCRMEvents::OnCRMAbort, OnCRMAbort, OnCRMAbort method [COM+], OnCRMAbort method [COM+],IComCRMEvents interface, _dtc_IComCRMEvents_OnCRMAbort, comsvcs/IComCRMEvents::OnCRMAbort, cos.icomcrmevents_oncrmabort
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
 - IComCRMEvents::OnCRMAbort
 - comsvcs/IComCRMEvents::OnCRMAbort
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
 - IComCRMEvents.OnCRMAbort
---

# IComCRMEvents::OnCRMAbort


## -description

Generated when CRM clerk receives an abort notification to pass on to the CRM compensator.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.

### -param guidClerkCLSID [in]

The identifier of the CRM clerk.

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomcrmevents">IComCRMEvents</a>