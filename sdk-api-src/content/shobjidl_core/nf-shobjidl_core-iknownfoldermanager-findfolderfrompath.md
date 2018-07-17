---
UID: NF:shobjidl_core.IKnownFolderManager.FindFolderFromPath
title: IKnownFolderManager::FindFolderFromPath
author: windows-sdk-content
description: Gets an object that represents a known folder based on a file system path.
old-location: shell\IKnownFolderManager_FindFolderFromPath.htm
old-project: shell
ms.assetid: e8033305-e5b9-499d-b794-ac3190141650
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: FFFP_EXACTMATCH, FFFP_NEARESTPARENTMATCH, FindFolderFromPath, FindFolderFromPath method [Windows Shell], FindFolderFromPath method [Windows Shell],IKnownFolderManager interface, IKnownFolderManager interface [Windows Shell],FindFolderFromPath method, IKnownFolderManager.FindFolderFromPath, IKnownFolderManager::FindFolderFromPath, _shell_IKnownFolderManager_FindFolderFromPath, shell.IKnownFolderManager_FindFolderFromPath, shobjidl_core/IKnownFolderManager::FindFolderFromPath
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IKnownFolderManager.FindFolderFromPath
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: Outlook Express 6.0
---

# IKnownFolderManager::FindFolderFromPath


## -description


Gets an object that represents a known folder based on a file system path. The object allows you to query certain folder properties, get the current path of the folder, redirect the folder to another location, and get the path of the folder as an <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a>.


## -parameters




### -param pszPath [in]

Type: <b>LPCWSTR</b>

Pointer to a null-terminated Unicode string of length MAX_PATH that contains a path to a known folder.


### -param mode [in]

Type: <b><a href="https://msdn.microsoft.com/ffa62c36-6fdf-4644-b90d-9b5cc989de8a">FFFP_MODE</a></b>

One of the following values that specify the precision of the match of path and known folder:



#### FFFP_EXACTMATCH

Retrieve only the specific known folder for the given file path.



#### FFFP_NEARESTPARENTMATCH

If an exact match is not found for the given file path, retrieve the first known folder that matches one of its parent folders walking up the parent tree.


### -param ppkf [out]

Type: <b><a href="https://msdn.microsoft.com/dbade93d-73f6-401b-9986-4e6fd439c874">IKnownFolder</a>**</b>

When this method returns, contains the address of a pointer to the <a href="https://msdn.microsoft.com/dbade93d-73f6-401b-9986-4e6fd439c874">IKnownFolder</a> object that represents the known folder.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/ba7dbef7-2732-49e8-b573-a3b731bdc633">IKnownFolderManager</a>



<a href="https://msdn.microsoft.com/49799A9E-BA86-4977-B5F3-590BE1E5FBF6">Known Folders Sample</a>
 

 

