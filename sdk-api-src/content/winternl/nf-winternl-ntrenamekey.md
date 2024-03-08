---
UID: NF:winternl.NtRenameKey
title: NtRenameKey function (winternl.h)
description: Changes the name of the specified registry key. (NtRenameKey)
helpviewer_keywords: ["NtRenameKey","NtRenameKey function [Windows API]","base.ntrenamekey","winprog.ntrenamekey","winternl/NtRenameKey"]
old-location: winprog\ntrenamekey.htm
tech.root: winprog
ms.assetid: fecd46f6-bcef-4cb4-8d53-3fb7ebe4cc53
ms.date: 12/05/2018
ms.keywords: NtRenameKey, NtRenameKey function [Windows API], base.ntrenamekey, winprog.ntrenamekey, winternl/NtRenameKey
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
req.lib: ntdll.lib
req.dll: ntdll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NtRenameKey
 - winternl/NtRenameKey
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ntdll.dll
api_name:
 - NtRenameKey
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

This function has no associated header file. You can also use the <a href="/windows/desktop/DevNotes/-loadlibrary">LoadLibrary</a> and <a href="/windows/desktop/DevNotes/-getprocaddress-">GetProcAddress</a> functions to dynamically link to Ntdll.dll.

The <b>NtRenameKey</b> function can be used to rename an entire registry subtree. The caller must have <b>KEY_CREATE_SUB_KEY</b> access to the parent of the specified key and DELETE access to the entire subtree being renamed.

## -see-also

<a href="/windows/desktop/SysInfo/registry-key-security-and-access-rights">Registry Key Security and Access Rights</a>
