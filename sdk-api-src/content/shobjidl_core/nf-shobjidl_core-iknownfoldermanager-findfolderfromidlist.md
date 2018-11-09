---
UID: NF:shobjidl_core.IKnownFolderManager.FindFolderFromIDList
title: IKnownFolderManager::FindFolderFromIDList
author: windows-sdk-content
description: Gets an object that represents a known folder based on an IDList. The object allows you to query certain folder properties, get the current path of the folder, redirect the folder to another location, and get the path of the folder as an ITEMIDLIST.
old-location: shell\IKnownFolderManager_FindFolderFromIDList.htm
tech.root: shell
ms.assetid: fda3e390-e436-47ab-9339-2abf30b53ba9
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: FindFolderFromIDList, FindFolderFromIDList method [Windows Shell], FindFolderFromIDList method [Windows Shell],IKnownFolderManager interface, IKnownFolderManager interface [Windows Shell],FindFolderFromIDList method, IKnownFolderManager.FindFolderFromIDList, IKnownFolderManager::FindFolderFromIDList, _shell_IKnownFolderManager_FindFolderFromIDList, shell.IKnownFolderManager_FindFolderFromIDList, shobjidl_core/IKnownFolderManager::FindFolderFromIDList
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
 - IKnownFolderManager.FindFolderFromIDList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IKnownFolderManager::FindFolderFromIDList


## -description


Gets an object that represents a known folder based on an IDList. The object allows you to query certain folder properties, get the current path of the folder, redirect the folder to another location, and get the path of the folder as an <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a>.


## -parameters




### -param pidl [in]

Type: <b>PCIDLIST_ABSOLUTE</b>

A pointer to the IDList.


### -param ppkf [out]

Type: <b><a href="https://msdn.microsoft.com/dbade93d-73f6-401b-9986-4e6fd439c874">IKnownFolder</a>**</b>

When this method returns, contains the address of a pointer to the <a href="https://msdn.microsoft.com/dbade93d-73f6-401b-9986-4e6fd439c874">IKnownFolder</a> object that represents the known folder.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/ba7dbef7-2732-49e8-b573-a3b731bdc633">IKnownFolderManager</a>



<a href="https://msdn.microsoft.com/49799A9E-BA86-4977-B5F3-590BE1E5FBF6">Known Folders Sample</a>
 

 

