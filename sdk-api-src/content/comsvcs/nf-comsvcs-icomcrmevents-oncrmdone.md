---
UID: NF:comsvcs.IComCRMEvents.OnCRMDone
title: IComCRMEvents::OnCRMDone
author: windows-sdk-content
description: Generated when CRM clerk is done processing transaction outcome notifications.
old-location: cos\icomcrmevents_oncrmdone.htm
old-project: cossdk
ms.assetid: 8845fd4d-a1a8-40cf-9359-5a2900432f32
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: IComCRMEvents interface [COM+],OnCRMDone method, IComCRMEvents.OnCRMDone, IComCRMEvents::OnCRMDone, OnCRMDone, OnCRMDone method [COM+], OnCRMDone method [COM+],IComCRMEvents interface, _dtc_IComCRMEvents_OnCRMDone, comsvcs/IComCRMEvents::OnCRMDone, cos.icomcrmevents_oncrmdone
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
 - IComCRMEvents.OnCRMDone
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IComCRMEvents::OnCRMDone


## -description


Generated when CRM clerk is done processing transaction outcome notifications.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/f4aa0892-4c93-42ea-adc6-1b304b917389">COMSVCSEVENTINFO</a> structure.


### -param guidClerkCLSID [in]

The identifier of the CRM clerk.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/720beffb-8fb5-4c87-9bcf-6db214543b01">IComCRMEvents</a>
 

 

