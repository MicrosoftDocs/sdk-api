---
UID: NF:comsvcs.ICrmCompensatorVariants.EndPrepareVariants
title: ICrmCompensatorVariants::EndPrepareVariants (comsvcs.h)
description: Notifies the CRM Compensator that it has had all the log records available during the prepare phase. (ICrmCompensatorVariants.EndPrepareVariants)
helpviewer_keywords: ["EndPrepareVariants","EndPrepareVariants method [COM+]","EndPrepareVariants method [COM+]","ICrmCompensatorVariants interface","ICrmCompensatorVariants interface [COM+]","EndPrepareVariants method","ICrmCompensatorVariants.EndPrepareVariants","ICrmCompensatorVariants::EndPrepareVariants","_dtc_ICrmCompensatorVariants_EndPrepareVariants","comsvcs/ICrmCompensatorVariants::EndPrepareVariants","cos.icrmcompensatorvariants_endpreparevariants"]
old-location: cos\icrmcompensatorvariants_endpreparevariants.htm
tech.root: cos
ms.assetid: 2b9a7e75-5e7c-4f5b-b625-78abb3c5e9b7
ms.date: 12/05/2018
ms.keywords: EndPrepareVariants, EndPrepareVariants method [COM+], EndPrepareVariants method [COM+],ICrmCompensatorVariants interface, ICrmCompensatorVariants interface [COM+],EndPrepareVariants method, ICrmCompensatorVariants.EndPrepareVariants, ICrmCompensatorVariants::EndPrepareVariants, _dtc_ICrmCompensatorVariants_EndPrepareVariants, comsvcs/ICrmCompensatorVariants::EndPrepareVariants, cos.icrmcompensatorvariants_endpreparevariants
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
 - ICrmCompensatorVariants::EndPrepareVariants
 - comsvcs/ICrmCompensatorVariants::EndPrepareVariants
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
 - ICrmCompensatorVariants.EndPrepareVariants
---

# ICrmCompensatorVariants::EndPrepareVariants


## -description

Notifies the CRM Compensator that it has had all the log records available during the prepare phase.

## -parameters

### -param pbOkToPrepare [out]

Indicates whether the prepare phase succeeded, in which case it is OK to commit this transaction.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icrmcompensatorvariants">ICrmCompensatorVariants</a>
