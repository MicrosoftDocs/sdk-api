---
UID: NF:comsvcs.ICrmCompensatorVariants.EndCommitVariants
title: ICrmCompensatorVariants::EndCommitVariants (comsvcs.h)
description: Notifies the CRM Compensator that it has delivered all the log records available during the commit phase. (ICrmCompensatorVariants.EndCommitVariants)
helpviewer_keywords: ["EndCommitVariants","EndCommitVariants method [COM+]","EndCommitVariants method [COM+]","ICrmCompensatorVariants interface","ICrmCompensatorVariants interface [COM+]","EndCommitVariants method","ICrmCompensatorVariants.EndCommitVariants","ICrmCompensatorVariants::EndCommitVariants","_dtc_ICrmCompensatorVariants_EndCommitVariants","comsvcs/ICrmCompensatorVariants::EndCommitVariants","cos.icrmcompensatorvariants_endcommitvariants"]
old-location: cos\icrmcompensatorvariants_endcommitvariants.htm
tech.root: cos
ms.assetid: 1004437b-0281-439c-9b6d-0043caeb2844
ms.date: 12/05/2018
ms.keywords: EndCommitVariants, EndCommitVariants method [COM+], EndCommitVariants method [COM+],ICrmCompensatorVariants interface, ICrmCompensatorVariants interface [COM+],EndCommitVariants method, ICrmCompensatorVariants.EndCommitVariants, ICrmCompensatorVariants::EndCommitVariants, _dtc_ICrmCompensatorVariants_EndCommitVariants, comsvcs/ICrmCompensatorVariants::EndCommitVariants, cos.icrmcompensatorvariants_endcommitvariants
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
 - ICrmCompensatorVariants::EndCommitVariants
 - comsvcs/ICrmCompensatorVariants::EndCommitVariants
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
 - ICrmCompensatorVariants.EndCommitVariants
---

# ICrmCompensatorVariants::EndCommitVariants


## -description

Notifies the CRM Compensator that it has delivered all the log records available during the commit phase. All log records for this transaction can be discarded from the log after this method has completed.



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icrmcompensatorvariants">ICrmCompensatorVariants</a>
