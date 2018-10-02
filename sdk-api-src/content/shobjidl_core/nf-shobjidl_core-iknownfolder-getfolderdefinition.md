---
UID: NF:shobjidl_core.IKnownFolder.GetFolderDefinition
title: IKnownFolder::GetFolderDefinition
author: windows-sdk-content
description: Retrieves a structure that contains the defining elements of a known folder, which includes the folder's category, name, path, description, tooltip, icon, and other properties.
old-location: shell\IKnownFolder_GetFolderDefinition.htm
tech.root: Shell
ms.assetid: b6f544cc-f487-405c-915d-b3a6dc59422c
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: GetFolderDefinition, GetFolderDefinition method [Windows Shell], GetFolderDefinition method [Windows Shell],IKnownFolder interface, IKnownFolder interface [Windows Shell],GetFolderDefinition method, IKnownFolder.GetFolderDefinition, IKnownFolder::GetFolderDefinition, _shell_IKnownFolder_GetFolderDefinition, shell.IKnownFolder_GetFolderDefinition, shobjidl_core/IKnownFolder::GetFolderDefinition
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - shobjidl_core.h
api_name:
 - IKnownFolder.GetFolderDefinition
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IKnownFolder::GetFolderDefinition


## -description


Retrieves a structure that contains the defining elements of a known folder, which includes the folder's category, name, path, description, tooltip, icon, and other properties.


## -parameters




### -param pKFD [out]

Type: <b><a href="https://msdn.microsoft.com/08bd8406-68fa-4e02-9a64-ed5e62f8639b">KNOWNFOLDER_DEFINITION</a>*</b>

When this method returns, contains a pointer to the <a href="https://msdn.microsoft.com/08bd8406-68fa-4e02-9a64-ed5e62f8639b">KNOWNFOLDER_DEFINITION</a> structure. When no longer needed, the calling application is responsible for calling <a href="https://msdn.microsoft.com/0ad17dd3-e612-403a-b8c3-e93d5f259c1f">FreeKnownFolderDefinitionFields</a> to free this resource.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When a third-party application creates their own known folder, they do so by defining it with a <a href="https://msdn.microsoft.com/08bd8406-68fa-4e02-9a64-ed5e62f8639b">KNOWNFOLDER_DEFINITION</a> structure, then registering it with the system. Any registered known folder definition information—system-provided or application-created—can be retrived through this method.

To call this method, the caller must have at least User privileges.




## -see-also




<a href="https://msdn.microsoft.com/dbade93d-73f6-401b-9986-4e6fd439c874">IKnownFolder</a>



<a href="https://msdn.microsoft.com/49799A9E-BA86-4977-B5F3-590BE1E5FBF6">Known Folders Sample</a>
 

 

