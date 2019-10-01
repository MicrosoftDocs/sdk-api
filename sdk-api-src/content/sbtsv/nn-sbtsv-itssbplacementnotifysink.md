---
UID: NN:sbtsv.ITsSbPlacementNotifySink
title: ITsSbPlacementNotifySink (sbtsv.h)
author: windows-sdk-content
description: Exposes methods that return information about environments to Remote Desktop Connection Broker (RD Connection Broker).
old-location: termserv\itssbplacementnotifysink.htm
tech.root: TermServ
ms.assetid: 7abc5454-141a-47bc-b9cd-341b41a093d2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITsSbPlacementNotifySink, ITsSbPlacementNotifySink interface [Remote Desktop Services], ITsSbPlacementNotifySink interface [Remote Desktop Services],described, sbtsv/ITsSbPlacementNotifySink, termserv.itssbplacementnotifysink
ms.topic: interface
f1_keywords: 
 - "sbtsv/ITsSbPlacementNotifySink"
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
 - ITsSbPlacementNotifySink
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITsSbPlacementNotifySink interface


## -description


Exposes methods that return information about environments to 
   Remote Desktop Connection Broker (RD Connection Broker).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITsSbPlacementNotifySink</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbbasenotifysink">ITsSbBaseNotifySink</a>. <b>ITsSbPlacementNotifySink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITsSbPlacementNotifySink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nf-sbtsv-itssbplacementnotifysink-onqueryenvironmentcompleted">OnQueryEnvironmentCompleted</a>
</td>
<td align="left" width="63%">
Notifies RD Connection Broker that the environment specified by the 
       <a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection">ITsSbClientConnection</a> object is already 
       hosting the correct target.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbbasenotifysink">ITsSbBaseNotifySink</a>



<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection">ITsSbClientConnection</a>



<a href="https://docs.microsoft.com/windows/desktop/TermServ/remote-desktop-virtualization-interfaces">Remote Desktop Virtualization Interfaces</a>
 

 

