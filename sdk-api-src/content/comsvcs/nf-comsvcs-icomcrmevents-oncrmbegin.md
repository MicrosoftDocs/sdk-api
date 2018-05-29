---
UID: NF:comsvcs.IComCRMEvents.OnCRMBegin
title: IComCRMEvents::OnCRMBegin
author: windows-sdk-content
description: Generated when a CRM clerk is starting, either due to a client registering a compensator or during recovery.
old-location: cos\icomcrmevents_oncrmbegin.htm
old-project: cossdk
ms.assetid: 8975cb5e-024f-40bf-acd7-c5af0abd88a0
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: IComCRMEvents interface [COM+],OnCRMBegin method, IComCRMEvents.OnCRMBegin, IComCRMEvents::OnCRMBegin, OnCRMBegin, OnCRMBegin method [COM+], OnCRMBegin method [COM+],IComCRMEvents interface, _dtc_IComCRMEvents_OnCRMBegin, comsvcs/IComCRMEvents::OnCRMBegin, cos.icomcrmevents_oncrmbegin
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
req.typenames: TRACKING_COLL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComSvcs.h
api_name:
-	IComCRMEvents.OnCRMBegin
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IComCRMEvents::OnCRMBegin


## -description


Generated when a CRM clerk is starting, either due to a client registering a compensator or during recovery.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/f4aa0892-4c93-42ea-adc6-1b304b917389">COMSVCSEVENTINFO</a> structure.


### -param guidClerkCLSID [in]

The identifier of the CRM clerk.


### -param guidActivity [in]

The activity identifier (NULL if recovery).


### -param guidTx [in]

The identifier of the Transaction Unit Of Work (UOW).


### -param szProgIdCompensator [in]

The ProgID of the CRM compensator.


### -param szDescription [in]

The description (blank if recovery).


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/720beffb-8fb5-4c87-9bcf-6db214543b01">IComCRMEvents</a>
 

 

