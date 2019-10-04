---
UID: NN:sbtsv.ITsSbProvisioningPluginNotifySink
title: ITsSbProvisioningPluginNotifySink (sbtsv.h)
author: windows-sdk-content
description: Exposes methods that notify Remote Desktop Connection Broker (RD Connection Broker) about the provisioning of virtual machines.
old-location: termserv\itssbprovisioningpluginnotifysink.htm
tech.root: TermServ
ms.assetid: 6f91021c-d7a5-4131-bef7-b4f5f37f9f8b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITsSbProvisioningPluginNotifySink, ITsSbProvisioningPluginNotifySink interface [Remote Desktop Services], ITsSbProvisioningPluginNotifySink interface [Remote Desktop Services],described, sbtsv/ITsSbProvisioningPluginNotifySink, termserv.itssbprovisioningpluginnotifysink
ms.topic: interface
f1_keywords: 
 - "sbtsv/ITsSbProvisioningPluginNotifySink"
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
 - ITsSbProvisioningPluginNotifySink
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITsSbProvisioningPluginNotifySink interface


## -description


Exposes methods that notify Remote Desktop Connection Broker (RD Connection Broker) about the provisioning of virtual machines.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITsSbProvisioningPluginNotifySink</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITsSbProvisioningPluginNotifySink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITsSbProvisioningPluginNotifySink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nf-sbtsv-itssbprovisioningpluginnotifysink-lockvirtualmachine">LockVirtualMachine</a>
</td>
<td align="left" width="63%">
Lock VM

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nf-sbtsv-itssbprovisioningpluginnotifysink-onjobcancelled">OnJobCancelled</a>
</td>
<td align="left" width="63%">
Job canceled notification

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nf-sbtsv-itssbprovisioningpluginnotifysink-onjobcompleted">OnJobCompleted</a>
</td>
<td align="left" width="63%">
Job complete notification

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nf-sbtsv-itssbprovisioningpluginnotifysink-onjobcreated">OnJobCreated</a>
</td>
<td align="left" width="63%">
Job created notification

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nf-sbtsv-itssbprovisioningpluginnotifysink-onvirtualmachinehoststatuschanged">OnVirtualMachineHostStatusChanged</a>
</td>
<td align="left" width="63%">
Virtual Machine Host status changed

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nf-sbtsv-itssbprovisioningpluginnotifysink-onvirtualmachinestatuschanged">OnVirtualMachineStatusChanged</a>
</td>
<td align="left" width="63%">
Virtual Machine status changed notification

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="https://docs.microsoft.com/windows/desktop/TermServ/remote-desktop-virtualization-interfaces">Remote Desktop Virtualization Interfaces</a>
 

 

