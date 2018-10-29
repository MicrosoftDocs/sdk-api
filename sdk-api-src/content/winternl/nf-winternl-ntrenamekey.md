---
UID: NF:winternl.NtRenameKey
title: NtRenameKey function
author: windows-sdk-content
description: Changes the name of the specified registry key.
old-location: winprog\ntrenamekey.htm
tech.root: DevNotes
ms.assetid: fecd46f6-bcef-4cb4-8d53-3fb7ebe4cc53
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: NtRenameKey, NtRenameKey function [Windows API], base.ntrenamekey, winprog.ntrenamekey, winternl/NtRenameKey
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winternl.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: Ntdll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ntdll.dll
api_name:
 - NtRenameKey
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

