---
UID: NF:comsvcs.IComCRMEvents.OnCRMAnalyze
title: IComCRMEvents::OnCRMAnalyze
author: windows-sdk-content
description: Generated when a CRM clerk receives a record during the analysis phase of recovery.
old-location: cos\icomcrmevents_oncrmanalyze.htm
old-project: cossdk
ms.assetid: 08bdc192-f1f8-4d0d-a432-cf6316d8033a
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IComCRMEvents interface [COM+],OnCRMAnalyze method, IComCRMEvents.OnCRMAnalyze, IComCRMEvents::OnCRMAnalyze, OnCRMAnalyze, OnCRMAnalyze method [COM+], OnCRMAnalyze method [COM+],IComCRMEvents interface, _dtc_IComCRMEvents_OnCRMAnalyze, comsvcs/IComCRMEvents::OnCRMAnalyze, cos.icomcrmevents_oncrmanalyze
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
 - IComCRMEvents.OnCRMAnalyze
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IComCRMEvents::OnCRMAnalyze


## -description


Generated when a CRM clerk receives a record during the analysis phase of recovery.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/f4aa0892-4c93-42ea-adc6-1b304b917389">COMSVCSEVENTINFO</a> structure.


### -param guidClerkCLSID [in]

The identifier of the CRM clerk.


### -param dwCrmRecordType [in]

The CRM log record type (internal).


### -param dwRecordSize [in]

The log record size (approximate).


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/720beffb-8fb5-4c87-9bcf-6db214543b01">IComCRMEvents</a>
 

 

