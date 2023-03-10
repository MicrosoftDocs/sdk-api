---
UID: NF:comsvcs.IComCRMEvents.OnCRMCommit
title: IComCRMEvents::OnCRMCommit (comsvcs.h)
description: Generated when CRM clerk receives a commit notification to pass on to the CRM compensator.
helpviewer_keywords: ["IComCRMEvents interface [COM+]","OnCRMCommit method","IComCRMEvents.OnCRMCommit","IComCRMEvents::OnCRMCommit","OnCRMCommit","OnCRMCommit method [COM+]","OnCRMCommit method [COM+]","IComCRMEvents interface","_dtc_IComCRMEvents_OnCRMCommit","comsvcs/IComCRMEvents::OnCRMCommit","cos.icomcrmevents_oncrmcommit"]
old-location: cos\icomcrmevents_oncrmcommit.htm
tech.root: cos
ms.assetid: 76b87452-fa29-49f7-acc8-2ae2039757b0
ms.date: 12/05/2018
ms.keywords: IComCRMEvents interface [COM+],OnCRMCommit method, IComCRMEvents.OnCRMCommit, IComCRMEvents::OnCRMCommit, OnCRMCommit, OnCRMCommit method [COM+], OnCRMCommit method [COM+],IComCRMEvents interface, _dtc_IComCRMEvents_OnCRMCommit, comsvcs/IComCRMEvents::OnCRMCommit, cos.icomcrmevents_oncrmcommit
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
 - IComCRMEvents::OnCRMCommit
 - comsvcs/IComCRMEvents::OnCRMCommit
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
 - IComCRMEvents.OnCRMCommit
---

# IComCRMEvents::OnCRMCommit


## -description

Generated when CRM clerk receives a commit notification to pass on to the CRM compensator.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.

### -param guidClerkCLSID [in]

The identifier of the CRM clerk.

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomcrmevents">IComCRMEvents</a>