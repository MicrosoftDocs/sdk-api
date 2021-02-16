---
UID: NF:shobjidl_core.IKnownFolderManager.GetFolder
title: IKnownFolderManager::GetFolder (shobjidl_core.h)
description: Gets an object that represents a known folder identified by its KNOWNFOLDERID.
helpviewer_keywords: ["GetFolder","GetFolder method [Windows Shell]","GetFolder method [Windows Shell]","IKnownFolderManager interface","IKnownFolderManager interface [Windows Shell]","GetFolder method","IKnownFolderManager.GetFolder","IKnownFolderManager::GetFolder","_shell_IKnownFolderManager_GetFolder","shell.IKnownFolderManager_GetFolder","shobjidl_core/IKnownFolderManager::GetFolder"]
old-location: shell\IKnownFolderManager_GetFolder.htm
tech.root: shell
ms.assetid: bd8dba51-c711-4f7c-af53-00c80f211cb8
ms.date: 12/05/2018
ms.keywords: GetFolder, GetFolder method [Windows Shell], GetFolder method [Windows Shell],IKnownFolderManager interface, IKnownFolderManager interface [Windows Shell],GetFolder method, IKnownFolderManager.GetFolder, IKnownFolderManager::GetFolder, _shell_IKnownFolderManager_GetFolder, shell.IKnownFolderManager_GetFolder, shobjidl_core/IKnownFolderManager::GetFolder
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
 - IKnownFolderManager::GetFolder
 - shobjidl_core/IKnownFolderManager::GetFolder
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
 - IKnownFolderManager.GetFolder
---

# IKnownFolderManager::GetFolder


## -description

Gets an object that represents a known folder identified by its <a href="/windows/desktop/shell/knownfolderid">KNOWNFOLDERID</a>. The object allows you to query certain folder properties, get the current path of the folder, redirect the folder to another location, and get the path of the folder as an <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a>.

## -parameters

### -param rfid [in]

Type: <b>REFKNOWNFOLDERID</b>

Reference to the <a href="/windows/desktop/shell/knownfolderid">KNOWNFOLDERID</a>.

### -param ppkf [out]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder">IKnownFolder</a>**</b>

When this method returns, contains an interface pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder">IKnownFolder</a> object that represents the folder.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise, including the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Among other things, this value can indicate that the <i>rfid</i> parameter references a <a href="/windows/desktop/shell/knownfolderid">KNOWNFOLDERID</a> that is not present on the system. Not all <b>KNOWNFOLDERID</b> values are present on all systems. Use <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-getfolderids">IKnownFolderManager::GetFolderIds</a> to retrieve the set of <b>KNOWNFOLDERID</b> values for the current system.

</td>
</tr>
</table>

## -remarks

To call this method, the caller must have at least User privileges.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Use this method when you know exactly which known folder you are looking for and want to access it directly.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfoldermanager">IKnownFolderManager</a>



<a href="/previous-versions/windows/desktop/legacy/dd940364(v=vs.85)">Known Folders Sample</a>