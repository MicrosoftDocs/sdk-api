---
UID: NF:dpapi.CryptProtectData
title: CryptProtectData function (dpapi.h)
description: Performs encryption on the data in a DATA_BLOB structure.
helpviewer_keywords: ["CRYPTPROTECT_AUDIT","CRYPTPROTECT_LOCAL_MACHINE","CRYPTPROTECT_UI_FORBIDDEN","CryptProtectData","CryptProtectData function [Security]","_crypto2_cryptprotectdata","dpapi/CryptProtectData","security.cryptprotectdata","wincrypt/CryptProtectData"]
old-location: security\cryptprotectdata.htm
tech.root: security
ms.assetid: 765a68fd-f105-49fc-a738-4a8129eb0770
ms.date: 11/13/2025
ms.keywords: CRYPTPROTECT_AUDIT, CRYPTPROTECT_LOCAL_MACHINE, CRYPTPROTECT_UI_FORBIDDEN, CryptProtectData, CryptProtectData function [Security], _crypto2_cryptprotectdata, dpapi/CryptProtectData, security.cryptprotectdata, wincrypt/CryptProtectData
req.header: dpapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CryptProtectData
 - dpapi/CryptProtectData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CryptProtectData
---

# CryptProtectData function

## -description

The **CryptProtectData** function performs encryption on the data in a [DATA_BLOB](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) structure. Typically, only a user with the same logon credential as the user who encrypted the data can decrypt the data. In addition, the encryption and decryption usually must be done on the same computer. For information about exceptions, see [Remarks](#remarks).

## -parameters

### -param pDataIn [in]

A pointer to a [DATA_BLOB](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) structure that contains the [plaintext](/windows/win32/SecGloss/p-gly) to be encrypted.

### -param szDataDescr [in, optional]

A string with a readable description of the data to be encrypted. This description string is included with the encrypted data. This parameter is optional and can be set to **NULL**.

### -param pOptionalEntropy [in, optional]

A pointer to a [DATA_BLOB](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) structure that contains a password or other additional entropy used to encrypt the data. The **DATA_BLOB** structure used in the encryption phase must also be used in the decryption phase. This parameter can be set to **NULL** for no additional entropy. For information about protecting passwords, see [Handling Passwords](/windows/win32/SecBP/handling-passwords).

### -param pvReserved [in]

Reserved for future use and must be set to **NULL**.

### -param pPromptStruct [in, optional]

A pointer to a [CRYPTPROTECT_PROMPTSTRUCT](nf-dpapi-cryptprotect_promptstruct.md) structure that provides information about where and when prompts are to be displayed and what the content of those prompts should be. This parameter can be set to **NULL** in both the encryption and decryption phases.

### -param dwFlags [in]

This parameter can be one of the following flags. If no flags are required, this parameter can be set to `0`.

| Value | Meaning |
|-------|---------|
| **CRYPTPROTECT_LOCAL_MACHINE** | When this flag is set, it associates the data encrypted with the current computer instead of with an individual user. Any user on the computer on which **CryptProtectData** is called can use [CryptUnprotectData](nf-dpapi-cryptunprotectdata.md) to decrypt the data. |
| **CRYPTPROTECT_UI_FORBIDDEN** | This flag is used for remote situations where presenting a user interface (UI) is not an option. When this flag is set and a UI is specified for either the protect or unprotect operation, the operation fails and [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the **ERROR_PASSWORD_RESTRICTION** code. |
| **CRYPTPROTECT_AUDIT** | This flag generates an audit on protect and unprotect operations. Audit log entries are recorded only if szDataDescr is not **NULL** and not empty. |

### -param pDataOut [out]

A pointer to a [DATA_BLOB](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) structure that receives the encrypted data. When you have finished using the **DATA_BLOB** structure, free its **pbData** member by calling the [LocalFree](/windows/win32/api/winbase/nf-winbase-localfree) function.

## -returns

If the function succeeds, the function returns **TRUE**.
						

If the function fails, it returns **FALSE**. For extended error information, call [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## -remarks

Typically, only a user with logon [credentials](/windows/win32/SecGloss/c-gly) that match those of the user who encrypted the data can decrypt the data. In addition, decryption usually can only be done on the computer where the data was encrypted. However, a user with a roaming profile can decrypt the data from another computer on the network.

If the **CRYPTPROTECT_LOCAL_MACHINE** flag is set when the data is encrypted, any user on the computer where the encryption was done can decrypt the data.

The function creates a session key to perform the encryption. The session key is derived again when the data is to be decrypted.

The function also adds a [Message Authentication Code](/windows/win32/SecGloss/m-gly) (MAC) (keyed integrity check) to the encrypted data to guard against data tampering.

To encrypt memory for temporary use in the same process or across processes, call the [CryptProtectMemory](nf-dpapi-cryptprotectmemory.md) function.

### Examples

The following example shows encryption of the data in a [DATA_BLOB](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) structure. The **CryptProtectData** function does the encryption by using a session key that the function creates by using the user's logon credentials. For another example that uses this function, see [Example C Program: Using CryptProtectData](/windows/win32/SecCrypto/example-c-program-using-cryptprotectdata).


```cpp
// Encrypt data from DATA_BLOB DataIn to DATA_BLOB DataOut.

//--------------------------------------------------------------------
// Declare and initialize variables.

DATA_BLOB DataIn;
DATA_BLOB DataOut;
BYTE *pbDataInput =(BYTE *)"Hello world of data protection.";
DWORD cbDataInput = strlen((char *)pbDataInput)+1;

//--------------------------------------------------------------------
// Initialize the DataIn structure.

DataIn.pbData = pbDataInput;    
DataIn.cbData = cbDataInput;

//--------------------------------------------------------------------
//  Begin protect phase. Note that the encryption key is created
//  by the function and is not passed.

if(CryptProtectData(
     &DataIn,
     L"This is the description string.", // A description string
                                         // to be included with the
                                         // encrypted data. 
     NULL,                               // Optional entropy not used.
     NULL,                               // Reserved.
     NULL,                               // Pass NULL for the 
                                         // prompt structure.
     0,
     &DataOut))
{
     printf("The encryption phase worked.\n");
     LocalFree(DataOut.pbData);
}
else
{
    printf("Encryption error using CryptProtectData.\n");
    exit(1); 
}
```

## -see-also

- [CryptProtectMemory](nf-dpapi-cryptprotectmemory.md)
- [CryptUnprotectData](nf-dpapi-cryptunprotectdata.md)
- [Data Encryption and Decryption Functions](/windows/win32/SecCrypto/cryptography-functions)
- [LocalFree](/windows/win32/api/winbase/nf-winbase-localfree)