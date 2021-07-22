---
UID: NF:sbtsv.ITsSbProvisioning.CancelJob
title: ITsSbProvisioning::CancelJob (sbtsv.h)
description: Cancels a provisioning job.
helpviewer_keywords: ["CancelJob","CancelJob method [Remote Desktop Services]","CancelJob method [Remote Desktop Services]","ITsSbProvisioning interface","ITsSbProvisioning interface [Remote Desktop Services]","CancelJob method","ITsSbProvisioning.CancelJob","ITsSbProvisioning::CancelJob","sbtsv/ITsSbProvisioning::CancelJob","termserv.itssbprovisioning_canceljob"]
old-location: termserv\itssbprovisioning_canceljob.htm
tech.root: TermServ
ms.assetid: c0496a8c-00ec-43a4-a7c2-071acb6b068a
ms.date: 12/05/2018
ms.keywords: CancelJob, CancelJob method [Remote Desktop Services], CancelJob method [Remote Desktop Services],ITsSbProvisioning interface, ITsSbProvisioning interface [Remote Desktop Services],CancelJob method, ITsSbProvisioning.CancelJob, ITsSbProvisioning::CancelJob, sbtsv/ITsSbProvisioning::CancelJob, termserv.itssbprovisioning_canceljob
req.header: sbtsv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sbtsv.idl
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
 - ITsSbProvisioning::CancelJob
 - sbtsv/ITsSbProvisioning::CancelJob
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbtsv.h
api_name:
 - ITsSbProvisioning.CancelJob
---

# ITsSbProvisioning::CancelJob


## -description

Cancels a provisioning job.

## -parameters

### -param JobGuid [in]

A <b>GUID</b> that identifies the job.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovisioning">ITsSbProvisioning</a>