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

# IFileSyncMergeHandler::Merge


## -description




## -parameters




### -param localFilePath [in]

Type: <b>LPCWSTR</b>

A pointer to a string containing the path to the local copy of the file.


### -param serverFilePath [in]

Type: <b>LPCWSTR</b>

A pointer to a string containing the network path to the server copy of the file.


### -param updateStatus [out]

Type: <b>MERGE_UPDATE_STATUS*</b>

When this method returns, contains a pointer to one of the following values indicating status of the merge process.



#### MUS_COMPLETE

Indicates that the process has completed successfully.



#### MUS_USERINPUTNEEDED

Indicates that additional input is required by the user for the process to complete.



#### MUS_FAILED

Indicates that the process has failed.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/467BF7B9-184E-409F-B5B7-F95E9891C2CD">IFileSyncMergeHandler</a>
 

 

