---
UID: NF:workspaceax.IWorkspaceResTypeRegistry.GetRegisteredFileExtensions
title: IWorkspaceResTypeRegistry::GetRegisteredFileExtensions
author: windows-driver-content
description: Retrieves the third-party file name extensions that are registered with the RemoteApp and Desktop Connections runtime.
old-location: termserv\iworkspacerestyperegistry_getregisteredfileextensions.htm
old-project: TermServ
ms.assetid: e86c93d4-d5da-4d44-b1ea-641cb1fcceb4
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: GetRegisteredFileExtensions, GetRegisteredFileExtensions method [Remote Desktop Services], GetRegisteredFileExtensions method [Remote Desktop Services],IWorkspaceResTypeRegistry interface, GetRegisteredFileExtensions method [Remote Desktop Services],Workspace object, IWorkspaceResTypeRegistry interface [Remote Desktop Services],GetRegisteredFileExtensions method, IWorkspaceResTypeRegistry.GetRegisteredFileExtensions, IWorkspaceResTypeRegistry::GetRegisteredFileExtensions, Workspace object [Remote Desktop Services],GetRegisteredFileExtensions method, termserv.iworkspacerestyperegistry_getregisteredfileextensions, workspaceax/IWorkspaceResTypeRegistry::GetRegisteredFileExtensions
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
req.typenames: WOF_FILE_COMPRESSION_INFO_V1, *PWOF_FILE_COMPRESSION_INFO_V1
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	TSWorkspace.dll
api_name:
-	IWorkspaceResTypeRegistry.GetRegisteredFileExtensions
-	Workspace.GetRegisteredFileExtensions
product: Windows
targetos: Windows
req.lib: 
req.dll: TSWorkspace.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWorkspaceResTypeRegistry::GetRegisteredFileExtensions


## -description


Retrieves the third-party file name extensions that are registered with the RemoteApp and Desktop Connections runtime.


## -parameters




### -param fMachineWide [in]

Specifies whether the resource is registered per user or per machine.



#### VARIANT_TRUE

The resource is registered per machine.



#### VARIANT_FALSE

The resource is registered per user.


### -param psaFileExtensions [out, retval]

The address of a pointer to a <b>SAFEARRAY</b> variable that receives an array of <b>BSTR</b>s that contain the registered file name extensions.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/bea617a0-cd64-4c77-af27-b418178e3dad">IWorkspaceResTypeRegistry</a>
 

 

