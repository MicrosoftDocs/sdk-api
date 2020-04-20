---
UID: NN:sbtsv.ITsSbPlacement
title: ITsSbPlacement (sbtsv.h)
description: Exposes methods that prepare the environment (the computer that hosts the virtual machine).helpviewer_keywords: ["ITsSbPlacement","ITsSbPlacement interface [Remote Desktop Services]","ITsSbPlacement interface [Remote Desktop Services]","described","sbtsv/ITsSbPlacement","termserv.itssbplacement"]
old-location: termserv\itssbplacement.htm
tech.root: TermServ
ms.assetid: d90501dd-ca15-463c-b204-b1f56103ebe7
ms.date: 12/05/2018
ms.keywords: ITsSbPlacement, ITsSbPlacement interface [Remote Desktop Services], ITsSbPlacement interface [Remote Desktop Services],described, sbtsv/ITsSbPlacement, termserv.itssbplacement
f1_keywords:
- sbtsv/ITsSbPlacement
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
- ITsSbPlacement
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITsSbPlacement interface


## -description


Exposes methods that prepare the environment (the computer that hosts the virtual 
machine). After Remote Desktop Connection Broker (RD Connection Broker) receives a load-balancing result, it calls <a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nf-sbtsv-itssbplacement-queryenvironmentfortarget">QueryEnvironmentForTarget</a> 
to determine whether the environment is present and ready. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITsSbPlacement</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbplugin">ITsSbPlugin</a>. <b>ITsSbPlacement</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITsSbPlacement</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nf-sbtsv-itssbplacement-queryenvironmentfortarget">QueryEnvironmentForTarget</a>
</td>
<td align="left" width="63%">
 Determines whether the specified environment is ready to host 
the target that was returned by load balancing.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbplugin">ITsSbPlugin</a>



<a href="https://docs.microsoft.com/windows/desktop/TermServ/remote-desktop-virtualization-interfaces">Remote Desktop Virtualization Interfaces</a>
 

 

