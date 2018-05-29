---
UID: NF:comsvcs.IComCRMEvents.OnCRMWrite
title: IComCRMEvents::OnCRMWrite
author: windows-sdk-content
description: Generated when a CRM clerk receives a request to write a log record, either from the CRM worker or CRM compensator.
old-location: cos\icomcrmevents_oncrmwrite.htm
old-project: cossdk
ms.assetid: 095452e3-a38d-4602-a925-8fa6445ddbc8
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: IComCRMEvents interface [COM+],OnCRMWrite method, IComCRMEvents.OnCRMWrite, IComCRMEvents::OnCRMWrite, OnCRMWrite, OnCRMWrite method [COM+], OnCRMWrite method [COM+],IComCRMEvents interface, _dtc_IComCRMEvents_OnCRMWrite, comsvcs/IComCRMEvents::OnCRMWrite, cos.icomcrmevents_oncrmwrite
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
-	IComCRMEvents.OnCRMWrite
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IComCRMEvents::OnCRMWrite


## -description


Generated when a CRM clerk receives a request to write a log record, either from the CRM worker or CRM compensator.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/f4aa0892-4c93-42ea-adc6-1b304b917389">COMSVCSEVENTINFO</a> structure.


### -param guidClerkCLSID [in]

The identifier of the CRM clerk.


### -param fVariants [in]

Indicates whether the log record is being written as a <b>Variant</b> array.


### -param dwRecordSize [in]

The log record size (approximate).


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/720beffb-8fb5-4c87-9bcf-6db214543b01">IComCRMEvents</a>
 

 

