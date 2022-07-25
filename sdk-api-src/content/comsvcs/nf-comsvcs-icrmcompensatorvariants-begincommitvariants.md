---
UID: NF:comsvcs.ICrmCompensatorVariants.BeginCommitVariants
title: ICrmCompensatorVariants::BeginCommitVariants (comsvcs.h)
description: Notifies the CRM Compensator of the commit phase (phase two) of the transaction completion and that records are about to be delivered.
helpviewer_keywords: ["BeginCommitVariants","BeginCommitVariants method [COM+]","BeginCommitVariants method [COM+]","ICrmCompensatorVariants interface","ICrmCompensatorVariants interface [COM+]","BeginCommitVariants method","ICrmCompensatorVariants.BeginCommitVariants","ICrmCompensatorVariants::BeginCommitVariants","_dtc_ICrmCompensatorVariants_BeginCommitVariants","comsvcs/ICrmCompensatorVariants::BeginCommitVariants","cos.icrmcompensatorvariants_begincommitvariants"]
old-location: cos\icrmcompensatorvariants_begincommitvariants.htm
tech.root: cos
ms.assetid: a6cd7421-5173-4edb-b752-5fbc44bac6dc
ms.date: 12/05/2018
ms.keywords: BeginCommitVariants, BeginCommitVariants method [COM+], BeginCommitVariants method [COM+],ICrmCompensatorVariants interface, ICrmCompensatorVariants interface [COM+],BeginCommitVariants method, ICrmCompensatorVariants.BeginCommitVariants, ICrmCompensatorVariants::BeginCommitVariants, _dtc_ICrmCompensatorVariants_BeginCommitVariants, comsvcs/ICrmCompensatorVariants::BeginCommitVariants, cos.icrmcompensatorvariants_begincommitvariants
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
 - ICrmCompensatorVariants::BeginCommitVariants
 - comsvcs/ICrmCompensatorVariants::BeginCommitVariants
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
 - ICrmCompensatorVariants.BeginCommitVariants
---

# ICrmCompensatorVariants::BeginCommitVariants


## -description

Notifies the CRM Compensator of the commit phase (phase two) of the transaction completion and that records are about to be delivered.

## -parameters

### -param bRecovery [in]

Indicates whether this method is being called during recovery.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The CRM Compensator should not depend on any state to be maintained between the prepare phase and the commit phase. The CRM infrastructure is free to release the CRM Compensator between these two phases if it needs to do so. However, state is maintained between the Begin-Record-End calls, and the CRM Compensator always gets the <a href="/windows/desktop/api/comsvcs/nn-comsvcs-icrmlogcontrol">ICrmLogControl</a> interface before delivery of any transaction outcome methods.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icrmcompensatorvariants">ICrmCompensatorVariants</a>