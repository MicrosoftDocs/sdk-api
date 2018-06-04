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

# NtRenameKey function


## -description


<p class="CCE_Message">[This function may be changed or removed from Windows without further notice. ]

Changes the name of the specified registry key.


## -parameters




### -param KeyHandle [in]

A handle to the key to be renamed. The handle must be opened with the KEY_WRITE access right.


### -param NewName [in]

A pointer to a UNICODE string that is the new name for the key.


## -returns



Returns an <b>NTSTATUS</b> or error code. An error code of <b>STATUS_ACCESS_DENIED</b> indicates that the caller does not have the necessary access rights to the specified registry key or subkeys.

The forms and significance of <b>NTSTATUS</b> error codes are listed in the Ntstatus.h header file available in the WDK, and are described in the WDK documentation.




## -remarks



This function has no associated header file. The associated import library, Ntdll.lib, is available in the WDK. You can also use the <a href="https://msdn.microsoft.com/191fcbd8-4542-4cad-955e-6951f3005fc5">LoadLibrary</a> and <a href="https://msdn.microsoft.com/e425948c-5588-4a4f-994c-4e608af18439">GetProcAddress</a> functions to dynamically link to Ntdll.dll.

The <b>NtRenameKey</b> function can be used to rename an entire registry subtree. The caller must have <b>KEY_CREATE_SUB_KEY</b> access to the parent of the specified key and DELETE access to the entire subtree being renamed. 




## -see-also




<a href="https://msdn.microsoft.com/266d5c8e-1bcd-48e5-bc06-2fbc956d8658">Registry Key Security and Access Rights</a>
 

 

