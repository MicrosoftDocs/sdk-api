---
UID: NF:ntsecapi.RtlEncryptMemory
title: RtlEncryptMemory function (ntsecapi.h)
description: Encrypts memory contents.
helpviewer_keywords: ["RTL_ENCRYPT_OPTION_CROSS_PROCESS","RTL_ENCRYPT_OPTION_SAME_LOGON","RtlEncryptMemory","RtlEncryptMemory function [Security]","ntsecapi/RtlEncryptMemory","security.rtlencryptmemory"]
old-location: security\rtlencryptmemory.htm
tech.root: security
ms.assetid: b124a7fe-c62c-42f7-9d2b-cbf74d17186a
ms.date: 01/08/2025
ms.keywords: RTL_ENCRYPT_OPTION_CROSS_PROCESS, RTL_ENCRYPT_OPTION_SAME_LOGON, RtlEncryptMemory, RtlEncryptMemory function [Security], ntsecapi/RtlEncryptMemory, security.rtlencryptmemory
req.header: ntsecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows Server 2003 [desktop apps only]
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
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RtlEncryptMemory
 - ntsecapi/RtlEncryptMemory
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
api_name:
 - RtlEncryptMemory
---

# RtlEncryptMemory function

## -description

<p class="CCE_Message">[The <a href="/windows/win32/api/ntsecapi/nf-ntsecapi-rtldecryptmemory">RtlDecryptMemory</a> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="/windows/win32/api/dpapi/nf-dpapi-cryptprotectmemory">CryptProtectMemory</a> function.]

The **RtlEncryptMemory** function encrypts memory contents. The encrypted contents can be decrypted by a subsequent call to the [RtlDecryptMemory](nf-ntsecapi-rtldecryptmemory.md) function.

> [!NOTE]
> This function has no associated import library. This function is available as a resource named **SystemFunction040** in `Advapi32.dll`. You must use the [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to `Advapi32.dll`.

## -parameters

### -param Memory [in, out]

A pointer to the memory to encrypt. The size of the memory must be a multiple of the **RTL_ENCRYPT_MEMORY_SIZE** constant.

### -param MemorySize [in]

Number of bytes to which *Memory* points. The number of bytes must be a multiple of the **RTL_ENCRYPT_MEMORY_SIZE** constant.

### -param OptionFlags [in]

Value that specifies how the encryption works over process boundaries and impersonation. This parameter can be one of the following values. The values are mutually exclusive. You must specify the same flag when encrypting and decrypting the memory.

| Value | Meaning |
|-------|---------|
| `0` | Encrypt and decrypt memory in the same process. An application running in a different process will not be able to decrypt the data. |
| **RTL_ENCRYPT_OPTION_CROSS_PROCESS**<br/>`0x01` | Encrypt and decrypt memory in different processes. An application running in a different process will be able to decrypt the data. |
| **RTL_ENCRYPT_OPTION_SAME_LOGON**<br/>`0x02` | Use the same logon credentials to encrypt and decrypt memory in different processes. An application running in a different process will be able to decrypt the data. However, the process must run as the same user that encrypted the data and in the same logon session. |
| **RTL_ENCRYPT_OPTION_FOR_SYSTEM**<br/>`0x04` | Allow callers to encrypt information to be decrypted only by a system process. |

## -returns

If the function is successful, the return value is **STATUS_SUCCESS**.

If the function fails, the return value is an **NTSTATUS** code that indicates the error.
