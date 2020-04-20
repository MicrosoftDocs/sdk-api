---
UID: NF:comsvcs.ICrmCompensatorVariants.EndPrepareVariants
title: ICrmCompensatorVariants::EndPrepareVariants (comsvcs.h)
description: Notifies the CRM Compensator that it has had all the log records available during the prepare phase.helpviewer_keywords: ["EndPrepareVariants","EndPrepareVariants method [COM+]","EndPrepareVariants method [COM+]","ICrmCompensatorVariants interface","ICrmCompensatorVariants interface [COM+]","EndPrepareVariants method","ICrmCompensatorVariants.EndPrepareVariants","ICrmCompensatorVariants::EndPrepareVariants","_dtc_ICrmCompensatorVariants_EndPrepareVariants","comsvcs/ICrmCompensatorVariants::EndPrepareVariants","cos.icrmcompensatorvariants_endpreparevariants"]
old-location: cos\icrmcompensatorvariants_endpreparevariants.htm
tech.root: cossdk
ms.assetid: 2b9a7e75-5e7c-4f5b-b625-78abb3c5e9b7
ms.date: 12/05/2018
ms.keywords: EndPrepareVariants, EndPrepareVariants method [COM+], EndPrepareVariants method [COM+],ICrmCompensatorVariants interface, ICrmCompensatorVariants interface [COM+],EndPrepareVariants method, ICrmCompensatorVariants.EndPrepareVariants, ICrmCompensatorVariants::EndPrepareVariants, _dtc_ICrmCompensatorVariants_EndPrepareVariants, comsvcs/ICrmCompensatorVariants::EndPrepareVariants, cos.icrmcompensatorvariants_endpreparevariants
f1_keywords:
- comsvcs/ICrmCompensatorVariants.EndPrepareVariants
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
- ICrmCompensatorVariants.EndPrepareVariants
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICrmCompensatorVariants::EndPrepareVariants


## -description


Notifies the CRM Compensator that it has had all the log records available during the prepare phase.


## -parameters




### -param pbOkToPrepare [out]

Indicates whether the prepare phase succeeded, in which case it is OK to commit this transaction.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-icrmcompensatorvariants">ICrmCompensatorVariants</a>
 

 

