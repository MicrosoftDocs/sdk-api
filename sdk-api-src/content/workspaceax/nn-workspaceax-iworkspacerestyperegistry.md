---
UID: NN:workspaceax.IWorkspaceResTypeRegistry
title: IWorkspaceResTypeRegistry
author: windows-sdk-content
description: Exposes methods that allow a plug-in to manage third-party file name extensions in RemoteApp and Desktop Connection runtime.
old-location: termserv\iworkspacerestyperegistry.htm
old-project: termserv
ms.assetid: bea617a0-cd64-4c77-af27-b418178e3dad
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IWorkspaceResTypeRegistry, IWorkspaceResTypeRegistry interface [Remote Desktop Services], IWorkspaceResTypeRegistry interface [Remote Desktop Services],described, termserv.iworkspacerestyperegistry, workspaceax/IWorkspaceResTypeRegistry
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: WOF_FILE_COMPRESSION_INFO_V1, *PWOF_FILE_COMPRESSION_INFO_V1
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tsworkspace.dll
api_name:
 - IWorkspaceResTypeRegistry
product: Windows
targetos: Windows
req.lib: 
req.dll: Tsworkspace.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWorkspaceResTypeRegistry interface


## -description


Exposes methods that allow a plug-in to manage third-party file name extensions in RemoteApp and Desktop Connection runtime. This interface is implemented by the Remote Desktop Services workspace runtime. These methods are called by custom clients.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWorkspaceResTypeRegistry</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IWorkspaceResTypeRegistry</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/0f4b82a6-1eca-4890-aa0c-1e4c5821cd33">AddResourceType</a>
</td>
<td align="left" width="63%">
Registers a third-party file name extension with the RemoteApp and Desktop Connections runtime.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a50bd4a0-8f59-4ed9-8f5f-c2522540c41e">DeleteResourceType</a>
</td>
<td align="left" width="63%">
Unregisters a third-party file name extension with the RemoteApp and Desktop Connections runtime.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e86c93d4-d5da-4d44-b1ea-641cb1fcceb4">GetRegisteredFileExtensions</a>
</td>
<td align="left" width="63%">
Retrieves the third-party file name extensions that are registered with the RemoteApp and Desktop Connections runtime.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/60fa6676-c098-41b6-bebd-0a600ca37954">GetResourceTypeInfo</a>
</td>
<td align="left" width="63%">
Retrieves information about a third-party file name extension that is registered with the RemoteApp and Desktop Connections runtime.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a1feac54-218c-4c17-87d6-27d764d355f9">ModifyResourceType</a>
</td>
<td align="left" width="63%">
Modifies a third-party file name extension that is registered with the RemoteApp and Desktop Connections runtime.

</td>
</tr>
</table> 

