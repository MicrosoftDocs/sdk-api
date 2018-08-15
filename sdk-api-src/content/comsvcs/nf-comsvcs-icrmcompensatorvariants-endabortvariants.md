---
UID: NF:comsvcs.ICrmCompensatorVariants.EndAbortVariants
title: ICrmCompensatorVariants::EndAbortVariants
author: windows-sdk-content
description: Notifies the CRM Compensator that it has received all the log records available during the abort phase.
old-location: cos\icrmcompensatorvariants_endabortvariants.htm
old-project: cossdk
ms.assetid: 021880c3-e52c-4fa7-9815-3180ee1564da
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: EndAbortVariants, EndAbortVariants method [COM+], EndAbortVariants method [COM+],ICrmCompensatorVariants interface, ICrmCompensatorVariants interface [COM+],EndAbortVariants method, ICrmCompensatorVariants.EndAbortVariants, ICrmCompensatorVariants::EndAbortVariants, _dtc_ICrmCompensatorVariants_EndAbortVariants, comsvcs/ICrmCompensatorVariants::EndAbortVariants, cos.icrmcompensatorvariants_endabortvariants
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: comsvcs.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: TRACKING_COLL_TYPE
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
req.lib: 
req.dll: 
req.irql: 
---

# ICrmCompensatorVariants::EndAbortVariants


## -description


Notifies the CRM Compensator that it has received all the log records available during the abort phase. All log records for this transaction can be discarded from the log after this method has completed.



## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/44b80062-b2bb-4c34-b9e1-31229c8e40ca">ICrmCompensatorVariants</a>
 

 

