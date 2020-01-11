---
UID: NN:sbtsv.ITsSbProvisioning
title: ITsSbProvisioning (sbtsv.h)
description: Exposes methods that create and maintain virtual machines.
old-location: termserv\itssbprovisioning.htm
tech.root: TermServ
ms.assetid: 136c1538-be4f-4b1c-b74f-8914a51f774a
ms.date: 12/05/2018
ms.keywords: ITsSbProvisioning, ITsSbProvisioning interface [Remote Desktop Services], ITsSbProvisioning interface [Remote Desktop Services],described, sbtsv/ITsSbProvisioning, termserv.itssbprovisioning
f1_keywords:
- sbtsv/ITsSbProvisioning
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
- ITsSbProvisioning
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITsSbProvisioning interface


## -description


Exposes methods that create and maintain virtual machines.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITsSbProvisioning</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbplugin">ITsSbPlugin</a>. <b>ITsSbProvisioning</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nf-sbtsv-itssbprovisioning-canceljob">CancelJob</a>
</td>
<td align="left" width="63%">
Cancels a provisioning job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nf-sbtsv-itssbprovisioning-createvirtualmachines">CreateVirtualMachines</a>
</td>
<td align="left" width="63%">
Creates a virtual machine asynchronously.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nf-sbtsv-itssbprovisioning-deletevirtualmachines">DeleteVirtualMachines</a>
</td>
<td align="left" width="63%">
Deletes a virtual machine asynchronously.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nf-sbtsv-itssbprovisioning-patchvirtualmachines">PatchVirtualMachines</a>
</td>
<td align="left" width="63%">
Patches a virtual machine asynchronously.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbplugin">ITsSbPlugin</a>



<a href="https://docs.microsoft.com/windows/desktop/TermServ/remote-desktop-virtualization-interfaces">Remote Desktop Virtualization Interfaces</a>
 

 

