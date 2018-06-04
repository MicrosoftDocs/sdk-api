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

# SHOpenRegStreamA function


## -description


Deprecated. Opens a registry value and supplies a stream that can be used to read from or write to the value.

            
<div class="alert"><b>Note</b>  This function has been replaced by <a href="https://msdn.microsoft.com/2450dde0-cd02-4d48-be40-467b4b8be240">SHOpenRegStream2</a>. It is recommended that you use <b>SHOpenRegStream2</b> at all times.</div><div> </div>

## -parameters




### -param hkey [in]

Type: <b>HKEY</b>

Required. The subtree, such as HKEY_LOCAL_MACHINE, that contains the value.


### -param pszSubkey [in, optional]

Type: <b>LPCTSTR</b>

Optional. Pointer to a null-terminated string that specifies the subkey that contains the value. This value can be <b>NULL</b>.


### -param pszValue [in, optional]

Type: <b>LPCTSTR</b>

Pointer to a null-terminated string that specifies the value to be accessed. This value can be <b>NULL</b>.


### -param grfMode [in]

Type: <b>DWORD</b>

The type of access for the stream. This can be one of the following values:



#### STGM_READ

Open the stream for reading.



#### STGM_WRITE

Open the stream for writing.



#### STGM_READWRITE

Open the stream for both reading and writing.


## -returns



Type: <b><a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>*</b>

Returns an <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> interface pointer if successful; otherwise, <b>NULL</b>. A <b>NULL</b> value can be caused by several situations, including an invalid <i>hkey</i> or <i>pszSubkey</i>, or an inability to open the stream. 

                    

<div class="alert"><b>Note</b>  In some situations, such as when the subkey named by <i>pszSubkey</i> does not exist or the caller does not have sufficient permissions to access the subkey, a zero-length stream is returned rather than a <b>NULL</b> value. <a href="https://msdn.microsoft.com/2450dde0-cd02-4d48-be40-467b4b8be240">SHOpenRegStream2</a> returns <b>NULL</b> in all error situations and is the preferred function for that reason.</div>
<div> </div>



## -remarks



The calling application is responsible for calling the <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> method of the returned object when that <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> object is no longer needed.



