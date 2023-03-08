---
UID: NF:dpapi.CryptUnprotectData
title: CryptUnprotectData function (dpapi.h)
description: Decrypts and does an integrity check of the data in a DATA_BLOB structure.
helpviewer_keywords: ["CRYPTPROTECT_UI_FORBIDDEN","CRYPTPROTECT_VERIFY_PROTECTION","CryptUnprotectData","CryptUnprotectData function [Security]","_crypto2_cryptunprotectdata","dpapi/CryptUnprotectData","security.cryptunprotectdata","wincrypt/CryptUnprotectData"]
old-location: security\cryptunprotectdata.htm
tech.root: security
ms.assetid: 54eab3b0-d341-47c6-9c32-79328d7a7155
ms.date: 12/05/2018
ms.keywords: CRYPTPROTECT_UI_FORBIDDEN, CRYPTPROTECT_VERIFY_PROTECTION, CryptUnprotectData, CryptUnprotectData function [Security], _crypto2_cryptunprotectdata, dpapi/CryptUnprotectData, security.cryptunprotectdata, wincrypt/CryptUnprotectData
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
 - CryptUnprotectData
 - dpapi/CryptUnprotectData
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
 - CryptUnprotectData
---

# CryptUnprotectData function


## -description

The <b>CryptUnprotectData</b> function decrypts and does an <a href="/windows/desktop/SecGloss/i-gly">integrity</a> check of the data in a 
<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">DATA_BLOB</a> structure. Usually, the only user who can decrypt the data is a user with the same logon <a href="/windows/desktop/SecGloss/c-gly">credentials</a> as the user who encrypted the data. In addition, the encryption and decryption must be done on the same computer. For information about exceptions, see the Remarks section of 
<a href="/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata">CryptProtectData</a>.

## -parameters

### -param pDataIn [in]

A pointer to a 
<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">DATA_BLOB</a> structure that holds the encrypted data. The <b>DATA_BLOB</b> structure's <b>cbData</b> member holds the length of the <b>pbData</b> member's byte string that contains the text to be encrypted.

### -param ppszDataDescr [out, optional]

A pointer to a string-readable description of the encrypted data included with the encrypted data. This parameter can be set to <b>NULL</b>.  When you have finished using <i>ppszDataDescr</i>, free it by calling the  <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> function.

### -param pOptionalEntropy [in, optional]

A pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">DATA_BLOB</a> structure that contains a password or other additional entropy used when the data was encrypted. This parameter can be set to <b>NULL</b>; however, if an optional entropy <b>DATA_BLOB</b> structure was used in the encryption phase, that same <b>DATA_BLOB</b> structure must be used for the decryption phase. For information about protecting passwords, see <a href="/windows/desktop/SecBP/handling-passwords">Handling Passwords</a>.

### -param pvReserved

This parameter is reserved for future use and must be set to <b>NULL</b>.

### -param pPromptStruct [in, optional]

A pointer to a 
<a href="/windows/desktop/api/dpapi/ns-dpapi-cryptprotect_promptstruct">CRYPTPROTECT_PROMPTSTRUCT</a> structure that provides information about where and when prompts are to be displayed and what the content of those prompts should be. This parameter can be set to <b>NULL</b>.

### -param dwFlags [in]

A <b>DWORD</b> value that specifies options for this function. This parameter can be zero, in which case no option is set, or the following flag.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPTPROTECT_UI_FORBIDDEN"></a><a id="cryptprotect_ui_forbidden"></a><dl>
<dt><b>CRYPTPROTECT_UI_FORBIDDEN</b></dt>
</dl>
</td>
<td width="60%">
This flag is used for remote situations where the user interface (UI) is not an option. When this flag is set and UI is specified for either the protect or unprotect operation, the operation fails and 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns the ERROR_PASSWORD_RESTRICTION code.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTPROTECT_VERIFY_PROTECTION"></a><a id="cryptprotect_verify_protection"></a><dl>
<dt><b>CRYPTPROTECT_VERIFY_PROTECTION</b></dt>
</dl>
</td>
<td width="60%">
This flag verifies the protection of a protected <a href="/windows/desktop/SecGloss/b-gly">BLOB</a>. If the default protection level configured of the host is higher than the current protection level for the BLOB, the function returns <b>CRYPT_I_NEW_PROTECTION_REQUIRED</b> to advise the caller to again protect the plaintext contained in the BLOB.

</td>
</tr>
</table>

### -param pDataOut [out]

A pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">DATA_BLOB</a> structure where the function stores the decrypted data. When you have finished using the <b>DATA_BLOB</b> structure, free its <b>pbData</b> member by calling the  <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> function.

## -returns

If the function succeeds, the function returns  <b>TRUE</b>.

If the function fails, it returns  <b>FALSE</b>.

## -remarks

The 
<a href="/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata">CryptProtectData</a> function creates a session key when the data is encrypted. That key is derived again and used to decrypt the data <a href="/windows/desktop/SecGloss/b-gly">BLOB</a>.

The <a href="/windows/desktop/SecGloss/m-gly">Message Authentication Code</a> (MAC) <a href="/windows/desktop/SecGloss/h-gly">hash</a> added to the encrypted data can be used to determine whether the encrypted data was altered in any way. Any tampering results in the return of the ERROR_INVALID_DATA code.

When you have finished using the <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">DATA_BLOB</a> structure, free its <b>pbData</b> member by calling the  <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> function. Any <i>ppszDataDescr</i> that is not <b>NULL</b> must also be freed by using <b>LocalFree</b>.

 When you have finished using sensitive information, clear it from memory by calling the <a href="/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)">SecureZeroMemory</a> function.  


#### Examples

The following example shows decrypting encrypted data in a 
<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">DATA_BLOB</a> structure. This function does the decryption by using a session key that the function creates by using the user's logon credentials. For another example that uses this function, see 
<a href="/windows/desktop/SecCrypto/example-c-program-using-cryptprotectdata">Example C Program: Using CryptProtectData</a>.


```cpp
// Decrypt data from DATA_BLOB DataOut to DATA_BLOB DataVerify.

//--------------------------------------------------------------------
// Declare and initialize variables.

DATA_BLOB DataOut;
DATA_BLOB DataVerify;
LPWSTR pDescrOut =  NULL;
//--------------------------------------------------------------------
// The buffer DataOut would be created using the CryptProtectData
// function. If may have been read in from a file.

//--------------------------------------------------------------------
//   Begin unprotect phase.

if (CryptUnprotectData(
        &DataOut,
        &pDescrOut,
        NULL,                 // Optional entropy
        NULL,                 // Reserved
        NULL,                 // Here, the optional 
                              // prompt structure is not
                              // used.
        0,
        &DataVerify))
{
     printf("The decrypted data is: %s\n", DataVerify.pbData);
     printf("The description of the data was: %s\n",pDescrOut);
     LocalFree(DataVerify.pbData);
     LocalFree(pDescrOut);
}
else
{
    printf("Decryption error!");
}

```

## -see-also

<a href="/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata">CryptProtectData</a>



<a href="/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectmemory">CryptUnprotectMemory</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Data Encryption and Decryption Functions</a>



<a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a>



<a href="/windows/desktop/SecCrypto/microsoft-base-cryptographic-provider">Microsoft Base Cryptographic Provider</a>