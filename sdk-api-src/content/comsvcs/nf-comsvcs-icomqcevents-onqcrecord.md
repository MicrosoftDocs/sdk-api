---
UID: NF:comsvcs.IComQCEvents.OnQCRecord
title: IComQCEvents::OnQCRecord
author: windows-sdk-content
description: Generated when the queued components recorder creates the queued message.
old-location: cos\icomqcevents_onqcrecord.htm
tech.root: cossdk
ms.assetid: 6a7ff5ac-df0f-4aea-b6f1-813c7e22e6c2
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IComQCEvents interface [COM+],OnQCRecord method, IComQCEvents.OnQCRecord, IComQCEvents::OnQCRecord, OnQCRecord, OnQCRecord method [COM+], OnQCRecord method [COM+],IComQCEvents interface, _dtc_IComQCEvents_OnQCRecord, comsvcs/IComQCEvents::OnQCRecord, cos.icomqcevents_onqcrecord
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
 - IComQCEvents.OnQCRecord
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IComQCEvents::OnQCRecord


## -description


Generated when the queued components recorder creates the queued message.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/f4aa0892-4c93-42ea-adc6-1b304b917389">COMSVCSEVENTINFO</a> structure.


### -param objid [in]

The just-in-time activated object.


### -param szQueue [in]

The name of the queue.


### -param guidMsgId [in]

The unique identifier for the queued message.


### -param guidWorkFlowId [in]

This parameter is reserved.


### -param msmqhr [in]

The Message Queuing return status for the queued message.



## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/d7c8220d-a302-4f95-b0b6-8d47f9f27da7">IComQCEvents</a>
 

 

