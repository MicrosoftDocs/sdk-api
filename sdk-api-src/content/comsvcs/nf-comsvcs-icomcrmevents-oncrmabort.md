---
UID: NF:comsvcs.IComCRMEvents.OnCRMAbort
title: IComCRMEvents::OnCRMAbort
author: windows-sdk-content
description: Generated when CRM clerk receives an abort notification to pass on to the CRM compensator.
old-location: cos\icomcrmevents_oncrmabort.htm
old-project: cossdk
ms.assetid: 9def1696-8bc7-4294-a848-ff8ad2632ed6
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IComCRMEvents interface [COM+],OnCRMAbort method, IComCRMEvents.OnCRMAbort, IComCRMEvents::OnCRMAbort, OnCRMAbort, OnCRMAbort method [COM+], OnCRMAbort method [COM+],IComCRMEvents interface, _dtc_IComCRMEvents_OnCRMAbort, comsvcs/IComCRMEvents::OnCRMAbort, cos.icomcrmevents_oncrmabort
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
 - IComCRMEvents.OnCRMAbort
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IComCRMEvents::OnCRMAbort


## -description


Generated when CRM clerk receives an abort notification to pass on to the CRM compensator.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/f4aa0892-4c93-42ea-adc6-1b304b917389">COMSVCSEVENTINFO</a> structure.


### -param guidClerkCLSID [in]

The identifier of the CRM clerk.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/720beffb-8fb5-4c87-9bcf-6db214543b01">IComCRMEvents</a>
 

 

