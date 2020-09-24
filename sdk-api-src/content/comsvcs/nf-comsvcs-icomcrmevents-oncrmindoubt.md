---
UID: NF:comsvcs.IComCRMEvents.OnCRMIndoubt
title: IComCRMEvents::OnCRMIndoubt (comsvcs.h)
description: Generated when CRM clerk receives an in-doubt notification to pass on to the CRM compensator.
helpviewer_keywords: ["IComCRMEvents interface [COM+]","OnCRMIndoubt method","IComCRMEvents.OnCRMIndoubt","IComCRMEvents::OnCRMIndoubt","OnCRMIndoubt","OnCRMIndoubt method [COM+]","OnCRMIndoubt method [COM+]","IComCRMEvents interface","_dtc_IComCRMEvents_OnCRMIndoubt","comsvcs/IComCRMEvents::OnCRMIndoubt","cos.icomcrmevents_oncrmindoubt"]
old-location: cos\icomcrmevents_oncrmindoubt.htm
tech.root: cos
ms.assetid: b1144b7c-097f-4a1c-b7d7-d71b8108625b
ms.date: 12/05/2018
ms.keywords: IComCRMEvents interface [COM+],OnCRMIndoubt method, IComCRMEvents.OnCRMIndoubt, IComCRMEvents::OnCRMIndoubt, OnCRMIndoubt, OnCRMIndoubt method [COM+], OnCRMIndoubt method [COM+],IComCRMEvents interface, _dtc_IComCRMEvents_OnCRMIndoubt, comsvcs/IComCRMEvents::OnCRMIndoubt, cos.icomcrmevents_oncrmindoubt
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
 - IComCRMEvents::OnCRMIndoubt
 - comsvcs/IComCRMEvents::OnCRMIndoubt
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
 - IComCRMEvents.OnCRMIndoubt
---

# IComCRMEvents::OnCRMIndoubt


## -description

Generated when CRM clerk receives an in-doubt notification to pass on to the CRM compensator.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.

### -param guidClerkCLSID [in]

The identifier of the CRM clerk.

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomcrmevents">IComCRMEvents</a>