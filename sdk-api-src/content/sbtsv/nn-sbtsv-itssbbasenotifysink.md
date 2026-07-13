---
UID: NN:sbtsv.ITsSbBaseNotifySink
title: ITsSbBaseNotifySink (sbtsv.h)
description: Exposes methods that report status and error messages to Remote Desktop Connection Broker (RD Connection Broker).
helpviewer_keywords: ["ITsSbBaseNotifySink","ITsSbBaseNotifySink interface [Remote Desktop Services]","ITsSbBaseNotifySink interface [Remote Desktop Services]","described","sbtsv/ITsSbBaseNotifySink","termserv.itssbbasenotifysink"]
old-location: termserv\itssbbasenotifysink.htm
tech.root: TermServ
ms.assetid: 11ef1bd4-301f-456b-a68b-2f32b75ac5ae
ms.date: 12/05/2018
ms.keywords: ITsSbBaseNotifySink, ITsSbBaseNotifySink interface [Remote Desktop Services], ITsSbBaseNotifySink interface [Remote Desktop Services],described, sbtsv/ITsSbBaseNotifySink, termserv.itssbbasenotifysink
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
 - ITsSbBaseNotifySink
 - sbtsv/ITsSbBaseNotifySink
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
 - ITsSbBaseNotifySink
---

# ITsSbBaseNotifySink interface


## -description

Exposes methods that report status and error messages to Remote Desktop Connection Broker (RD Connection Broker).

## -inheritance

The <b>ITsSbBaseNotifySink</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITsSbBaseNotifySink</b> also has these types of members:

## -remarks

Plug-ins can use this interface to report status and error messages to RD Connection Broker.

The RD Connection Broker server and the Remote Desktop Session Host (RD Session Host) server (the redirector) must 
    be running Windows Server 2008 R2, and clients must use RDC 7.0.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbbasenotifysink">ITsSbBaseNotifySink</a>



<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalancingnotifysink">ITsSbLoadBalancingNotifySink</a>



<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssborchestrationnotifysink">ITsSbOrchestrationNotifySink</a>



<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbplacementnotifysink">ITsSbPlacementNotifySink</a>



<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbpluginnotifysink">ITsSbPluginNotifySink</a>



<a href="/windows/desktop/TermServ/remote-desktop-virtualization-interfaces">Remote Desktop Virtualization Interfaces</a>
