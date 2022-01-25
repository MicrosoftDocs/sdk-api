---
UID: NF:dpapi.CryptProtectMemory
title: CryptProtectMemory function (dpapi.h)
description: encrypts memory to prevent others from viewing sensitive information in your process.
helpviewer_keywords: ["CRYPTPROTECTMEMORY_CROSS_PROCESS","CRYPTPROTECTMEMORY_SAME_LOGON","CRYPTPROTECTMEMORY_SAME_PROCESS","CryptProtectMemory","CryptProtectMemory function [Security]","dpapi/CryptProtectMemory","security.cryptprotectmemory","wincrypt/CryptProtectMemory"]
old-location: security\cryptprotectmemory.htm
tech.root: security
ms.assetid: 6b372552-87d4-4047-afa5-0d1113348289
ms.date: 12/05/2018
ms.keywords: CRYPTPROTECTMEMORY_CROSS_PROCESS, CRYPTPROTECTMEMORY_SAME_LOGON, CRYPTPROTECTMEMORY_SAME_PROCESS, CryptProtectMemory, CryptProtectMemory function [Security], dpapi/CryptProtectMemory, security.cryptprotectmemory, wincrypt/CryptProtectMemory
req.header: dpapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
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
 - CryptProtectMemory
 - dpapi/CryptProtectMemory
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
 - CryptProtectMemory
---

# CryptProtectMemory function


## -description

The <b>CryptProtectMemory</b> function <a href="/windows/desktop/SecGloss/e-gly">encrypts</a> memory to prevent others from viewing sensitive information in your process. For example, use the <b>CryptProtectMemory</b> function to encrypt memory that contains a password. Encrypting the password prevents others from viewing it when the process is paged out to the swap file. Otherwise, the password is in <a href="/windows/desktop/SecGloss/p-gly">plaintext</a> and viewable by others.

## -parameters

### -param pDataIn [in, out]

A pointer to the block of memory to encrypt. The <i>cbDataIn</i> parameter specifies the number of bytes that will be encrypted. If the data contained in the memory space is smaller than the number of bytes specified, data outside of the intended block will be encrypted. If it is larger than <i>cbDataIn</i> bytes, then only the first <i>cbDataIn</i> bytes will be encrypted.

### -param cbDataIn [in]

Number of bytes of memory pointed to by the <i>pData</i> parameter to encrypt. The number of bytes must be a multiple of the <b>CRYPTPROTECTMEMORY_BLOCK_SIZE</b> constant defined in Wincrypt.h.

### -param dwFlags [in]

This parameter can be one of the following flags. You must specify the same flag when encrypting and decrypting the memory.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPTPROTECTMEMORY_SAME_PROCESS"></a><a id="cryptprotectmemory_same_process"></a><dl>
<dt><b>CRYPTPROTECTMEMORY_SAME_PROCESS</b></dt>
</dl>
</td>
<td width="60%">
Encrypt and decrypt memory in the same process. An application running in a different process will not be able to decrypt the data.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTPROTECTMEMORY_CROSS_PROCESS"></a><a id="cryptprotectmemory_cross_process"></a><dl>
<dt><b>CRYPTPROTECTMEMORY_CROSS_PROCESS</b></dt>
</dl>
</td>
<td width="60%">
Encrypt and decrypt memory in different processes. An application running in a different process will be able to decrypt the data.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTPROTECTMEMORY_SAME_LOGON"></a><a id="cryptprotectmemory_same_logon"></a><dl>
<dt><b>CRYPTPROTECTMEMORY_SAME_LOGON</b></dt>
</dl>
</td>
<td width="60%">
Use the same logon credentials to encrypt and decrypt memory in different processes. An application running in a different process will be able to decrypt the data. However, the process must run as the same user that encrypted the data and in the same logon session. 

</td>
</tr>
</table>

## -returns

If the function succeeds, the function returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. For extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Using  <a href="/windows/desktop/api/dpapi/nf-dpapi-cryptprotectmemory">CryptProtectMemory</a> and <a href="/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectmemory">CryptUnprotectMemory</a> for password encryption is not secure because the data exists as plaintext in memory before it is encrypted and at any time the caller decrypts it for use.

Typically, you use the <b>CryptProtectMemory</b> function to encrypt sensitive information that you are going to decrypt while your process is running.  Do not use this function to save data that you want to decrypt later; you will not be able to decrypt the data if the computer is restarted. To save encrypted data to a file to decrypt later, use the <a href="/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata">CryptProtectData</a> function.  

Call the <a href="/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectmemory">CryptUnprotectMemory</a> function to decrypt memory encrypted with the <b>CryptProtectMemory</b> function.  When you have finished using the sensitive information, clear it from memory by calling the <a href="/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)">SecureZeroMemory</a> function. 

Use the CRYPTPROTECTMEMORY_CROSS_PROCESS or CRYPTPROTECTMEMORY_SAME_LOGON flag if you use RPC or LRPC to pass encrypted data to another process. The receiving process must specify the same flag to decrypt the data. Also, use these flags if you use shared memory.

If the client uses the CRYPTPROTECTMEMORY_SAME_LOGON flag, the server must impersonate the client (<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcimpersonateclient">RpcImpersonateClient</a>) before decrypting the memory. 


#### Examples

The following example calls  the <b>CryptProtectMemory</b> function to encrypt data that is in memory.


```cpp
#include <windows.h>
#include <stdio.h>
#include <Wincrypt.h>

#define SSN_STR_LEN 12  // includes null

void main()
{
    HRESULT hr = S_OK;
    LPWSTR pSensitiveText = NULL;
    DWORD cbSensitiveText = 0;
    DWORD cbPlainText = SSN_STR_LEN*sizeof(WCHAR);
    DWORD dwMod = 0;

    //  Memory to encrypt must be a multiple of CRYPTPROTECTMEMORY_BLOCK_SIZE.
    if (dwMod = cbPlainText % CRYPTPROTECTMEMORY_BLOCK_SIZE)
        cbSensitiveText = cbPlainText +
		(CRYPTPROTECTMEMORY_BLOCK_SIZE - dwMod);
    else
        cbSensitiveText = cbPlainText;

    pSensitiveText = (LPWSTR)LocalAlloc(LPTR, cbSensitiveText);
    if (NULL == pSensitiveText)
    {
        wprintf(L"Memory allocation failed.\n");
        return E_OUTOFMEMORY;
    }

    //  Place sensitive string to encrypt in pSensitiveText.

    if (!CryptProtectMemory(pSensitiveText, cbSensitiveText,
		CRYPTPROTECTMEMORY_SAME_PROCESS))
    {
        wprintf(L"CryptProtectMemory failed: %d\n", GetLastError());
        SecureZeroMemory(pSensitiveText, cbSensitiveText);
        LocalFree(pSensitiveText);
        pSensitiveText = NULL;
        return E_FAIL;
    }

    //  Call CryptUnprotectMemory to decrypt and use the memory.

    SecureZeroMemory(pSensitiveText, cbSensitiveText);
    LocalFree(pSensitiveText);
    pSensitiveText = NULL;

    return hr;
}
```

## -see-also

<a href="/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata">CryptProtectData</a>



<a href="/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectmemory">CryptUnprotectMemory</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-rtldecryptmemory">RtlDecryptMemory</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-rtlencryptmemory">RtlEncryptMemory</a>
