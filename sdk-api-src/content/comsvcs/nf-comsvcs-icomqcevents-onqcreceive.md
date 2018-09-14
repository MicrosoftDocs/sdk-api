---
UID: NF:comsvcs.IComQCEvents.OnQCReceive
title: IComQCEvents::OnQCReceive
author: windows-sdk-content
description: Generated when a message is successfully de-queued even though the queued components service might find something wrong with the contents.
old-location: cos\icomqcevents_onqcreceive.htm
tech.root: cossdk
ms.assetid: d4404fad-c656-4cbf-90d1-a09a7162a38f
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: IComQCEvents interface [COM+],OnQCReceive method, IComQCEvents.OnQCReceive, IComQCEvents::OnQCReceive, OnQCReceive, OnQCReceive method [COM+], OnQCReceive method [COM+],IComQCEvents interface, _dtc_IComQCEvents_OnQCReceive, comsvcs/IComQCEvents::OnQCReceive, cos.icomqcevents_onqcreceive
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
 - IComQCEvents.OnQCReceive
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IComQCEvents::OnQCReceive


## -description


Generated when a message is successfully de-queued even though the queued components service might find something wrong with the contents.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/f4aa0892-4c93-42ea-adc6-1b304b917389">COMSVCSEVENTINFO</a> structure.


### -param QueueID [in]

The unique identifier for the queue.


### -param guidMsgId [in]

The unique identifier for the queued message.


### -param guidWorkFlowId [in]

This parameter is reserved.


### -param hr [in]

The status from Queued Components processing of the received message.



## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/d7c8220d-a302-4f95-b0b6-8d47f9f27da7">IComQCEvents</a>
 

 

