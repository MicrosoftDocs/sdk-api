---
UID: NN:sbtsv.ITsSbProvisioningPluginNotifySink
title: ITsSbProvisioningPluginNotifySink
author: windows-sdk-content
description: Exposes methods that notify Remote Desktop Connection Broker (RD Connection Broker) about the provisioning of virtual machines.
old-location: termserv\itssbprovisioningpluginnotifysink.htm
tech.root: termserv
ms.assetid: 6f91021c-d7a5-4131-bef7-b4f5f37f9f8b
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: ITsSbProvisioningPluginNotifySink, ITsSbProvisioningPluginNotifySink interface [Remote Desktop Services], ITsSbProvisioningPluginNotifySink interface [Remote Desktop Services],described, sbtsv/ITsSbProvisioningPluginNotifySink, termserv.itssbprovisioningpluginnotifysink
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITsSbProvisioningPluginNotifySink interface


## -description


Exposes methods that notify Remote Desktop Connection Broker (RD Connection Broker) about the provisioning of virtual machines.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITsSbProvisioningPluginNotifySink</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITsSbProvisioningPluginNotifySink</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/48eeaf06-3c6e-4c45-b5cd-9301dce7caee">LockVirtualMachine</a>
</td>
<td align="left" width="63%">
Lock VM

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c4e65194-47c1-43d9-93b3-fbbb57d7f34a">OnJobCancelled</a>
</td>
<td align="left" width="63%">
Job canceled notification

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7d0399c8-2161-4d6e-8c14-7fd5bc2757b8">OnJobCompleted</a>
</td>
<td align="left" width="63%">
Job complete notification

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/daab9172-d984-4b47-9f64-59216513aff7">OnJobCreated</a>
</td>
<td align="left" width="63%">
Job created notification

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d86e9092-42ca-4e62-8613-cdcf2f8b627d">OnVirtualMachineHostStatusChanged</a>
</td>
<td align="left" width="63%">
Virtual Machine Host status changed

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5a256dec-fa40-48c2-b7e3-e89ec9e75f0e">OnVirtualMachineStatusChanged</a>
</td>
<td align="left" width="63%">
Virtual Machine status changed notification

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>



<a href="https://msdn.microsoft.com/150a3c9a-d504-4854-adaa-92e3a7e8ea70">Remote Desktop Virtualization Interfaces</a>
 

 

