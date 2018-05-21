---
UID: NF:comsvcs.IComCRMEvents.OnCRMForget
title: IComCRMEvents::OnCRMForget
author: windows-driver-content
description: Generated when a CRM clerk receives a request to forget a log record, either from the CRM worker or from the CRM compensator.
old-location: cos\icomcrmevents_oncrmforget.htm
old-project: cossdk
ms.assetid: 2e6c5bb1-aa99-434a-9376-c853b1fb1d12
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IComCRMEvents interface [COM+],OnCRMForget method, IComCRMEvents.OnCRMForget, IComCRMEvents::OnCRMForget, OnCRMForget, OnCRMForget method [COM+], OnCRMForget method [COM+],IComCRMEvents interface, _dtc_IComCRMEvents_OnCRMForget, comsvcs/IComCRMEvents::OnCRMForget, cos.icomcrmevents_oncrmforget
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
-	IComCRMEvents.OnCRMForget
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IComCRMEvents::OnCRMForget


## -description


Generated when a CRM clerk receives a request to forget a log record, either from the CRM worker or from the CRM compensator.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/f4aa0892-4c93-42ea-adc6-1b304b917389">COMSVCSEVENTINFO</a> structure.


### -param guidClerkCLSID [in]

The identifier of the CRM clerk.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/720beffb-8fb5-4c87-9bcf-6db214543b01">IComCRMEvents</a>
 

 

