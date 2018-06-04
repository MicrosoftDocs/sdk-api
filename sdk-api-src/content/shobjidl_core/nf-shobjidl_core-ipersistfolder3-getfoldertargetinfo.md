---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IPersistFolder3::GetFolderTargetInfo


## -description


Provides the location and attributes of a folder shortcut's target folder.


## -parameters




### -param ppfti [out]

Type: <b><a href="https://msdn.microsoft.com/74441551-c315-4203-a4f5-cd4e6c57b58b">PERSIST_FOLDER_TARGET_INFO</a>*</b>


          A pointer to a <a href="https://msdn.microsoft.com/74441551-c315-4203-a4f5-cd4e6c57b58b">PERSIST_FOLDER_TARGET_INFO</a> structure used to return the target folder's location and attributes.
        


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




        The <a href="https://msdn.microsoft.com/74441551-c315-4203-a4f5-cd4e6c57b58b">PERSIST_FOLDER_TARGET_INFO</a> structure might not be initialized by the caller. <b>GetFolderTargetInfo</b> must assign values to all members of the structure before returning it to the caller.
      



