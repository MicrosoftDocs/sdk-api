---
UID: NF:shobjidl_core.IKnownFolderManager.FindFolderFromIDList
title: IKnownFolderManager::FindFolderFromIDList (shobjidl_core.h)
description: Gets an object that represents a known folder based on an IDList. The object allows you to query certain folder properties, get the current path of the folder, redirect the folder to another location, and get the path of the folder as an ITEMIDLIST.
helpviewer_keywords: ["FindFolderFromIDList","FindFolderFromIDList method [Windows Shell]","FindFolderFromIDList method [Windows Shell]","IKnownFolderManager interface","IKnownFolderManager interface [Windows Shell]","FindFolderFromIDList method","IKnownFolderManager.FindFolderFromIDList","IKnownFolderManager::FindFolderFromIDList","_shell_IKnownFolderManager_FindFolderFromIDList","shell.IKnownFolderManager_FindFolderFromIDList","shobjidl_core/IKnownFolderManager::FindFolderFromIDList"]
old-location: shell\IKnownFolderManager_FindFolderFromIDList.htm
tech.root: shell
ms.assetid: fda3e390-e436-47ab-9339-2abf30b53ba9
ms.date: 12/05/2018
ms.keywords: FindFolderFromIDList, FindFolderFromIDList method [Windows Shell], FindFolderFromIDList method [Windows Shell],IKnownFolderManager interface, IKnownFolderManager interface [Windows Shell],FindFolderFromIDList method, IKnownFolderManager.FindFolderFromIDList, IKnownFolderManager::FindFolderFromIDList, _shell_IKnownFolderManager_FindFolderFromIDList, shell.IKnownFolderManager_FindFolderFromIDList, shobjidl_core/IKnownFolderManager::FindFolderFromIDList
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IKnownFolderManager::FindFolderFromIDList
 - shobjidl_core/IKnownFolderManager::FindFolderFromIDList
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IKnownFolderManager.FindFolderFromIDList
---

# IKnownFolderManager::FindFolderFromIDList


## -description

Gets an object that represents a known folder based on an IDList. The object allows you to query certain folder properties, get the current path of the folder, redirect the folder to another location, and get the path of the folder as an <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a>.

## -parameters

### -param pidl [in]

Type: <b>PCIDLIST_ABSOLUTE</b>

A pointer to the IDList.

### -param ppkf [out]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder">IKnownFolder</a>**</b>

When this method returns, contains the address of a pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder">IKnownFolder</a> object that represents the known folder.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfoldermanager">IKnownFolderManager</a>



<a href="/previous-versions/windows/desktop/legacy/dd940364(v=vs.85)">Known Folders Sample</a>