---
UID: NF:comsvcs.IComCRMEvents.OnCRMRelease
title: IComCRMEvents::OnCRMRelease (comsvcs.h)
description: Generated when the CRM clerk is finished and releases its resource locks.
helpviewer_keywords: ["IComCRMEvents interface [COM+]","OnCRMRelease method","IComCRMEvents.OnCRMRelease","IComCRMEvents::OnCRMRelease","OnCRMRelease","OnCRMRelease method [COM+]","OnCRMRelease method [COM+]","IComCRMEvents interface","_dtc_IComCRMEvents_OnCRMRelease","comsvcs/IComCRMEvents::OnCRMRelease","cos.icomcrmevents_oncrmrelease"]
old-location: cos\icomcrmevents_oncrmrelease.htm
tech.root: cos
ms.assetid: e97b6cbf-1e78-475b-9dc7-baa4c05f1a6b
ms.date: 12/05/2018
ms.keywords: IComCRMEvents interface [COM+],OnCRMRelease method, IComCRMEvents.OnCRMRelease, IComCRMEvents::OnCRMRelease, OnCRMRelease, OnCRMRelease method [COM+], OnCRMRelease method [COM+],IComCRMEvents interface, _dtc_IComCRMEvents_OnCRMRelease, comsvcs/IComCRMEvents::OnCRMRelease, cos.icomcrmevents_oncrmrelease
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
 - IComCRMEvents::OnCRMRelease
 - comsvcs/IComCRMEvents::OnCRMRelease
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
 - IComCRMEvents.OnCRMRelease
---

# IComCRMEvents::OnCRMRelease


## -description

Generated when the CRM clerk is finished and releases its resource locks.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.

### -param guidClerkCLSID [in]

The identifier of the CRM clerk.

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomcrmevents">IComCRMEvents</a>