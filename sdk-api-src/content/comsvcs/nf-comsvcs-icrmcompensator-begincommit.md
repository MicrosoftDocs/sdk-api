---
UID: NF:comsvcs.ICrmCompensator.BeginCommit
title: ICrmCompensator::BeginCommit (comsvcs.h)
description: Notifies the CRM Compensator of the commit phase of the transaction completion and that records are about to be delivered.
helpviewer_keywords: ["BeginCommit","BeginCommit method [COM+]","BeginCommit method [COM+]","ICrmCompensator interface","ICrmCompensator interface [COM+]","BeginCommit method","ICrmCompensator.BeginCommit","ICrmCompensator::BeginCommit","_dtc_ICrmCompensator_BeginCommit","comsvcs/ICrmCompensator::BeginCommit","cos.icrmcompensator_begincommit"]
old-location: cos\icrmcompensator_begincommit.htm
tech.root: cos
ms.assetid: 350f91f9-b019-4c70-9c3e-0d567479d3d0
ms.date: 12/05/2018
ms.keywords: BeginCommit, BeginCommit method [COM+], BeginCommit method [COM+],ICrmCompensator interface, ICrmCompensator interface [COM+],BeginCommit method, ICrmCompensator.BeginCommit, ICrmCompensator::BeginCommit, _dtc_ICrmCompensator_BeginCommit, comsvcs/ICrmCompensator::BeginCommit, cos.icrmcompensator_begincommit
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
 - ICrmCompensator::BeginCommit
 - comsvcs/ICrmCompensator::BeginCommit
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
 - ICrmCompensator.BeginCommit
---

# ICrmCompensator::BeginCommit


## -description

Notifies the CRM Compensator of the commit phase of the transaction completion and that records are about to be delivered.

## -parameters

### -param fRecovery [in]

Indicates whether this method is being called during recovery (TRUE) or normal processing (FALSE).

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The commit or abort phases are received by the compensator without a prepare phase during recovery. Also, the abort phase can be received during normal processing without a prepare phase if the client decides to initiate abort.

The CRM Compensator should not depend on any state to be maintained between the prepare and commit/abort phases; the CRM infrastructure is free to release the CRM Compensator between these two phases if it needs to do so. However, state is maintained between the Begin-Record-End calls, and the CRM Compensator always gets the <a href="/windows/desktop/api/comsvcs/nn-comsvcs-icrmlogcontrol">ICrmLogControl</a> interface before delivery of any transaction outcome methods.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icrmcompensator">ICrmCompensator</a>