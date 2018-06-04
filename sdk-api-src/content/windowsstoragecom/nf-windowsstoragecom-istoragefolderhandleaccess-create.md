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

# IStorageFolderHandleAccess::Create


## -description


Creates a handle to a file that is  in a storage folder.


## -parameters




### -param fileName [in]

The name of the file that you want to get a handle to.


### -param creationOptions [in]

The action to take on a file that exists or doesn't exist.


### -param accessOptions [in]

The level of access that a handle has on the file. 


### -param sharingOptions [in]

The requested sharing mode of the handle.


### -param options [in]

The flags of the file handle.


### -param oplockBreakingHandler [in, optional]

Not currently implemented.


### -param interopHandle [out, retval]

The handle to the file.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/C579B4D9-0CD6-45D7-BE6D-54FDFB3E7753">IStorageFolderHandleAccess</a>
 

 

