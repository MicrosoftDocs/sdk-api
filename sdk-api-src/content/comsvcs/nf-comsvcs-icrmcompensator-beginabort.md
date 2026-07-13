---
UID: NF:comsvcs.ICrmCompensator.BeginAbort
title: ICrmCompensator::BeginAbort (comsvcs.h)
description: Notifies the CRM Compensator of the abort phase of the transaction completion and that records are about to be delivered. (ICrmCompensator.BeginAbort)
helpviewer_keywords: ["BeginAbort","BeginAbort method [COM+]","BeginAbort method [COM+]","ICrmCompensator interface","ICrmCompensator interface [COM+]","BeginAbort method","ICrmCompensator.BeginAbort","ICrmCompensator::BeginAbort","_dtc_ICrmCompensator_BeginAbort","comsvcs/ICrmCompensator::BeginAbort","cos.icrmcompensator_beginabort"]
old-location: cos\icrmcompensator_beginabort.htm
tech.root: cos
ms.assetid: 443d0a09-0f5f-4237-870b-5cc47c80e2fe
ms.date: 12/05/2018
ms.keywords: BeginAbort, BeginAbort method [COM+], BeginAbort method [COM+],ICrmCompensator interface, ICrmCompensator interface [COM+],BeginAbort method, ICrmCompensator.BeginAbort, ICrmCompensator::BeginAbort, _dtc_ICrmCompensator_BeginAbort, comsvcs/ICrmCompensator::BeginAbort, cos.icrmcompensator_beginabort
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
 - ICrmCompensator::BeginAbort
 - comsvcs/ICrmCompensator::BeginAbort
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
 - ICrmCompensator.BeginAbort
---

# ICrmCompensator::BeginAbort


## -description

Notifies the CRM Compensator of the abort phase of the transaction completion and that records are about to be delivered.

## -parameters

### -param fRecovery [in]

Indicates whether this method is being called during recovery.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The abort phase can be received during normal processing without a prepare phase should the client decide to initiate abort.

The CRM Compensator should not depend on any state to be maintained between the prepare phase and this phase; the CRM infrastructure is free to release the CRM Compensator between these two phases if it needs to do so. However, state is maintained between the Begin-Record-End calls, and the CRM Compensator always gets the <a href="/windows/desktop/api/comsvcs/nn-comsvcs-icrmlogcontrol">ICrmLogControl</a> interface before delivery of any transaction outcome methods.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icrmcompensator">ICrmCompensator</a>
