---
UID: NF:workspaceax.IWorkspaceResTypeRegistry.AddResourceType
title: IWorkspaceResTypeRegistry::AddResourceType (workspaceax.h)
description: Registers a third-party file name extension with the RemoteApp and Desktop Connections runtime.
helpviewer_keywords: ["AddResourceType","AddResourceType method [Remote Desktop Services]","AddResourceType method [Remote Desktop Services]","IWorkspaceResTypeRegistry interface","AddResourceType method [Remote Desktop Services]","Workspace object","IWorkspaceResTypeRegistry interface [Remote Desktop Services]","AddResourceType method","IWorkspaceResTypeRegistry.AddResourceType","IWorkspaceResTypeRegistry::AddResourceType","Workspace object [Remote Desktop Services]","AddResourceType method","termserv.iworkspacerestyperegistry_addresourcetype","workspaceax/IWorkspaceResTypeRegistry::AddResourceType"]
old-location: termserv\iworkspacerestyperegistry_addresourcetype.htm
tech.root: TermServ
ms.assetid: 0f4b82a6-1eca-4890-aa0c-1e4c5821cd33
ms.date: 12/05/2018
ms.keywords: AddResourceType, AddResourceType method [Remote Desktop Services], AddResourceType method [Remote Desktop Services],IWorkspaceResTypeRegistry interface, AddResourceType method [Remote Desktop Services],Workspace object, IWorkspaceResTypeRegistry interface [Remote Desktop Services],AddResourceType method, IWorkspaceResTypeRegistry.AddResourceType, IWorkspaceResTypeRegistry::AddResourceType, Workspace object [Remote Desktop Services],AddResourceType method, termserv.iworkspacerestyperegistry_addresourcetype, workspaceax/IWorkspaceResTypeRegistry::AddResourceType
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWorkspaceResTypeRegistry::AddResourceType
 - workspaceax/IWorkspaceResTypeRegistry::AddResourceType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - TSWorkspace.dll
api_name:
 - IWorkspaceResTypeRegistry.AddResourceType
 - Workspace.AddResourceType
---

# IWorkspaceResTypeRegistry::AddResourceType


## -description

Registers a third-party file name extension with the RemoteApp and Desktop Connections runtime.

## -parameters

### -param fMachineWide [in]

Specifies whether the resource is to be registered per user or per machine.



#### VARIANT_TRUE

The resource is registered per machine.



#### VARIANT_FALSE

The resource is registered per user.

### -param bstrFileExtension [in]

A string that contains the file name extension to register. The period must be included in the extension, for example, ".txt".

### -param bstrLauncher [in]

A string that contains the fully qualified path and file name of the application to use to launch files with the extension specified by the <i>bstrFileExtension</i> parameter.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is called when the plug-in is installed to register non-RDP resources.

## -see-also

<a href="/windows/desktop/api/workspaceax/nn-workspaceax-iworkspacerestyperegistry">IWorkspaceResTypeRegistry</a>