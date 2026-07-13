---
UID: NF:sbtsv.ITsSbOrchestrationNotifySink.OnReadyToConnect
title: ITsSbOrchestrationNotifySink::OnReadyToConnect (sbtsv.h)
description: Returns an ITsSbTarget object to Remote Desktop Connection Broker (RD Connection Broker) after the target is successfully prepared for a connection.
helpviewer_keywords: ["ITsSbOrchestrationNotifySink interface [Remote Desktop Services]","OnReadyToConnect method","ITsSbOrchestrationNotifySink.OnReadyToConnect","ITsSbOrchestrationNotifySink::OnReadyToConnect","OnReadyToConnect","OnReadyToConnect method [Remote Desktop Services]","OnReadyToConnect method [Remote Desktop Services]","ITsSbOrchestrationNotifySink interface","sbtsv/ITsSbOrchestrationNotifySink::OnReadyToConnect","termserv.itssborchestrationnotifysink_onreadytoconnect"]
old-location: termserv\itssborchestrationnotifysink_onreadytoconnect.htm
tech.root: TermServ
ms.assetid: 781cb67c-75bb-4d3c-8b86-fddbe9511255
ms.date: 12/05/2018
ms.keywords: ITsSbOrchestrationNotifySink interface [Remote Desktop Services],OnReadyToConnect method, ITsSbOrchestrationNotifySink.OnReadyToConnect, ITsSbOrchestrationNotifySink::OnReadyToConnect, OnReadyToConnect, OnReadyToConnect method [Remote Desktop Services], OnReadyToConnect method [Remote Desktop Services],ITsSbOrchestrationNotifySink interface, sbtsv/ITsSbOrchestrationNotifySink::OnReadyToConnect, termserv.itssborchestrationnotifysink_onreadytoconnect
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITsSbOrchestrationNotifySink::OnReadyToConnect
 - sbtsv/ITsSbOrchestrationNotifySink::OnReadyToConnect
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbtsv.h
api_name:
 - ITsSbOrchestrationNotifySink.OnReadyToConnect
---

# ITsSbOrchestrationNotifySink::OnReadyToConnect


## -description

Returns an <a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget">ITsSbTarget</a> object to Remote Desktop Connection Broker (RD Connection Broker) after the target is successfully prepared for a connection.

## -parameters

### -param pTarget [in]

A pointer to an <a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget">ITsSbTarget</a> target object.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The target object referenced by the <i>pTarget</i> parameter should contain the external IP address of the target object. Without this information, the request will fail.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssborchestrationnotifysink">ITsSbOrchestrationNotifySink</a>



<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget">ITsSbTarget</a>