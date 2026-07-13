---
UID: NF:comsvcs.ICrmCompensator.EndCommit
title: ICrmCompensator::EndCommit (comsvcs.h)
description: Notifies the CRM Compensator that it has delivered all the log records available during the commit phase. (ICrmCompensator.EndCommit)
helpviewer_keywords: ["EndCommit","EndCommit method [COM+]","EndCommit method [COM+]","ICrmCompensator interface","ICrmCompensator interface [COM+]","EndCommit method","ICrmCompensator.EndCommit","ICrmCompensator::EndCommit","_dtc_ICrmCompensator_EndCommit","comsvcs/ICrmCompensator::EndCommit","cos.icrmcompensator_endcommit"]
old-location: cos\icrmcompensator_endcommit.htm
tech.root: cos
ms.assetid: 83701797-c386-4471-91ed-cbe936b1988e
ms.date: 12/05/2018
ms.keywords: EndCommit, EndCommit method [COM+], EndCommit method [COM+],ICrmCompensator interface, ICrmCompensator interface [COM+],EndCommit method, ICrmCompensator.EndCommit, ICrmCompensator::EndCommit, _dtc_ICrmCompensator_EndCommit, comsvcs/ICrmCompensator::EndCommit, cos.icrmcompensator_endcommit
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
 - ICrmCompensator::EndCommit
 - comsvcs/ICrmCompensator::EndCommit
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
 - ICrmCompensator.EndCommit
---

# ICrmCompensator::EndCommit


## -description

Notifies the CRM Compensator that it has delivered all the log records available during the commit phase. All log records for this transaction can be discarded from the log after this method has completed.



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icrmcompensator">ICrmCompensator</a>
