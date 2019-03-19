---
UID: NN:workspaceruntime.IWorkspace3
title: IWorkspace3 (workspaceruntime.h)
author: windows-sdk-content
description: Exposes methods that provide information about a connection in RemoteApp and Desktop Connection, and adds the ability to retrieve or set a claims token.
old-location: termserv\iworkspace3.htm
tech.root: TermServ
ms.assetid: a63240fb-8724-4cd2-b845-f48075f4cb57
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWorkspace3, IWorkspace3 interface [Remote Desktop Services], IWorkspace3 interface [Remote Desktop Services],described, termserv.iworkspace3, workspaceruntime/IWorkspace3
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWorkspace3 interface


## -description


Exposes methods that provide information about a connection in RemoteApp and Desktop Connection, and adds 
   the ability to retrieve or set a claims token.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWorkspace3</b> interface inherits from <a href="https://msdn.microsoft.com/8155cd78-4c6b-47a9-a2c7-f9fffc95f700">IWorkspace2</a>. <b>IWorkspace3</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/d615b999-0713-4d16-a89b-b5b208a76124">GetClaimsToken2</a>
</td>
<td align="left" width="63%">
Sets the claims token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/221b0e8f-b43a-4942-9e70-152daf5b1ef0">SetClaimsToken</a>
</td>
<td align="left" width="63%">
Retrieves the claims token.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/8155cd78-4c6b-47a9-a2c7-f9fffc95f700">IWorkspace2</a>



<a href="https://msdn.microsoft.com/4580df05-5e44-40d0-8765-5d9b4e1d339e">RemoteApp and Desktop Connection Runtime interfaces</a>
 

 

