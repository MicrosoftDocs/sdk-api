---
UID: NF:comsvcs.ICrmCompensatorVariants.SetLogControlVariants
title: ICrmCompensatorVariants::SetLogControlVariants method
author: windows-driver-content
description: Delivers an ICrmLogControl interface to the CRM Compensator.
old-location: cos\icrmcompensatorvariants_setlogcontrolvariants.htm
old-project: cossdk
ms.assetid: 5cf602fb-b5b9-471b-b617-9df6725eaf35
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: ICrmCompensatorVariants, ICrmCompensatorVariants interface [COM+], SetLogControlVariants method, ICrmCompensatorVariants::SetLogControlVariants, SetLogControlVariants method [COM+], SetLogControlVariants method [COM+], ICrmCompensatorVariants interface, SetLogControlVariants,ICrmCompensatorVariants.SetLogControlVariants, _dtc_ICrmCompensatorVariants_SetLogControlVariants, comsvcs/ICrmCompensatorVariants::SetLogControlVariants, cos.icrmcompensatorvariants_setlogcontrolvariants
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
req.typenames: TRACKING_COLL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComSvcs.h
api_name:
-	ICrmCompensatorVariants.SetLogControlVariants
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICrmCompensatorVariants::SetLogControlVariants method


## -description


Delivers an <a href="https://msdn.microsoft.com/3309ed58-8161-46f3-93bc-afc0c9bc8d50">ICrmLogControl</a> interface to the CRM Compensator. This method is the first method called on the CRM Compensator after it has been created.


## -parameters




### -param pLogControl [in]

A pointer to the <a href="https://msdn.microsoft.com/3309ed58-8161-46f3-93bc-afc0c9bc8d50">ICrmLogControl</a> interface of the CRM clerk.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To write additional log records, use the <a href="https://msdn.microsoft.com/3309ed58-8161-46f3-93bc-afc0c9bc8d50">ICrmLogControl</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/44b80062-b2bb-4c34-b9e1-31229c8e40ca">ICrmCompensatorVariants</a>
 

 

