---
UID: NF:shobjidl_core.IKnownFolderManager.GetFolderIds
title: IKnownFolderManager::GetFolderIds
author: windows-sdk-content
description: Gets an array of all registered known folder IDs. This can be used in enumerating all known folders.
old-location: shell\IKnownFolderManager_GetFolderIds.htm
tech.root: shell
ms.assetid: 3ac09fc4-15c4-4346-94ad-2a4617c463d1
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: GetFolderIds, GetFolderIds method [Windows Shell], GetFolderIds method [Windows Shell],IKnownFolderManager interface, IKnownFolderManager interface [Windows Shell],GetFolderIds method, IKnownFolderManager.GetFolderIds, IKnownFolderManager::GetFolderIds, _shell_IKnownFolderManager_GetFolderIds, shell.IKnownFolderManager_GetFolderIds, shobjidl_core/IKnownFolderManager::GetFolderIds
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
 - IKnownFolderManager.GetFolderIds
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IKnownFolderManager::GetFolderIds


## -description


Gets an array of all registered known folder IDs. This can be used in enumerating all known folders.


## -parameters




### -param ppKFId [out]

Type: <b><a href="https://msdn.microsoft.com/f2c08ade-3083-44e4-82b0-dde45f0e3094">KNOWNFOLDERID</a>**</b>

When this method returns, contains a pointer to an array of all <a href="https://msdn.microsoft.com/f2c08ade-3083-44e4-82b0-dde45f0e3094">KNOWNFOLDERID</a> values registered with the system. Use <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> to free these resources when they are no longer needed.


### -param pCount [in, out]

Type: <b>UINT*</b>

When this method returns, contains a pointer to the number of <a href="https://msdn.microsoft.com/f2c08ade-3083-44e4-82b0-dde45f0e3094">KNOWNFOLDERID</a> values in the array at <i>ppKFId</i>. The [in] functionality of this parameter is not used.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The caller of this method must have User privileges.

You can use <a href="https://msdn.microsoft.com/61210ebd-cbf3-4e78-b077-53d2779053eb">StringFromCLSID</a> or <a href="https://msdn.microsoft.com/5f437658-b749-416b-805a-2afdac682660">StringFromGUID2</a> to convert the retrieved <a href="https://msdn.microsoft.com/f2c08ade-3083-44e4-82b0-dde45f0e3094">KNOWNFOLDERID</a> values to strings.




## -see-also




<a href="https://msdn.microsoft.com/ba7dbef7-2732-49e8-b573-a3b731bdc633">IKnownFolderManager</a>



<a href="https://msdn.microsoft.com/49799A9E-BA86-4977-B5F3-590BE1E5FBF6">Known Folders Sample</a>
 

 

