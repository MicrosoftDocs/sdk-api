---
UID: NF:shobjidl_core.IKnownFolderManager.UnregisterFolder
title: IKnownFolderManager::UnregisterFolder
author: windows-sdk-content
description: Remove a known folder from the registry, which makes it unknown to the known folder system. This method does not remove the folder itself.
old-location: shell\IKnownFolderManager_UnregisterFolder.htm
old-project: shell
ms.assetid: 2c66f5e3-3479-414c-8888-0a888708dbe0
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IKnownFolderManager interface [Windows Shell],UnregisterFolder method, IKnownFolderManager.UnregisterFolder, IKnownFolderManager::UnregisterFolder, UnregisterFolder, UnregisterFolder method [Windows Shell], UnregisterFolder method [Windows Shell],IKnownFolderManager interface, _shell_IKnownFolderManager_UnregisterFolder, shell.IKnownFolderManager_UnregisterFolder, shobjidl_core/IKnownFolderManager::UnregisterFolder
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.redist: 
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
 - IKnownFolderManager.UnregisterFolder
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: Outlook Express 6.0
---

# IKnownFolderManager::UnregisterFolder


## -description


Remove a known folder from the registry, which makes it unknown to the known folder system. This method does not remove the folder itself.


## -parameters




### -param rfid [in]

Type: <b>REFKNOWNFOLDERID</b>

<b>GUID</b> or <a href="https://msdn.microsoft.com/f2c08ade-3083-44e4-82b0-dde45f0e3094">KNOWNFOLDERID</a> that represents the known folder.


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
Among other things, this value can indicate that the <i>rfid</i> parameter references a <a href="https://msdn.microsoft.com/f2c08ade-3083-44e4-82b0-dde45f0e3094">KNOWNFOLDERID</a> that is not present on the system. Not all <b>KNOWNFOLDERID</b> values are present on all systems. Use <a href="https://msdn.microsoft.com/3ac09fc4-15c4-4346-94ad-2a4617c463d1">IKnownFolderManager::GetFolderIds</a> to retrieve the set of <b>KNOWNFOLDERID</b> values known to the current system.

</td>
</tr>
</table>
 




## -remarks



<div class="alert"><b>Note</b>  This method updates <b>HKEY_LOCAL_MACHINE</b> and needs to be run in the context of an administrator. Setup programs need administrator privileges to register or unregister a known folder.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/ba7dbef7-2732-49e8-b573-a3b731bdc633">IKnownFolderManager</a>



<a href="https://msdn.microsoft.com/1b3d492f-26a3-4f04-ba01-768ebad39e1b">IKnownFolderManager::RegisterFolder</a>



<a href="https://msdn.microsoft.com/49799A9E-BA86-4977-B5F3-590BE1E5FBF6">Known Folders Sample</a>
 

 

