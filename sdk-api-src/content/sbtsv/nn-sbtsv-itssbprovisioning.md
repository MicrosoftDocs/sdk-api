---
UID: NN:sbtsv.ITsSbProvisioning
title: ITsSbProvisioning
author: windows-sdk-content
description: Exposes methods that create and maintain virtual machines.
old-location: termserv\itssbprovisioning.htm
old-project: TermServ
ms.assetid: 136c1538-be4f-4b1c-b74f-8914a51f774a
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: ITsSbProvisioning, ITsSbProvisioning interface [Remote Desktop Services], ITsSbProvisioning interface [Remote Desktop Services],described, sbtsv/ITsSbProvisioning, termserv.itssbprovisioning
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
tech.root: 
req.typenames: TS_SB_SORT_BY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbtsv.h
api_name:
 - ITsSbProvisioning
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# ITsSbProvisioning interface


## -description


Exposes methods that create and maintain virtual machines.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITsSbProvisioning</b> interface inherits from <a href="https://msdn.microsoft.com/db3d3ee7-9e53-4bac-9711-4e85f1016db9">ITsSbPlugin</a>. <b>ITsSbProvisioning</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITsSbProvisioning</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c0496a8c-00ec-43a4-a7c2-071acb6b068a">CancelJob</a>
</td>
<td align="left" width="63%">
Cancels a provisioning job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/752da6d8-d036-4a39-aed5-c1fd7a11474e">CreateVirtualMachines</a>
</td>
<td align="left" width="63%">
Creates a virtual machine asynchronously.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/45f5398d-2d27-4f6b-9020-bcbb44edc89a">DeleteVirtualMachines</a>
</td>
<td align="left" width="63%">
Deletes a virtual machine asynchronously.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/99afcba2-5567-47fa-9752-80394f145176">PatchVirtualMachines</a>
</td>
<td align="left" width="63%">
Patches a virtual machine asynchronously.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/db3d3ee7-9e53-4bac-9711-4e85f1016db9">ITsSbPlugin</a>



<a href="https://msdn.microsoft.com/150a3c9a-d504-4854-adaa-92e3a7e8ea70">Remote Desktop Virtualization Interfaces</a>
 

 

