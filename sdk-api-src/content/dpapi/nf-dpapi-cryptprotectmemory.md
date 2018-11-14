---
UID: NF:dpapi.CryptProtectMemory
title: CryptProtectMemory function
author: windows-sdk-content
description: encrypts memory to prevent others from viewing sensitive information in your process.
old-location: security\cryptprotectmemory.htm
tech.root: seccrypto
ms.assetid: 6b372552-87d4-4047-afa5-0d1113348289
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: CRYPTPROTECTMEMORY_CROSS_PROCESS, CRYPTPROTECTMEMORY_SAME_LOGON, CRYPTPROTECTMEMORY_SAME_PROCESS, CryptProtectMemory, CryptProtectMemory function [Security], dpapi/CryptProtectMemory, security.cryptprotectmemory, wincrypt/CryptProtectMemory
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CryptProtectMemory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- CryptProtectMemory
: 
---

# CryptProtectMemory function


## -description


The <b>CryptProtectMemory</b> function <a href="https://msdn.microsoft.com/f1caccd2-3453-448e-b194-bf899eff8091">encrypts</a> memory to prevent others from viewing sensitive information in your process. For example, use the <b>CryptProtectMemory</b> function to encrypt memory that contains a password. Encrypting the password prevents others from viewing it when the process is paged out to the swap file. Otherwise, the password is in <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">plaintext</a> and viewable by others.


## -parameters




### -param pDataIn [in, out]

A pointer to the block of memory to encrypt. The <i>cbData</i> parameter specifies the number of bytes that will be encrypted. If the data contained in the memory space is smaller than the number of bytes specified, data outside of the intended block will be encrypted. If it is larger than <i>cbData</i> bytes, then only the first <i>cbData</i> bytes will be encrypted.


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

If the function fails, it returns <b>FALSE</b>. For extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Using  <a href="seccpki.cryptprotectmemory">CryptProtectMemory</a> and <a href="seccpki.cryptunprotectmemory">CryptUnprotectMemory</a> for password encryption is not secure because the data exists as plaintext in memory before it is encrypted and at any time the caller decrypts it for use.

Typically, you use the <b>CryptProtectMemory</b> function to encrypt sensitive information that you are going to decrypt while your process is running.  Do not use this function to save data that you want to decrypt later; you will not be able to decrypt the data if the computer is restarted. To save encrypted data to a file to decrypt later, use the <a href="https://msdn.microsoft.com/765a68fd-f105-49fc-a738-4a8129eb0770">CryptProtectData</a> function.  

Call the <a href="https://msdn.microsoft.com/1c7980ac-4e9e-43fd-b6d7-c0d0a69c8040">CryptUnprotectMemory</a> function to decrypt memory encrypted with the <b>CryptProtectMemory</b> function.  When you have finished using the sensitive information, clear it from memory by calling the <a href="https://msdn.microsoft.com/2c4090a6-025b-4b7b-8f31-7e744ad51b39">SecureZeroMemory</a> function. 

Use the CRYPTPROTECTMEMORY_CROSS_PROCESS or CRYPTPROTECTMEMORY_SAME_LOGON flag if you use RPC or LRPC to pass encrypted data to another process. The receiving process must specify the same flag to decrypt the data. Also, use these flags if you use shared memory.

If the client uses the CRYPTPROTECTMEMORY_SAME_LOGON flag, the server must impersonate the client (<a href="https://msdn.microsoft.com/1b91c4dc-ac49-4002-b293-a25ca2ffcb21">RpcImpersonateClient</a>) before decrypting the memory. 


#### Examples

The following example calls  the <b>CryptProtectMemory</b> function to encrypt data that is in memory.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;windows.h&gt;
#include &lt;stdio.h&gt;
#include &lt;Wincrypt.h&gt;

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
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/765a68fd-f105-49fc-a738-4a8129eb0770">CryptProtectData</a>



<a href="https://msdn.microsoft.com/1c7980ac-4e9e-43fd-b6d7-c0d0a69c8040">CryptUnprotectMemory</a>



<a href="https://msdn.microsoft.com/8ecc5007-92ce-4e32-a093-dcb75ee8ba62">RtlDecryptMemory</a>



<a href="https://msdn.microsoft.com/b124a7fe-c62c-42f7-9d2b-cbf74d17186a">RtlEncryptMemory</a>
 

 

