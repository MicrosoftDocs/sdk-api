---
UID: NN:workspaceruntime.IWorkspace2
title: IWorkspace2
author: windows-sdk-content
description: Exposes additional methods that provide information about a connection in RemoteApp and Desktop Connection.
old-location: termserv\iworkspace2.htm
tech.root: termserv
ms.assetid: 8155cd78-4c6b-47a9-a2c7-f9fffc95f700
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IWorkspace2, IWorkspace2 interface [Remote Desktop Services], IWorkspace2 interface [Remote Desktop Services],described, termserv.iworkspace2, workspaceruntime/IWorkspace2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: workspaceruntime.h
req.include-header: Workspaceruntime.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WorkspaceRuntime.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: WkspRt.exe
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WkspRt.exe
api_name:
 - IWorkspace2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWorkspace2 interface


## -description


Not supported.

Exposes additional methods that provide information about a connection in RemoteApp and Desktop Connection. This interface is implemented by the Remote Desktop Services workspace runtime. These methods are called by custom clients that implement the <a href="https://msdn.microsoft.com/f72b0709-1a55-49c9-ab5d-22f9259c41f0">IWorkspaceClientExt</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWorkspace2</b> interface inherits from <a href="https://msdn.microsoft.com/7a94ef42-8a63-4709-816d-1f51a948d486">IWorkspace</a>. <b>IWorkspace2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWorkspace2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/df901da6-6464-4ed3-abbb-16756f90ccf1">StartRemoteApplicationEx</a>
</td>
<td align="left" width="63%">
Starts a RemoteApp program with additional options and features.

</td>
</tr>
</table> 

