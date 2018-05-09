---
UID: NF:comsvcs.IComQCEvents.OnQCReceiveFail
title: IComQCEvents::OnQCReceiveFail
author: windows-driver-content
description: Generated when the receive message fails.
old-location: cos\icomqcevents_onqcreceivefail.htm
old-project: cossdk
ms.assetid: 21d685ce-b65f-4d13-b653-e6c6d1afa704
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: IComQCEvents interface [COM+],OnQCReceiveFail method, IComQCEvents.OnQCReceiveFail, IComQCEvents::OnQCReceiveFail, OnQCReceiveFail, OnQCReceiveFail method [COM+], OnQCReceiveFail method [COM+],IComQCEvents interface, _dtc_IComQCEvents_OnQCReceiveFail, comsvcs/IComQCEvents::OnQCReceiveFail, cos.icomqcevents_onqcreceivefail
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	IComQCEvents.OnQCReceiveFail
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IComQCEvents::OnQCReceiveFail


## -description


Generated when the receive message fails.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/f4aa0892-4c93-42ea-adc6-1b304b917389">COMSVCSEVENTINFO</a> structure.


### -param QueueID [in]

The unique identifier for the queue.


### -param msmqhr [in]

The status from Queued Components processing of the received message.



## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/d7c8220d-a302-4f95-b0b6-8d47f9f27da7">IComQCEvents</a>
 

 

