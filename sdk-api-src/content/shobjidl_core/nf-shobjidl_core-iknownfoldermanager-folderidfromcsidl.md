---
UID: NF:shobjidl_core.IKnownFolderManager.FolderIdFromCsidl
title: IKnownFolderManager::FolderIdFromCsidl
author: windows-sdk-content
description: Gets the KNOWNFOLDERID that is the equivalent of a legacy CSIDL value.
old-location: shell\IKnownFolderManager_FolderIdFromCsidl.htm
old-project: shell
ms.assetid: 8c819558-8cbd-4576-98e6-99efa39ca5a6
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: FolderIdFromCsidl, FolderIdFromCsidl method [Windows Shell], FolderIdFromCsidl method [Windows Shell],IKnownFolderManager interface, IKnownFolderManager interface [Windows Shell],FolderIdFromCsidl method, IKnownFolderManager.FolderIdFromCsidl, IKnownFolderManager::FolderIdFromCsidl, _shell_IKnownFolderManager_FolderIdFromCsidl, shell.IKnownFolderManager_FolderIdFromCsidl, shobjidl_core/IKnownFolderManager::FolderIdFromCsidl
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
 - IKnownFolderManager.FolderIdFromCsidl
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: Outlook Express 6.0
---

# IKnownFolderManager::FolderIdFromCsidl


## -description


Gets the <a href="https://msdn.microsoft.com/f2c08ade-3083-44e4-82b0-dde45f0e3094">KNOWNFOLDERID</a> that is the equivalent of a legacy <a href="https://msdn.microsoft.com/33d92271-2865-4ebd-b96c-bf293deb4310">CSIDL</a> value.


## -parameters




### -param nCsidl [in]

Type: <b>int</b>

The <a href="https://msdn.microsoft.com/33d92271-2865-4ebd-b96c-bf293deb4310">CSIDL</a> value.


### -param pfid [out]

Type: <b><a href="https://msdn.microsoft.com/f2c08ade-3083-44e4-82b0-dde45f0e3094">KNOWNFOLDERID</a>*</b>

When this method returns, contains a pointer to the <a href="https://msdn.microsoft.com/f2c08ade-3083-44e4-82b0-dde45f0e3094">KNOWNFOLDERID</a>. This pointer is passed uninitialized.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To call this method, the caller must have at least User privileges.




## -see-also




<a href="https://msdn.microsoft.com/ba7dbef7-2732-49e8-b573-a3b731bdc633">IKnownFolderManager</a>



<a href="https://msdn.microsoft.com/27bd8c79-34ff-44ee-ad99-aa079af7da89">IKnownFolderManager::FolderIdToCsidl</a>



<a href="https://msdn.microsoft.com/49799A9E-BA86-4977-B5F3-590BE1E5FBF6">Known Folders Sample</a>
 

 

