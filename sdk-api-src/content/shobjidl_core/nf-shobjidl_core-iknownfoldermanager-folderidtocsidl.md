---
UID: NF:shobjidl_core.IKnownFolderManager.FolderIdToCsidl
title: IKnownFolderManager::FolderIdToCsidl
author: windows-sdk-content
description: Gets the legacy CSIDL value that is the equivalent of a given KNOWNFOLDERID.
old-location: shell\IKnownFolderManager_FolderIdToCsidl.htm
tech.root: shell
ms.assetid: 27bd8c79-34ff-44ee-ad99-aa079af7da89
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: FolderIdToCsidl, FolderIdToCsidl method [Windows Shell], FolderIdToCsidl method [Windows Shell],IKnownFolderManager interface, IKnownFolderManager interface [Windows Shell],FolderIdToCsidl method, IKnownFolderManager.FolderIdToCsidl, IKnownFolderManager::FolderIdToCsidl, _shell_IKnownFolderManager_FolderIdToCsidl, shell.IKnownFolderManager_FolderIdToCsidl, shobjidl_core/IKnownFolderManager::FolderIdToCsidl
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
req.dll: Shell32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IKnownFolderManager.FolderIdToCsidl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IKnownFolderManager::FolderIdToCsidl


## -description


Gets the legacy <a href="https://msdn.microsoft.com/33d92271-2865-4ebd-b96c-bf293deb4310">CSIDL</a> value that is the equivalent of a given <a href="https://msdn.microsoft.com/f2c08ade-3083-44e4-82b0-dde45f0e3094">KNOWNFOLDERID</a>.


## -parameters




### -param rfid [in]

Type: <b>REFKNOWNFOLDERID</b>

Reference to the <a href="https://msdn.microsoft.com/f2c08ade-3083-44e4-82b0-dde45f0e3094">KNOWNFOLDERID</a>.


### -param pnCsidl [out]

Type: <b>int*</b>

When this method returns, contains a pointer to the <a href="https://msdn.microsoft.com/33d92271-2865-4ebd-b96c-bf293deb4310">CSIDL</a> value. This pointer is passed uninitialized.


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
Among other things, this value can indicate that the <i>rfid</i> parameter references a <a href="https://msdn.microsoft.com/f2c08ade-3083-44e4-82b0-dde45f0e3094">KNOWNFOLDERID</a> that is not present on the system. Not all <b>KNOWNFOLDERID</b> values are present on all systems. Use <a href="https://msdn.microsoft.com/3ac09fc4-15c4-4346-94ad-2a4617c463d1">IKnownFolderManager::GetFolderIds</a> to retrieve the set of <b>KNOWNFOLDERID</b> values for the current system.

</td>
</tr>
</table>
 




## -remarks



To call this method, the caller must have at least User privileges.




## -see-also




<a href="https://msdn.microsoft.com/ba7dbef7-2732-49e8-b573-a3b731bdc633">IKnownFolderManager</a>



<a href="https://msdn.microsoft.com/8c819558-8cbd-4576-98e6-99efa39ca5a6">IKnownFolderManager::FolderIdFromCsidl</a>



<a href="https://msdn.microsoft.com/49799A9E-BA86-4977-B5F3-590BE1E5FBF6">Known Folders Sample</a>
 

 

