---
UID: NN:sbtsv.ITsSbTaskPlugin
title: ITsSbTaskPlugin (sbtsv.h)
description: Exposes methods that update the queue of tasks for Remote Desktop Connection Broker plugins.
old-location: termserv\itssbtaskplugin.htm
tech.root: TermServ
ms.assetid: 56463b47-c2f2-43b7-884f-d6fab9bebbf0
ms.date: 12/05/2018
ms.keywords: ITsSbTaskPlugin, ITsSbTaskPlugin interface [Remote Desktop Services], ITsSbTaskPlugin interface [Remote Desktop Services],described, sbtsv/ITsSbTaskPlugin, termserv.itssbtaskplugin
f1_keywords:
- sbtsv/ITsSbTaskPlugin
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
- ITsSbTaskPlugin
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITsSbTaskPlugin interface


## -description


Exposes methods that update the queue of tasks for Remote Desktop Connection Broker plugins.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITsSbTaskPlugin</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbplugin">ITsSbPlugin</a>. <b>ITsSbTaskPlugin</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITsSbTaskPlugin</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskplugin-initializetaskplugin">InitializeTaskPlugin</a>
</td>
<td align="left" width="63%">
Initializes a task that is in the queue of a Remote Desktop Connection Broker plugin.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskplugin-settaskqueue">SetTaskQueue</a>
</td>
<td align="left" width="63%">
Updates a task in the queue of  a Remote Desktop Connection Broker plugin.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbplugin">ITsSbPlugin</a>



<a href="https://docs.microsoft.com/windows/desktop/TermServ/remote-desktop-virtualization-interfaces">Remote Desktop Virtualization Interfaces</a>
 

 

