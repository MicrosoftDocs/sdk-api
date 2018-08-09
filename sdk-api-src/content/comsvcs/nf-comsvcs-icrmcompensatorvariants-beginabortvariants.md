---
UID: NF:comsvcs.ICrmCompensatorVariants.BeginAbortVariants
title: ICrmCompensatorVariants::BeginAbortVariants
author: windows-sdk-content
description: Notifies the CRM Compensator of the abort phase of the transaction completion and that records are about to be delivered.
old-location: cos\icrmcompensatorvariants_beginabortvariants.htm
old-project: cossdk
ms.assetid: 485170e3-c69b-446a-af93-a0ed4f25c84a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: BeginAbortVariants, BeginAbortVariants method [COM+], BeginAbortVariants method [COM+],ICrmCompensatorVariants interface, ICrmCompensatorVariants interface [COM+],BeginAbortVariants method, ICrmCompensatorVariants.BeginAbortVariants, ICrmCompensatorVariants::BeginAbortVariants, _dtc_ICrmCompensatorVariants_BeginAbortVariants, comsvcs/ICrmCompensatorVariants::BeginAbortVariants, cos.icrmcompensatorvariants_beginabortvariants
ms.prod: windows
ms.technology: windows-sdk
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
 - ICrmCompensatorVariants.BeginAbortVariants
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICrmCompensatorVariants::BeginAbortVariants


## -description


Notifies the CRM Compensator of the abort phase of the transaction completion and that records are about to be delivered. The abort phase can be received during normal processing without a prepare phase if the client decides to initiate abort.



## -parameters




### -param bRecovery [in]

Indicates whether this method is being called during recovery.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The CRM Compensator should not depend on any state to be maintained between the prepare phase and the abort phase. The CRM infrastructure is free to release the CRM Compensator between these two phases if it needs to do so. However, state is maintained between the Begin-Record-End calls, and the CRM Compensator always gets the <a href="https://msdn.microsoft.com/3309ed58-8161-46f3-93bc-afc0c9bc8d50">ICrmLogControl</a> interface before delivery of any transaction outcome methods.






## -see-also




<a href="https://msdn.microsoft.com/44b80062-b2bb-4c34-b9e1-31229c8e40ca">ICrmCompensatorVariants</a>
 

 

