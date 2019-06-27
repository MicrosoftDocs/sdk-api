---
UID: NF:comsvcs.ICrmCompensatorVariants.EndAbortVariants
title: ICrmCompensatorVariants::EndAbortVariants (comsvcs.h)
author: windows-sdk-content
description: Notifies the CRM Compensator that it has received all the log records available during the abort phase.
old-location: cos\icrmcompensatorvariants_endabortvariants.htm
tech.root: cossdk
ms.assetid: 021880c3-e52c-4fa7-9815-3180ee1564da
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EndAbortVariants, EndAbortVariants method [COM+], EndAbortVariants method [COM+],ICrmCompensatorVariants interface, ICrmCompensatorVariants interface [COM+],EndAbortVariants method, ICrmCompensatorVariants.EndAbortVariants, ICrmCompensatorVariants::EndAbortVariants, _dtc_ICrmCompensatorVariants_EndAbortVariants, comsvcs/ICrmCompensatorVariants::EndAbortVariants, cos.icrmcompensatorvariants_endabortvariants
ms.topic: method
f1_keywords: 
 - "comsvcs/ICrmCompensatorVariants.EndAbortVariants"
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
 - ICrmCompensatorVariants.EndAbortVariants
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICrmCompensatorVariants::EndAbortVariants


## -description


Notifies the CRM Compensator that it has received all the log records available during the abort phase. All log records for this transaction can be discarded from the log after this method has completed.



## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-icrmcompensatorvariants">ICrmCompensatorVariants</a>
 

 

