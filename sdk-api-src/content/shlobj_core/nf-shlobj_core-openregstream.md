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

# OpenRegStream function


## -description


<p class="CCE_Message">[<b>OpenRegStream</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/2450dde0-cd02-4d48-be40-467b4b8be240">SHOpenRegStream2</a> or <a href="https://msdn.microsoft.com/2f839b89-8584-4b4d-91e7-166b6e2b6892">SHOpenRegStream</a>.]

Opens a registry value and supplies an <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> interface that can be used to read from or write to the value.


## -parameters




### -param hkey [in]

Type: <b>HKEY</b>

A handle to the key that is currently open.


### -param pszSubkey [in, optional]

Type: <b>PCWSTR</b>

A null-terminated Unicode string that specifies the name of the subkey.


### -param pszValue [in, optional]

Type: <b>PCWSTR</b>

A null-terminated Unicode string that specifies the value to be accessed.


### -param grfMode

Type: <b>DWORD</b>

The type of access for the stream. This can be one of the following values.



#### STGM_READ

Open the stream for reading.



#### STGM_WRITE

Open the stream for writing.



#### STGM_READWRITE

Open the stream for reading and writing.


## -returns



Type: <b><a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>*</b>

Returns the address of an <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> interface if successful, or <b>NULL</b> otherwise.



