---
UID: NF:comsvcs.IComCRMEvents.OnCRMRelease
title: IComCRMEvents::OnCRMRelease (comsvcs.h)
author: windows-sdk-content
description: Generated when the CRM clerk is finished and releases its resource locks.
old-location: cos\icomcrmevents_oncrmrelease.htm
tech.root: cossdk
ms.assetid: e97b6cbf-1e78-475b-9dc7-baa4c05f1a6b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IComCRMEvents interface [COM+],OnCRMRelease method, IComCRMEvents.OnCRMRelease, IComCRMEvents::OnCRMRelease, OnCRMRelease, OnCRMRelease method [COM+], OnCRMRelease method [COM+],IComCRMEvents interface, _dtc_IComCRMEvents_OnCRMRelease, comsvcs/IComCRMEvents::OnCRMRelease, cos.icomcrmevents_oncrmrelease
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
 - IComCRMEvents.OnCRMRelease
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IComCRMEvents::OnCRMRelease


## -description


Generated when the CRM clerk is finished and releases its resource locks.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms688276(v=VS.85).aspx">COMSVCSEVENTINFO</a> structure.


### -param guidClerkCLSID [in]

The identifier of the CRM clerk.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/720beffb-8fb5-4c87-9bcf-6db214543b01">IComCRMEvents</a>
 

 

