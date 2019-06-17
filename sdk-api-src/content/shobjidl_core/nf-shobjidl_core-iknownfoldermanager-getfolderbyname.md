---
UID: NF:shobjidl_core.IKnownFolderManager.GetFolderByName
title: IKnownFolderManager::GetFolderByName (shobjidl_core.h)
author: windows-sdk-content
description: Gets an object that represents a known folder identified by its canonical name.
old-location: shell\IKnownFolderManager_GetFolderByName.htm
tech.root: shell
ms.assetid: cfabc06c-825d-488d-919e-4cd9109eae52
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetFolderByName, GetFolderByName method [Windows Shell], GetFolderByName method [Windows Shell],IKnownFolderManager interface, IKnownFolderManager interface [Windows Shell],GetFolderByName method, IKnownFolderManager.GetFolderByName, IKnownFolderManager::GetFolderByName, _shell_IKnownFolderManager_GetFolderByName, shell.IKnownFolderManager_GetFolderByName, shobjidl_core/IKnownFolderManager::GetFolderByName
ms.topic: method
f1_keywords: ["shobjidl_core/IKnownFolderManager.GetFolderByName"]
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
ms.custom: 19H1
---

# IKnownFolderManager::GetFolderByName


## -description


Gets an object that represents a known folder identified by its canonical name. The object allows you to query certain folder properties, get the current path of the folder, redirect the folder to another location, and get the path of the folder as an <a href="https://docs.microsoft.com/windows/desktop/api/shtypes/ns-shtypes-_itemidlist">ITEMIDLIST</a>.


## -parameters




### -param pszCanonicalName [in]

Type: <b>LPCWSTR</b>

A pointer to the non-localized, canonical name for the known folder, stored as a null-terminated Unicode string. If this folder is a <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/ne-shobjidl_core-kf_category">common</a> or <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/ne-shobjidl_core-kf_category">per-user</a> folder, this value is also used as the value name of the "User Shell Folders" registry settings. This value is retrieved through the <b>pszName</b> member of the folder's <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/ns-shobjidl_core-knownfolder_definition">KNOWNFOLDER_DEFINITION</a> structure.


### -param ppkf [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder">IKnownFolder</a>**</b>

When this method returns, contains the address of a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder">IKnownFolder</a> object that represents the known folder.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Use this method when you know exactly which known folder you are looking for and want to access it directly.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfoldermanager">IKnownFolderManager</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd940364(v=vs.85)">Known Folders Sample</a>
 

 

