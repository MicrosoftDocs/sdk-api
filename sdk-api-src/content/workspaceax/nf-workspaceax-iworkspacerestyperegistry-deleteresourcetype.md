---
UID: NF:workspaceax.IWorkspaceResTypeRegistry.DeleteResourceType
title: IWorkspaceResTypeRegistry::DeleteResourceType (workspaceax.h)
author: windows-sdk-content
description: Unregisters a third-party file name extension with the RemoteApp and Desktop Connections runtime.
old-location: termserv\iworkspacerestyperegistry_deleteresourcetype.htm
tech.root: TermServ
ms.assetid: a50bd4a0-8f59-4ed9-8f5f-c2522540c41e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DeleteResourceType, DeleteResourceType method [Remote Desktop Services], DeleteResourceType method [Remote Desktop Services],IWorkspaceResTypeRegistry interface, DeleteResourceType method [Remote Desktop Services],Workspace object, IWorkspaceResTypeRegistry interface [Remote Desktop Services],DeleteResourceType method, IWorkspaceResTypeRegistry.DeleteResourceType, IWorkspaceResTypeRegistry::DeleteResourceType, Workspace object [Remote Desktop Services],DeleteResourceType method, termserv.iworkspacerestyperegistry_deleteresourcetype, workspaceax/IWorkspaceResTypeRegistry::DeleteResourceType
ms.topic: method
f1_keywords: ["workspaceax/IWorkspaceResTypeRegistry.DeleteResourceType"]
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
req.type-library: TSWorkspace.dll
req.lib: 
req.dll: TSWorkspace.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - TSWorkspace.dll
api_name:
 - IWorkspaceResTypeRegistry.DeleteResourceType
 - Workspace.DeleteResourceType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWorkspaceResTypeRegistry::DeleteResourceType


## -description


Unregisters a third-party file name extension with the RemoteApp and Desktop Connections 
   runtime.


## -parameters




### -param fMachineWide [in]

Specifies whether the resource is registered per user or per machine.



#### VARIANT_TRUE

The resource is registered per machine.



#### VARIANT_FALSE

The resource is registered per user.


### -param bstrFileExtension [in]

A string that contains the file name extension to unregister. The period must be included in the extension, 
   for example, ".txt".


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is called when the plug-in is uninstalled to unregister non-RDP resources.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/workspaceax/nn-workspaceax-iworkspacerestyperegistry">IWorkspaceResTypeRegistry</a>
 

 

