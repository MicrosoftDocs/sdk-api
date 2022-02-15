---
UID: NF:workspaceax.IWorkspaceResTypeRegistry.GetResourceTypeInfo
title: IWorkspaceResTypeRegistry::GetResourceTypeInfo (workspaceax.h)
description: Retrieves information about a third-party file name extension that is registered with the RemoteApp and Desktop Connections runtime.
helpviewer_keywords: ["GetResourceTypeInfo","GetResourceTypeInfo method [Remote Desktop Services]","GetResourceTypeInfo method [Remote Desktop Services]","IWorkspaceResTypeRegistry interface","GetResourceTypeInfo method [Remote Desktop Services]","Workspace object","IWorkspaceResTypeRegistry interface [Remote Desktop Services]","GetResourceTypeInfo method","IWorkspaceResTypeRegistry.GetResourceTypeInfo","IWorkspaceResTypeRegistry::GetResourceTypeInfo","Workspace object [Remote Desktop Services]","GetResourceTypeInfo method","termserv.iworkspacerestyperegistry_getresourcetypeinfo","workspaceax/IWorkspaceResTypeRegistry::GetResourceTypeInfo"]
old-location: termserv\iworkspacerestyperegistry_getresourcetypeinfo.htm
tech.root: TermServ
ms.assetid: 60fa6676-c098-41b6-bebd-0a600ca37954
ms.date: 12/05/2018
ms.keywords: GetResourceTypeInfo, GetResourceTypeInfo method [Remote Desktop Services], GetResourceTypeInfo method [Remote Desktop Services],IWorkspaceResTypeRegistry interface, GetResourceTypeInfo method [Remote Desktop Services],Workspace object, IWorkspaceResTypeRegistry interface [Remote Desktop Services],GetResourceTypeInfo method, IWorkspaceResTypeRegistry.GetResourceTypeInfo, IWorkspaceResTypeRegistry::GetResourceTypeInfo, Workspace object [Remote Desktop Services],GetResourceTypeInfo method, termserv.iworkspacerestyperegistry_getresourcetypeinfo, workspaceax/IWorkspaceResTypeRegistry::GetResourceTypeInfo
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
 - IWorkspaceResTypeRegistry::GetResourceTypeInfo
 - workspaceax/IWorkspaceResTypeRegistry::GetResourceTypeInfo
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
 - IWorkspaceResTypeRegistry.GetResourceTypeInfo
 - Workspace.GetResourceTypeInfo
---

# IWorkspaceResTypeRegistry::GetResourceTypeInfo


## -description

Retrieves information about a third-party file name extension that is registered with the RemoteApp and Desktop Connections runtime.

## -parameters

### -param fMachineWide [in]

Specifies whether the resource is registered per user or per machine.



#### VARIANT_TRUE

The resource is registered per machine.



#### VARIANT_FALSE

The resource is registered per user.

### -param bstrFileExtension [in]

A string that contains the file name extension to retrieve the information for. The period must be included in the extension, for example, ".txt".

### -param pbstrLauncher [out, retval]

A pointer to a <b>BSTR</b> variable that receives the fully qualified path and file name of the application to use to launch files with the extension specified by the <i>bstrFileExtension</i> parameter.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/workspaceax/nn-workspaceax-iworkspacerestyperegistry">IWorkspaceResTypeRegistry</a>