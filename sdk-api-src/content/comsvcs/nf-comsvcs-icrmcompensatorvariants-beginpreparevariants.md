---
UID: NF:comsvcs.ICrmCompensatorVariants.BeginPrepareVariants
title: ICrmCompensatorVariants::BeginPrepareVariants (comsvcs.h)
description: Notifies the CRM Compensator of the prepare phase of the transaction completion and that records are about to be delivered.
helpviewer_keywords: ["BeginPrepareVariants","BeginPrepareVariants method [COM+]","BeginPrepareVariants method [COM+]","ICrmCompensatorVariants interface","ICrmCompensatorVariants interface [COM+]","BeginPrepareVariants method","ICrmCompensatorVariants.BeginPrepareVariants","ICrmCompensatorVariants::BeginPrepareVariants","_dtc_ICrmCompensatorVariants_BeginPrepareVariants","comsvcs/ICrmCompensatorVariants::BeginPrepareVariants","cos.icrmcompensatorvariants_beginpreparevariants"]
old-location: cos\icrmcompensatorvariants_beginpreparevariants.htm
tech.root: cos
ms.assetid: f0cbfc39-2a29-4b1f-8d6e-87d0b1c68582
ms.date: 12/05/2018
ms.keywords: BeginPrepareVariants, BeginPrepareVariants method [COM+], BeginPrepareVariants method [COM+],ICrmCompensatorVariants interface, ICrmCompensatorVariants interface [COM+],BeginPrepareVariants method, ICrmCompensatorVariants.BeginPrepareVariants, ICrmCompensatorVariants::BeginPrepareVariants, _dtc_ICrmCompensatorVariants_BeginPrepareVariants, comsvcs/ICrmCompensatorVariants::BeginPrepareVariants, cos.icrmcompensatorvariants_beginpreparevariants
f1_keywords:
- comsvcs/ICrmCompensatorVariants.BeginPrepareVariants
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- ComSvcs.h
api_name:
- ICrmCompensatorVariants.BeginPrepareVariants
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICrmCompensatorVariants::BeginPrepareVariants


## -description


Notifies the CRM Compensator of the prepare phase of the transaction completion and that records are about to be delivered.

Prepare notifications are never received during recovery, only during normal processing.




## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-icrmcompensatorvariants">ICrmCompensatorVariants</a>
 

 

