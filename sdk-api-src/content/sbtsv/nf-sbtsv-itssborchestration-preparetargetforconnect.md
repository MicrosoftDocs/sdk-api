---
UID: NF:sbtsv.ITsSbOrchestration.PrepareTargetForConnect
title: ITsSbOrchestration::PrepareTargetForConnect (sbtsv.h)
description: Prepares the target for a client connection.helpviewer_keywords: ["ITsSbOrchestration interface [Remote Desktop Services]","PrepareTargetForConnect method","ITsSbOrchestration.PrepareTargetForConnect","ITsSbOrchestration::PrepareTargetForConnect","PrepareTargetForConnect","PrepareTargetForConnect method [Remote Desktop Services]","PrepareTargetForConnect method [Remote Desktop Services]","ITsSbOrchestration interface","sbtsv/ITsSbOrchestration::PrepareTargetForConnect","termserv.itssborchestration_preparetargetforconnect"]
old-location: termserv\itssborchestration_preparetargetforconnect.htm
tech.root: TermServ
ms.assetid: 46ffad8a-bafc-426f-9963-9a6f6f60329b
ms.date: 12/05/2018
ms.keywords: ITsSbOrchestration interface [Remote Desktop Services],PrepareTargetForConnect method, ITsSbOrchestration.PrepareTargetForConnect, ITsSbOrchestration::PrepareTargetForConnect, PrepareTargetForConnect, PrepareTargetForConnect method [Remote Desktop Services], PrepareTargetForConnect method [Remote Desktop Services],ITsSbOrchestration interface, sbtsv/ITsSbOrchestration::PrepareTargetForConnect, termserv.itssborchestration_preparetargetforconnect
f1_keywords:
- sbtsv/ITsSbOrchestration.PrepareTargetForConnect
dev_langs:
- c++
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
- ITsSbOrchestration.PrepareTargetForConnect
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITsSbOrchestration::PrepareTargetForConnect


## -description


Prepares the target for a client connection.


## -parameters




### -param pConnection [in]

 A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection">ITsSbClientConnection</a> client connection object.


### -param pOrchestrationNotifySink [in]

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssborchestrationnotifysink">ITsSbOrchestrationNotifySink</a> orchestration notify sink object.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is particularly useful for plug-ins that redirect users to virtual desktops. Remote Desktop Connection Broker (RD Connection Broker) 
calls this method after placement has successfully completed. Orchestration can 
include waking a virtual machine and determining its IP address. Your implementation of this method should ensure that the target is ready to accept a client connection.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection">ITsSbClientConnection</a>



<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssborchestration">ITsSbOrchestration</a>



<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssborchestrationnotifysink">ITsSbOrchestrationNotifySink</a>
 

 

