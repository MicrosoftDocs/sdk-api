---
UID: NN:workspaceax.IWorkspaceResTypeRegistry
title: IWorkspaceResTypeRegistry (workspaceax.h)
author: windows-sdk-content
description: Exposes methods that allow a plug-in to manage third-party file name extensions in RemoteApp and Desktop Connection runtime.
old-location: termserv\iworkspacerestyperegistry.htm
tech.root: TermServ
ms.assetid: bea617a0-cd64-4c77-af27-b418178e3dad
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWorkspaceResTypeRegistry, IWorkspaceResTypeRegistry interface [Remote Desktop Services], IWorkspaceResTypeRegistry interface [Remote Desktop Services],described, termserv.iworkspacerestyperegistry, workspaceax/IWorkspaceResTypeRegistry
ms.topic: interface
f1_keywords: 
 - "workspaceax/IWorkspaceResTypeRegistry"
dev_langs:
 - c++
req.header: workspaceax.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Tsworkspace.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tsworkspace.dll
api_name:
 - IWorkspaceResTypeRegistry
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWorkspaceResTypeRegistry interface


## -description


Exposes methods that allow a plug-in to manage third-party file name extensions in RemoteApp and Desktop Connection runtime. This interface is implemented by the Remote Desktop Services workspace runtime. These methods are called by custom clients.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWorkspaceResTypeRegistry</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IWorkspaceResTypeRegistry</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWorkspaceResTypeRegistry</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/workspaceax/nf-workspaceax-iworkspacerestyperegistry-addresourcetype">AddResourceType</a>
</td>
<td align="left" width="63%">
Registers a third-party file name extension with the RemoteApp and Desktop Connections runtime.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/workspaceax/nf-workspaceax-iworkspacerestyperegistry-deleteresourcetype">DeleteResourceType</a>
</td>
<td align="left" width="63%">
Unregisters a third-party file name extension with the RemoteApp and Desktop Connections runtime.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/workspaceax/nf-workspaceax-iworkspacerestyperegistry-getregisteredfileextensions">GetRegisteredFileExtensions</a>
</td>
<td align="left" width="63%">
Retrieves the third-party file name extensions that are registered with the RemoteApp and Desktop Connections runtime.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/workspaceax/nf-workspaceax-iworkspacerestyperegistry-getresourcetypeinfo">GetResourceTypeInfo</a>
</td>
<td align="left" width="63%">
Retrieves information about a third-party file name extension that is registered with the RemoteApp and Desktop Connections runtime.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/workspaceax/nf-workspaceax-iworkspacerestyperegistry-modifyresourcetype">ModifyResourceType</a>
</td>
<td align="left" width="63%">
Modifies a third-party file name extension that is registered with the RemoteApp and Desktop Connections runtime.

</td>
</tr>
</table> 

