---
UID: NF:comsvcs.IComQCEvents.OnQCReceiveFail
title: IComQCEvents::OnQCReceiveFail (comsvcs.h)
author: windows-sdk-content
description: Generated when the receive message fails.
old-location: cos\icomqcevents_onqcreceivefail.htm
tech.root: cossdk
ms.assetid: 21d685ce-b65f-4d13-b653-e6c6d1afa704
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IComQCEvents interface [COM+],OnQCReceiveFail method, IComQCEvents.OnQCReceiveFail, IComQCEvents::OnQCReceiveFail, OnQCReceiveFail, OnQCReceiveFail method [COM+], OnQCReceiveFail method [COM+],IComQCEvents interface, _dtc_IComQCEvents_OnQCReceiveFail, comsvcs/IComQCEvents::OnQCReceiveFail, cos.icomqcevents_onqcreceivefail
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
 - IComQCEvents.OnQCReceiveFail
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IComQCEvents::OnQCReceiveFail


## -description


Generated when the receive message fails.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/ns-comsvcs-__midl___midl_itf_autosvcs_0000_0013_0001">COMSVCSEVENTINFO</a> structure.


### -param QueueID [in]

The unique identifier for the queue.


### -param msmqhr [in]

The status from Queued Components processing of the received message.



## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-icomqcevents">IComQCEvents</a>
 

 

