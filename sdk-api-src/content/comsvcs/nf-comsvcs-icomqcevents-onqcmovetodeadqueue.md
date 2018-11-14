---
UID: NF:comsvcs.IComQCEvents.OnQCMoveToDeadQueue
title: IComQCEvents::OnQCMoveToDeadQueue
author: windows-sdk-content
description: Generated when a message is moved to the dead letter queue and cannot be delivered.
old-location: cos\icomqcevents_onqcmovetodeadqueue.htm
tech.root: cossdk
ms.assetid: 54117583-4e8d-4ae9-8262-781f5f81636d
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IComQCEvents interface [COM+],OnQCMoveToDeadQueue method, IComQCEvents.OnQCMoveToDeadQueue, IComQCEvents::OnQCMoveToDeadQueue, OnQCMoveToDeadQueue, OnQCMoveToDeadQueue method [COM+], OnQCMoveToDeadQueue method [COM+],IComQCEvents interface, _dtc_IComQCEvents_OnQCMoveToDeadQueue, comsvcs/IComQCEvents::OnQCMoveToDeadQueue, cos.icomqcevents_onqcmovetodeadqueue
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
 - IComQCEvents.OnQCMoveToDeadQueue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- comsvcs.h
: 
- IComQCEvents.OnQCMoveToDeadQueue
: 
---

# IComQCEvents::OnQCMoveToDeadQueue


## -description


Generated when a message is moved to the dead letter queue and cannot be delivered.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/f4aa0892-4c93-42ea-adc6-1b304b917389">COMSVCSEVENTINFO</a> structure.


### -param guidMsgId [in]

The unique identifier for the message.


### -param guidWorkFlowId [in]

This parameter is reserved.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/d7c8220d-a302-4f95-b0b6-8d47f9f27da7">IComQCEvents</a>
 

 

