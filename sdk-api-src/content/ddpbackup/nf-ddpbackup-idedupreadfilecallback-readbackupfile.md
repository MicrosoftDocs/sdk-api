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

# IDedupReadFileCallback::ReadBackupFile


## -description


 Reads data from a Data Deduplication store metadata or  container file located  in the backup store.


## -parameters




### -param FileFullPath [in]

The full path from the root directory of the volume to the container file.


### -param FileOffset [in]

The offset, in bytes, from the beginning of the file to the beginning of the data to be read.


### -param SizeToRead [in]

The number of bytes to read from the file.


### -param FileBuffer [out]

A pointer to a buffer that receives the data that is read from the file. The size of the buffer must be greater than or equal to the number specified in the <i>SizeToRead</i> parameter.


### -param ReturnedSize [out]

Pointer to a ULONG variable that receives the number of bytes that were read from the backup store. If the call to <b>ReadBackupFile</b> is successful, this number is equal to the value that was specified in the <i>SizeToRead</i> parameter.


### -param Flags [in]

This parameter is reserved for future use.


## -returns



This method can return standard <b>HRESULT</b> values, such as <b>S_OK</b>. It can also return converted <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>  using the <a href="_com_hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Possible return values include the following.




## -see-also




<a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>



<a href="https://msdn.microsoft.com/0B7F5A5B-EB60-4BAF-86AF-D9101F3B482C">IDedupReadFileCallback</a>



<a href="https://msdn.microsoft.com/4ad4580d-c002-44a4-a5f6-757e83ed8732">ReadFile</a>
 

 

