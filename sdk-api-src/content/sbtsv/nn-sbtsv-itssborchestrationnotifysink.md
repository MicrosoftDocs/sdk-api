---
UID: NN:sbtsv.ITsSbOrchestrationNotifySink
title: ITsSbOrchestrationNotifySink (sbtsv.h)
description: Exposes methods that return an ITsSbTarget object to Remote Desktop Connection Broker (RD Connection Broker) after the target is successfully prepared for a connection.
helpviewer_keywords: ["ITsSbOrchestrationNotifySink","ITsSbOrchestrationNotifySink interface [Remote Desktop Services]","ITsSbOrchestrationNotifySink interface [Remote Desktop Services]","described","sbtsv/ITsSbOrchestrationNotifySink","termserv.itssborchestrationnotifysink"]
old-location: termserv\itssborchestrationnotifysink.htm
tech.root: TermServ
ms.assetid: 767b6e73-ee0d-4802-99ff-ac37880a0884
ms.date: 12/05/2018
ms.keywords: ITsSbOrchestrationNotifySink, ITsSbOrchestrationNotifySink interface [Remote Desktop Services], ITsSbOrchestrationNotifySink interface [Remote Desktop Services],described, sbtsv/ITsSbOrchestrationNotifySink, termserv.itssborchestrationnotifysink
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
 - ITsSbOrchestrationNotifySink
 - sbtsv/ITsSbOrchestrationNotifySink
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
 - ITsSbOrchestrationNotifySink
---

# ITsSbOrchestrationNotifySink interface


## -description

Exposes methods that return an <a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget">ITsSbTarget</a> object to Remote Desktop Connection Broker (RD Connection Broker) after the target is successfully prepared for a connection.

## -inheritance

The <b>ITsSbOrchestrationNotifySink</b> interface inherits from <a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbbasenotifysink">ITsSbBaseNotifySink</a>. <b>ITsSbOrchestrationNotifySink</b> also has these types of members:

## -remarks

Plug-ins should use this interface to return an <a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget">ITsSbTarget</a> object to RD Connection Broker after the plug-in has successfully prepared ("orchestrated") the target.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbbasenotifysink">ITsSbBaseNotifySink</a>



<a href="/windows/desktop/TermServ/remote-desktop-virtualization-interfaces">Remote Desktop Virtualization Interfaces</a>
