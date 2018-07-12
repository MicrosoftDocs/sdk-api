---
UID: NF:comsvcs.IComCRMEvents.OnCRMIndoubt
title: IComCRMEvents::OnCRMIndoubt
author: windows-sdk-content
description: Generated when CRM clerk receives an in-doubt notification to pass on to the CRM compensator.
old-location: cos\icomcrmevents_oncrmindoubt.htm
old-project: cossdk
ms.assetid: b1144b7c-097f-4a1c-b7d7-d71b8108625b
ms.author: windowssdkdev
ms.date: 06/18/2018
ms.keywords: IComCRMEvents interface [COM+],OnCRMIndoubt method, IComCRMEvents.OnCRMIndoubt, IComCRMEvents::OnCRMIndoubt, OnCRMIndoubt, OnCRMIndoubt method [COM+], OnCRMIndoubt method [COM+],IComCRMEvents interface, _dtc_IComCRMEvents_OnCRMIndoubt, comsvcs/IComCRMEvents::OnCRMIndoubt, cos.icomcrmevents_oncrmindoubt
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
 - IComCRMEvents.OnCRMIndoubt
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IComCRMEvents::OnCRMIndoubt


## -description


Generated when CRM clerk receives an in-doubt notification to pass on to the CRM compensator.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/f4aa0892-4c93-42ea-adc6-1b304b917389">COMSVCSEVENTINFO</a> structure.


### -param guidClerkCLSID [in]

The identifier of the CRM clerk.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/720beffb-8fb5-4c87-9bcf-6db214543b01">IComCRMEvents</a>
 

 

