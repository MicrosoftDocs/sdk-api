---
UID: NF:shobjidl_core.IKnownFolderManager.UnregisterFolder
title: IKnownFolderManager::UnregisterFolder (shobjidl_core.h)
description: Remove a known folder from the registry, which makes it unknown to the known folder system. This method does not remove the folder itself.
helpviewer_keywords: ["IKnownFolderManager interface [Windows Shell]","UnregisterFolder method","IKnownFolderManager.UnregisterFolder","IKnownFolderManager::UnregisterFolder","UnregisterFolder","UnregisterFolder method [Windows Shell]","UnregisterFolder method [Windows Shell]","IKnownFolderManager interface","_shell_IKnownFolderManager_UnregisterFolder","shell.IKnownFolderManager_UnregisterFolder","shobjidl_core/IKnownFolderManager::UnregisterFolder"]
old-location: shell\IKnownFolderManager_UnregisterFolder.htm
tech.root: shell
ms.assetid: 2c66f5e3-3479-414c-8888-0a888708dbe0
ms.date: 12/05/2018
ms.keywords: IKnownFolderManager interface [Windows Shell],UnregisterFolder method, IKnownFolderManager.UnregisterFolder, IKnownFolderManager::UnregisterFolder, UnregisterFolder, UnregisterFolder method [Windows Shell], UnregisterFolder method [Windows Shell],IKnownFolderManager interface, _shell_IKnownFolderManager_UnregisterFolder, shell.IKnownFolderManager_UnregisterFolder, shobjidl_core/IKnownFolderManager::UnregisterFolder
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
 - IKnownFolderManager::UnregisterFolder
 - shobjidl_core/IKnownFolderManager::UnregisterFolder
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
 - IKnownFolderManager.UnregisterFolder
---

# IKnownFolderManager::UnregisterFolder


## -description

Remove a known folder from the registry, which makes it unknown to the known folder system. This method does not remove the folder itself.

## -parameters

### -param rfid [in]

Type: <b>REFKNOWNFOLDERID</b>

<b>GUID</b> or <a href="/windows/desktop/shell/knownfolderid">KNOWNFOLDERID</a> that represents the known folder.

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
Among other things, this value can indicate that the <i>rfid</i> parameter references a <a href="/windows/desktop/shell/knownfolderid">KNOWNFOLDERID</a> that is not present on the system. Not all <b>KNOWNFOLDERID</b> values are present on all systems. Use <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-getfolderids">IKnownFolderManager::GetFolderIds</a> to retrieve the set of <b>KNOWNFOLDERID</b> values known to the current system.

</td>
</tr>
</table>

## -remarks

<div class="alert"><b>Note</b>  This method updates <b>HKEY_LOCAL_MACHINE</b> and needs to be run in the context of an administrator. Setup programs need administrator privileges to register or unregister a known folder.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfoldermanager">IKnownFolderManager</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-registerfolder">IKnownFolderManager::RegisterFolder</a>



<a href="/previous-versions/windows/desktop/legacy/dd940364(v=vs.85)">Known Folders Sample</a>