---
UID: NF:comsvcs.IComCRMEvents.OnCRMCheckpoint
title: IComCRMEvents::OnCRMCheckpoint (comsvcs.h)
author: windows-sdk-content
description: Generated when a CRM checkpoint occurs.
old-location: cos\icomcrmevents_oncrmcheckpoint.htm
tech.root: cossdk
ms.assetid: f1a91d24-0a78-4d4f-a686-817d0609e2b1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IComCRMEvents interface [COM+],OnCRMCheckpoint method, IComCRMEvents.OnCRMCheckpoint, IComCRMEvents::OnCRMCheckpoint, OnCRMCheckpoint, OnCRMCheckpoint method [COM+], OnCRMCheckpoint method [COM+],IComCRMEvents interface, _dtc_IComCRMEvents_OnCRMCheckpoint, comsvcs/IComCRMEvents::OnCRMCheckpoint, cos.icomcrmevents_oncrmcheckpoint
ms.topic: method
f1_keywords: ["comsvcs/IComCRMEvents.OnCRMCheckpoint"]
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
 - IComCRMEvents.OnCRMCheckpoint
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IComCRMEvents::OnCRMCheckpoint


## -description


Generated when a CRM checkpoint occurs.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/ns-comsvcs-__midl___midl_itf_autosvcs_0000_0013_0001">COMSVCSEVENTINFO</a> structure.


### -param guidApp [in]

The globally unique identifier (GUID) of the application.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-icomcrmevents">IComCRMEvents</a>
 

 

