---
UID: NN:sbtsv.ITsSbBaseNotifySink
title: ITsSbBaseNotifySink (sbtsv.h)
author: windows-sdk-content
description: Exposes methods that report status and error messages to Remote Desktop Connection Broker (RD Connection Broker).
old-location: termserv\itssbbasenotifysink.htm
tech.root: TermServ
ms.assetid: 11ef1bd4-301f-456b-a68b-2f32b75ac5ae
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITsSbBaseNotifySink, ITsSbBaseNotifySink interface [Remote Desktop Services], ITsSbBaseNotifySink interface [Remote Desktop Services],described, sbtsv/ITsSbBaseNotifySink, termserv.itssbbasenotifysink
ms.topic: interface
f1_keywords: ["sbtsv/ITsSbBaseNotifySink"]
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
 - ITsSbBaseNotifySink
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITsSbBaseNotifySink interface


## -description


Exposes methods that report status and error messages to Remote Desktop Connection Broker (RD Connection Broker).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITsSbBaseNotifySink</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITsSbBaseNotifySink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITsSbBaseNotifySink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nf-sbtsv-itssbbasenotifysink-onerror">OnError</a>
</td>
<td align="left" width="63%">
Reports an error condition to RD Connection Broker. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nf-sbtsv-itssbbasenotifysink-onreportstatus">OnReportStatus</a>
</td>
<td align="left" width="63%">
Sends status messages to the Remote Desktop Connection (RDC) client regarding the processing of a client 
       connection.

</td>
</tr>
</table> 


## -remarks



Plug-ins can use this interface to report status and error messages to RD Connection Broker.

The RD Connection Broker server and the Remote Desktop Session Host (RD Session Host) server (the redirector) must 
    be running Windows Server 2008 R2, and clients must use RDC 7.0.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbbasenotifysink">ITsSbBaseNotifySink</a>



<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalancingnotifysink">ITsSbLoadBalancingNotifySink</a>



<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssborchestrationnotifysink">ITsSbOrchestrationNotifySink</a>



<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbplacementnotifysink">ITsSbPlacementNotifySink</a>



<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbpluginnotifysink">ITsSbPluginNotifySink</a>



<a href="https://docs.microsoft.com/windows/desktop/TermServ/remote-desktop-virtualization-interfaces">Remote Desktop Virtualization Interfaces</a>
 

 

