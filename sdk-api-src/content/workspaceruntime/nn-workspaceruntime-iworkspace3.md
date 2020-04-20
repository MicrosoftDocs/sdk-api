---
UID: NN:workspaceruntime.IWorkspace3
title: IWorkspace3 (workspaceruntime.h)
description: Exposes methods that provide information about a connection in RemoteApp and Desktop Connection, and adds the ability to retrieve or set a claims token.helpviewer_keywords: ["IWorkspace3","IWorkspace3 interface [Remote Desktop Services]","IWorkspace3 interface [Remote Desktop Services]","described","termserv.iworkspace3","workspaceruntime/IWorkspace3"]
old-location: termserv\iworkspace3.htm
tech.root: TermServ
ms.assetid: a63240fb-8724-4cd2-b845-f48075f4cb57
ms.date: 12/05/2018
ms.keywords: IWorkspace3, IWorkspace3 interface [Remote Desktop Services], IWorkspace3 interface [Remote Desktop Services],described, termserv.iworkspace3, workspaceruntime/IWorkspace3
f1_keywords:
- workspaceruntime/IWorkspace3
dev_langs:
- c++
req.header: workspaceruntime.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WorkspaceRuntime.idl
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
- workspaceruntime.h
api_name:
- IWorkspace3
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWorkspace3 interface


## -description


Exposes methods that provide information about a connection in RemoteApp and Desktop Connection, and adds 
   the ability to retrieve or set a claims token.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWorkspace3</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspace2">IWorkspace2</a>. <b>IWorkspace3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWorkspace3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/workspaceruntime/nf-workspaceruntime-iworkspace3-getclaimstoken2">GetClaimsToken2</a>
</td>
<td align="left" width="63%">
Sets the claims token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/workspaceruntime/nf-workspaceruntime-iworkspace3-setclaimstoken">SetClaimsToken</a>
</td>
<td align="left" width="63%">
Retrieves the claims token.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspace2">IWorkspace2</a>



<a href="https://docs.microsoft.com/windows/desktop/TermServ/remoteapp-and-desktop-connection-runtime-interfaces">RemoteApp and Desktop Connection Runtime interfaces</a>
 

 

