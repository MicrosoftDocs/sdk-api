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

# SfcGetNextProtectedFile function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems specified in the Requirements section. Support for this function was removed in Windows Vista and Windows Server 2008. Use the supported functions listed in <a href="https://msdn.microsoft.com/6806c320-6071-4075-9003-2469089a9cc4">WRP Functions</a> instead.]

Retrieves the complete list of protected files. Applications should not replace these files.


## -parameters




### -param RpcHandle [in]

This parameter must be <b>NULL</b>.


### -param ProtFileData [in, out]

The list of protected files. The format of this structure is as follows. 




<pre class="syntax" xml:space="preserve"><code>typedef struct _PROTECTED_FILE_DATA {
    WCHAR   FileName[MAX_PATH];
    DWORD   FileNumber;
} PROTECTED_FILE_DATA, *PPROTECTED_FILE_DATA;</code></pre>
Before calling this function the first time, set the <b>FileNumber</b> member to zero.


## -returns



If the function succeeds, the return value is nonzero.

If there are no more protected files to enumerate, the return value is zero and 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns ERROR_NO_MORE_FILES. If the function fails, <b>GetLastError</b> will return a different error code.




## -see-also




<a href="https://msdn.microsoft.com/6882f7ef-0265-4db5-afa5-54df35b9dba1">SfcIsFileProtected</a>
 

 

