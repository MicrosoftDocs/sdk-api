---
UID: NF:workspaceax.IWorkspaceResTypeRegistry.ModifyResourceType
title: IWorkspaceResTypeRegistry::ModifyResourceType
author: windows-sdk-content
description: Modifies a third-party file name extension that is registered with the RemoteApp and Desktop Connections runtime.
old-location: termserv\iworkspacerestyperegistry_modifyresourcetype.htm
tech.root: termserv
ms.assetid: a1feac54-218c-4c17-87d6-27d764d355f9
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IWorkspaceResTypeRegistry interface [Remote Desktop Services],ModifyResourceType method, IWorkspaceResTypeRegistry.ModifyResourceType, IWorkspaceResTypeRegistry::ModifyResourceType, ModifyResourceType, ModifyResourceType method [Remote Desktop Services], ModifyResourceType method [Remote Desktop Services],IWorkspaceResTypeRegistry interface, ModifyResourceType method [Remote Desktop Services],Workspace object, Workspace object [Remote Desktop Services],ModifyResourceType method, termserv.iworkspacerestyperegistry_modifyresourcetype, workspaceax/IWorkspaceResTypeRegistry::ModifyResourceType
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IWorkspaceResTypeRegistry.ModifyResourceType
 - Workspace.ModifyResourceType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWorkspaceResTypeRegistry::ModifyResourceType


## -description


Modifies a third-party file name extension that is registered with the RemoteApp and Desktop Connections runtime.


## -parameters




### -param fMachineWide [in]

Specifies whether the resource is registered per user or per machine.



#### VARIANT_TRUE

The resource is registered per machine.



#### VARIANT_FALSE

The resource is registered per user.


### -param bstrFileExtension [in]

A string that contains the file name extension to update. The period must be included in the extension, for example, ".txt".


### -param bstrLauncher [in]

A string that contains the new fully qualified path and file name of the application to use to launch files with the extension specified by the <i>bstrFileExtension</i> parameter.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/bea617a0-cd64-4c77-af27-b418178e3dad">IWorkspaceResTypeRegistry</a>
 

 

