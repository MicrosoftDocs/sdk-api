---
UID: NF:sbtsv.ITsSbOrchestrationNotifySink.OnReadyToConnect
title: ITsSbOrchestrationNotifySink::OnReadyToConnect
author: windows-sdk-content
description: Returns an ITsSbTarget object to Remote Desktop Connection Broker (RD Connection Broker) after the target is successfully prepared for a connection.
old-location: termserv\itssborchestrationnotifysink_onreadytoconnect.htm
tech.root: termserv
ms.assetid: 781cb67c-75bb-4d3c-8b86-fddbe9511255
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: ITsSbOrchestrationNotifySink interface [Remote Desktop Services],OnReadyToConnect method, ITsSbOrchestrationNotifySink.OnReadyToConnect, ITsSbOrchestrationNotifySink::OnReadyToConnect, OnReadyToConnect, OnReadyToConnect method [Remote Desktop Services], OnReadyToConnect method [Remote Desktop Services],ITsSbOrchestrationNotifySink interface, sbtsv/ITsSbOrchestrationNotifySink::OnReadyToConnect, termserv.itssborchestrationnotifysink_onreadytoconnect
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: sbtsv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sbtsv.idl
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
 - sbtsv.h
api_name:
 - ITsSbOrchestrationNotifySink.OnReadyToConnect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITsSbOrchestrationNotifySink::OnReadyToConnect


## -description


Returns an <a href="https://msdn.microsoft.com/bcb26b43-ec6e-4cc8-9d40-15a7a3a62582">ITsSbTarget</a> object to Remote Desktop Connection Broker (RD Connection Broker) after the target is successfully prepared for a connection.


## -parameters




### -param pTarget [in]

A pointer to an <a href="https://msdn.microsoft.com/bcb26b43-ec6e-4cc8-9d40-15a7a3a62582">ITsSbTarget</a> target object.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The target object referenced by the <i>pTarget</i> parameter should contain the external IP address of the target object. Without this information, the request will fail.




## -see-also




<a href="https://msdn.microsoft.com/767b6e73-ee0d-4802-99ff-ac37880a0884">ITsSbOrchestrationNotifySink</a>



<a href="https://msdn.microsoft.com/bcb26b43-ec6e-4cc8-9d40-15a7a3a62582">ITsSbTarget</a>
 

 

