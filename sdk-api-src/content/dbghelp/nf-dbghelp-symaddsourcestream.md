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

# SymAddSourceStream function


## -description


Adds the stream to the specified module for use by the <a href="https://msdn.microsoft.com/c7bf51ce-7fb4-49aa-ad33-e551b2c8362b">Source Server</a>.


## -parameters




### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a> function.


### -param Base [in]

The base address of the module.


### -param StreamFile [in, optional]

A null-terminated string that contains the absolute or relative path to a file that contains the source indexing stream. Can be <b>NULL</b> if <i>Buffer</i> is not <b>NULL</b>.


### -param Buffer [in, optional]

A buffer that contains the source indexing stream. Can be <b>NULL</b> if <i>StreamFile</i> is not <b>NULL</b>.


### -param Size [in]

Size, in bytes, of the <i>Buffer</i> buffer.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



<b>SymAddSourceStream</b> adds a stream of data formatted for use by the <a href="https://msdn.microsoft.com/c7bf51ce-7fb4-49aa-ad33-e551b2c8362b">source Server</a> to a designated module.  The caller can pass the stream either as a buffer in the <i>Buffer</i> parameter or a file in the <i>StreamFile</i> parameter.  If both parameters are filled, then the function uses the   <i>Buffer</i> parameter.  If both parameters are <b>NULL</b>, then the function returns <b>FALSE</b> and the <a href="https://msdn.microsoft.com/fd5b0d6e-78cf-4f51-b61d-d32576cd485a">last-error code</a> is set to <b>ERROR_INVALID_PARAMETER</b>.

It is important to note that <b>SymAddSourceStream</b> does not add the stream to any corresponding PDB in order to persist the data.  This function is used by those programmatically implementing their own debuggers in scenarios in which a PDB is not available.



