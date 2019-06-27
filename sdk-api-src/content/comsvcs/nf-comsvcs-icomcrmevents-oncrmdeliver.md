---
UID: NF:comsvcs.IComCRMEvents.OnCRMDeliver
title: IComCRMEvents::OnCRMDeliver (comsvcs.h)
author: windows-sdk-content
description: Generated when a CRM clerk delivers a record to a CRM compensator.
old-location: cos\icomcrmevents_oncrmdeliver.htm
tech.root: cossdk
ms.assetid: e93e5548-b833-43a9-a73e-1ccad9d252b6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IComCRMEvents interface [COM+],OnCRMDeliver method, IComCRMEvents.OnCRMDeliver, IComCRMEvents::OnCRMDeliver, OnCRMDeliver, OnCRMDeliver method [COM+], OnCRMDeliver method [COM+],IComCRMEvents interface, _dtc_IComCRMEvents_OnCRMDeliver, comsvcs/IComCRMEvents::OnCRMDeliver, cos.icomcrmevents_oncrmdeliver
ms.topic: method
f1_keywords: 
 - "comsvcs/IComCRMEvents.OnCRMDeliver"
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
 - IComCRMEvents.OnCRMDeliver
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IComCRMEvents::OnCRMDeliver


## -description


Generated when a CRM clerk delivers a record to a CRM compensator.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/ns-comsvcs-__midl___midl_itf_autosvcs_0000_0013_0001">COMSVCSEVENTINFO</a> structure.


### -param guidClerkCLSID [in]

The identifier of the CRM clerk.


### -param fVariants [in]

Indicates whether the log record is being written as a <b>Variant</b> array.


### -param dwRecordSize [in]

The log record size (approximate).


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-icomcrmevents">IComCRMEvents</a>
 

 

