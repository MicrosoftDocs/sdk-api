---
UID: NF:comsvcs.IComCRMEvents.OnCRMRecoveryDone
title: IComCRMEvents::OnCRMRecoveryDone
author: windows-driver-content
description: Generated when CRM recovery is done.
old-location: cos\icomcrmevents_oncrmrecoverydone.htm
old-project: cossdk
ms.assetid: 533148f3-ecb4-495c-81c4-c75db7284ded
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: IComCRMEvents interface [COM+],OnCRMRecoveryDone method, IComCRMEvents.OnCRMRecoveryDone, IComCRMEvents::OnCRMRecoveryDone, OnCRMRecoveryDone, OnCRMRecoveryDone method [COM+], OnCRMRecoveryDone method [COM+],IComCRMEvents interface, _dtc_IComCRMEvents_OnCRMRecoveryDone, comsvcs/IComCRMEvents::OnCRMRecoveryDone, cos.icomcrmevents_oncrmrecoverydone
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
-	IComCRMEvents.OnCRMRecoveryDone
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IComCRMEvents::OnCRMRecoveryDone


## -description


Generated when CRM recovery is done.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/f4aa0892-4c93-42ea-adc6-1b304b917389">COMSVCSEVENTINFO</a> structure.


### -param guidApp [in]

The globally unique identifier (GUID) of the application.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/720beffb-8fb5-4c87-9bcf-6db214543b01">IComCRMEvents</a>
 

 

