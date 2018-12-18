---
UID: NF:comsvcs.IComCRMEvents.OnCRMPrepare
title: IComCRMEvents::OnCRMPrepare
author: windows-sdk-content
description: Generated when CRM clerk receives a prepare notification to pass on to the CRM compensator.
old-location: cos\icomcrmevents_oncrmprepare.htm
tech.root: cossdk
ms.assetid: 16ecd4a5-6ca6-443d-ab03-f9ceb951ed13
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IComCRMEvents interface [COM+],OnCRMPrepare method, IComCRMEvents.OnCRMPrepare, IComCRMEvents::OnCRMPrepare, OnCRMPrepare, OnCRMPrepare method [COM+], OnCRMPrepare method [COM+],IComCRMEvents interface, _dtc_IComCRMEvents_OnCRMPrepare, comsvcs/IComCRMEvents::OnCRMPrepare, cos.icomcrmevents_oncrmprepare
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
 - IComCRMEvents.OnCRMPrepare
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IComCRMEvents::OnCRMPrepare


## -description


Generated when CRM clerk receives a prepare notification to pass on to the CRM compensator.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/f4aa0892-4c93-42ea-adc6-1b304b917389">COMSVCSEVENTINFO</a> structure.


### -param guidClerkCLSID [in]

The identifier of the CRM clerk.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/720beffb-8fb5-4c87-9bcf-6db214543b01">IComCRMEvents</a>
 

 

