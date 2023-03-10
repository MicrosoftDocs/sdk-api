---
UID: NF:comsvcs.ICrmCompensatorVariants.BeginAbortVariants
title: ICrmCompensatorVariants::BeginAbortVariants (comsvcs.h)
description: Notifies the CRM Compensator of the abort phase of the transaction completion and that records are about to be delivered. (ICrmCompensatorVariants.BeginAbortVariants)
helpviewer_keywords: ["BeginAbortVariants","BeginAbortVariants method [COM+]","BeginAbortVariants method [COM+]","ICrmCompensatorVariants interface","ICrmCompensatorVariants interface [COM+]","BeginAbortVariants method","ICrmCompensatorVariants.BeginAbortVariants","ICrmCompensatorVariants::BeginAbortVariants","_dtc_ICrmCompensatorVariants_BeginAbortVariants","comsvcs/ICrmCompensatorVariants::BeginAbortVariants","cos.icrmcompensatorvariants_beginabortvariants"]
old-location: cos\icrmcompensatorvariants_beginabortvariants.htm
tech.root: cos
ms.assetid: 485170e3-c69b-446a-af93-a0ed4f25c84a
ms.date: 12/05/2018
ms.keywords: BeginAbortVariants, BeginAbortVariants method [COM+], BeginAbortVariants method [COM+],ICrmCompensatorVariants interface, ICrmCompensatorVariants interface [COM+],BeginAbortVariants method, ICrmCompensatorVariants.BeginAbortVariants, ICrmCompensatorVariants::BeginAbortVariants, _dtc_ICrmCompensatorVariants_BeginAbortVariants, comsvcs/ICrmCompensatorVariants::BeginAbortVariants, cos.icrmcompensatorvariants_beginabortvariants
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
 - ICrmCompensatorVariants::BeginAbortVariants
 - comsvcs/ICrmCompensatorVariants::BeginAbortVariants
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
 - ICrmCompensatorVariants.BeginAbortVariants
---

# ICrmCompensatorVariants::BeginAbortVariants


## -description

Notifies the CRM Compensator of the abort phase of the transaction completion and that records are about to be delivered. The abort phase can be received during normal processing without a prepare phase if the client decides to initiate abort.

## -parameters

### -param bRecovery [in]

Indicates whether this method is being called during recovery.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The CRM Compensator should not depend on any state to be maintained between the prepare phase and the abort phase. The CRM infrastructure is free to release the CRM Compensator between these two phases if it needs to do so. However, state is maintained between the Begin-Record-End calls, and the CRM Compensator always gets the <a href="/windows/desktop/api/comsvcs/nn-comsvcs-icrmlogcontrol">ICrmLogControl</a> interface before delivery of any transaction outcome methods.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icrmcompensatorvariants">ICrmCompensatorVariants</a>
