---
UID: NF:shobjidl_core.IKnownFolderManager.GetFolderByName
title: IKnownFolderManager::GetFolderByName
author: windows-sdk-content
description: Gets an object that represents a known folder identified by its canonical name.
old-location: shell\IKnownFolderManager_GetFolderByName.htm
tech.root: shell
ms.assetid: cfabc06c-825d-488d-919e-4cd9109eae52
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: GetFolderByName, GetFolderByName method [Windows Shell], GetFolderByName method [Windows Shell],IKnownFolderManager interface, IKnownFolderManager interface [Windows Shell],GetFolderByName method, IKnownFolderManager.GetFolderByName, IKnownFolderManager::GetFolderByName, _shell_IKnownFolderManager_GetFolderByName, shell.IKnownFolderManager_GetFolderByName, shobjidl_core/IKnownFolderManager::GetFolderByName
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
 - IKnownFolderManager.GetFolderByName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IKnownFolderManager::GetFolderByName


## -description


Gets an object that represents a known folder identified by its canonical name. The object allows you to query certain folder properties, get the current path of the folder, redirect the folder to another location, and get the path of the folder as an <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a>.


## -parameters




### -param pszCanonicalName [in]

Type: <b>LPCWSTR</b>

A pointer to the non-localized, canonical name for the known folder, stored as a null-terminated Unicode string. If this folder is a <a href="https://msdn.microsoft.com/2ca0d3e2-bb4c-4a28-90d6-fe2852373b88">common</a> or <a href="https://msdn.microsoft.com/2ca0d3e2-bb4c-4a28-90d6-fe2852373b88">per-user</a> folder, this value is also used as the value name of the "User Shell Folders" registry settings. This value is retrieved through the <b>pszName</b> member of the folder's <a href="https://msdn.microsoft.com/08bd8406-68fa-4e02-9a64-ed5e62f8639b">KNOWNFOLDER_DEFINITION</a> structure.


### -param ppkf [out]

Type: <b><a href="https://msdn.microsoft.com/dbade93d-73f6-401b-9986-4e6fd439c874">IKnownFolder</a>**</b>

When this method returns, contains the address of a pointer to the <a href="https://msdn.microsoft.com/dbade93d-73f6-401b-9986-4e6fd439c874">IKnownFolder</a> object that represents the known folder.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Use this method when you know exactly which known folder you are looking for and want to access it directly.




## -see-also




<a href="https://msdn.microsoft.com/ba7dbef7-2732-49e8-b573-a3b731bdc633">IKnownFolderManager</a>



<a href="https://msdn.microsoft.com/49799A9E-BA86-4977-B5F3-590BE1E5FBF6">Known Folders Sample</a>
 

 

