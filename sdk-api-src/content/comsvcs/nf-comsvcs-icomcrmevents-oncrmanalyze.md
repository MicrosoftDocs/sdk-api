---
UID: NF:comsvcs.IComCRMEvents.OnCRMAnalyze
title: IComCRMEvents::OnCRMAnalyze (comsvcs.h)
description: Generated when a CRM clerk receives a record during the analysis phase of recovery.
helpviewer_keywords: ["IComCRMEvents interface [COM+]","OnCRMAnalyze method","IComCRMEvents.OnCRMAnalyze","IComCRMEvents::OnCRMAnalyze","OnCRMAnalyze","OnCRMAnalyze method [COM+]","OnCRMAnalyze method [COM+]","IComCRMEvents interface","_dtc_IComCRMEvents_OnCRMAnalyze","comsvcs/IComCRMEvents::OnCRMAnalyze","cos.icomcrmevents_oncrmanalyze"]
old-location: cos\icomcrmevents_oncrmanalyze.htm
tech.root: cos
ms.assetid: 08bdc192-f1f8-4d0d-a432-cf6316d8033a
ms.date: 12/05/2018
ms.keywords: IComCRMEvents interface [COM+],OnCRMAnalyze method, IComCRMEvents.OnCRMAnalyze, IComCRMEvents::OnCRMAnalyze, OnCRMAnalyze, OnCRMAnalyze method [COM+], OnCRMAnalyze method [COM+],IComCRMEvents interface, _dtc_IComCRMEvents_OnCRMAnalyze, comsvcs/IComCRMEvents::OnCRMAnalyze, cos.icomcrmevents_oncrmanalyze
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
 - IComCRMEvents::OnCRMAnalyze
 - comsvcs/IComCRMEvents::OnCRMAnalyze
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
 - IComCRMEvents.OnCRMAnalyze
---

# IComCRMEvents::OnCRMAnalyze


## -description

Generated when a CRM clerk receives a record during the analysis phase of recovery.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.

### -param guidClerkCLSID [in]

The identifier of the CRM clerk.

### -param dwCrmRecordType [in]

The CRM log record type (internal).

### -param dwRecordSize [in]

The log record size (approximate).

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomcrmevents">IComCRMEvents</a>