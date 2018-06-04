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

# _lopen function


## -description


The _lopen function opens an existing file and sets the file pointer to the beginning of the file. This function is provided for compatibility with 16-bit versions of Windows. Win32-based applications should use the CreateFile function. 


## -parameters




### -param lpPathName

Pointer to a null-terminated string that names the file to open. The string must consist of characters from the Windows ANSI character set.


### -param iReadWrite

Specifies the modes in which to open the file. This parameter consists of one access mode and an optional share mode. The access mode must be one of the following values: OF_READ,  OF_READWRITE, OF_WRITE

The share mode can be one of the following values: OF_SHARE_COMPAT,  OF_SHARE_DENY_NONE, OF_SHARE_DENY_READ, OF_SHARE_DENY_WRITE, OF_SHARE_EXCLUSIVE


## -returns



If the function succeeds, the return value is a file handle.



