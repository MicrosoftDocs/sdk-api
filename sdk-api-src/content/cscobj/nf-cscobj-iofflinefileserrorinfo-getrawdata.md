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

# IOfflineFilesErrorInfo::GetRawData


## -description



    Retrieves a block of bytes containing internal data associated with the error. The content of this block is intended for use by the Windows development and support teams and is subject to change in any version of Windows.  No definition of the data block is provided.


## -parameters




### -param ppBlob [out]

Receives the address of a BYTE_BLOB structure describing the raw data.  The caller must free this memory block by using the <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680722">CoTaskMemFree</a> function.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -remarks



The BYTE_BLOB structure is defined in Wtypes.h.




## -see-also




<a href="https://msdn.microsoft.com/6c78d475-aa63-49e4-863f-1a197801f2f9">IOfflineFilesErrorInfo</a>
 

 

