---
UID: NF:comsvcs.ICrmCompensatorVariants.EndCommitVariants
title: ICrmCompensatorVariants::EndCommitVariants
author: windows-sdk-content
description: Notifies the CRM Compensator that it has delivered all the log records available during the commit phase.
old-location: cos\icrmcompensatorvariants_endcommitvariants.htm
tech.root: cossdk
ms.assetid: 1004437b-0281-439c-9b6d-0043caeb2844
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: EndCommitVariants, EndCommitVariants method [COM+], EndCommitVariants method [COM+],ICrmCompensatorVariants interface, ICrmCompensatorVariants interface [COM+],EndCommitVariants method, ICrmCompensatorVariants.EndCommitVariants, ICrmCompensatorVariants::EndCommitVariants, _dtc_ICrmCompensatorVariants_EndCommitVariants, comsvcs/ICrmCompensatorVariants::EndCommitVariants, cos.icrmcompensatorvariants_endcommitvariants
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - ICrmCompensatorVariants.EndCommitVariants
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- comsvcs.h
: 
- ICrmCompensatorVariants.EndCommitVariants
: 
---

# ICrmCompensatorVariants::EndCommitVariants


## -description


Notifies the CRM Compensator that it has delivered all the log records available during the commit phase. All log records for this transaction can be discarded from the log after this method has completed.



## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/44b80062-b2bb-4c34-b9e1-31229c8e40ca">ICrmCompensatorVariants</a>
 

 

