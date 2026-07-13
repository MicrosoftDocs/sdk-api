---
UID: NF:shobjidl_core.IKnownFolderManager.FindFolderFromPath
title: IKnownFolderManager::FindFolderFromPath (shobjidl_core.h)
description: Gets an object that represents a known folder based on a file system path.
helpviewer_keywords: ["FFFP_EXACTMATCH","FFFP_NEARESTPARENTMATCH","FindFolderFromPath","FindFolderFromPath method [Windows Shell]","FindFolderFromPath method [Windows Shell]","IKnownFolderManager interface","IKnownFolderManager interface [Windows Shell]","FindFolderFromPath method","IKnownFolderManager.FindFolderFromPath","IKnownFolderManager::FindFolderFromPath","_shell_IKnownFolderManager_FindFolderFromPath","shell.IKnownFolderManager_FindFolderFromPath","shobjidl_core/IKnownFolderManager::FindFolderFromPath"]
old-location: shell\IKnownFolderManager_FindFolderFromPath.htm
tech.root: shell
ms.assetid: e8033305-e5b9-499d-b794-ac3190141650
ms.date: 12/05/2018
ms.keywords: FFFP_EXACTMATCH, FFFP_NEARESTPARENTMATCH, FindFolderFromPath, FindFolderFromPath method [Windows Shell], FindFolderFromPath method [Windows Shell],IKnownFolderManager interface, IKnownFolderManager interface [Windows Shell],FindFolderFromPath method, IKnownFolderManager.FindFolderFromPath, IKnownFolderManager::FindFolderFromPath, _shell_IKnownFolderManager_FindFolderFromPath, shell.IKnownFolderManager_FindFolderFromPath, shobjidl_core/IKnownFolderManager::FindFolderFromPath
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
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IKnownFolderManager::FindFolderFromPath
 - shobjidl_core/IKnownFolderManager::FindFolderFromPath
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IKnownFolderManager.FindFolderFromPath
---

# IKnownFolderManager::FindFolderFromPath


## -description

Gets an object that represents a known folder based on a file system path. The object allows you to query certain folder properties, get the current path of the folder, redirect the folder to another location, and get the path of the folder as an <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a>.

## -parameters

### -param pszPath [in]

Type: <b>LPCWSTR</b>

Pointer to a null-terminated Unicode string of length MAX_PATH that contains a path to a known folder.

### -param mode [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-fffp_mode">FFFP_MODE</a></b>

One of the following values that specify the precision of the match of path and known folder:



#### FFFP_EXACTMATCH

Retrieve only the specific known folder for the given file path.



#### FFFP_NEARESTPARENTMATCH

If an exact match is not found for the given file path, retrieve the first known folder that matches one of its parent folders walking up the parent tree.

### -param ppkf [out]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder">IKnownFolder</a>**</b>

When this method returns, contains the address of a pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder">IKnownFolder</a> object that represents the known folder.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfoldermanager">IKnownFolderManager</a>



<a href="/previous-versions/windows/desktop/legacy/dd940364(v=vs.85)">Known Folders Sample</a>