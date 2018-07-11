---
UID: NF:wincrypt.CryptGetDefaultProviderW
title: CryptGetDefaultProviderW function
author: windows-sdk-content
description: Finds the default cryptographic service provider (CSP) of a specified provider type for the local computer or current user.
old-location: security\cryptgetdefaultprovider.htm
old-project: seccrypto
ms.assetid: 5d15641e-1ad7-441d-9423-65fd51de9812
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: CRYPT_MACHINE_DEFAULT, CRYPT_USER_DEFAULT, CryptGetDefaultProvider, CryptGetDefaultProvider function [Security], CryptGetDefaultProviderA, CryptGetDefaultProviderW, _crypto2_cryptgetdefaultprovider, security.cryptgetdefaultprovider, wincrypt/CryptGetDefaultProvider, wincrypt/CryptGetDefaultProviderA, wincrypt/CryptGetDefaultProviderW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CryptGetDefaultProviderW (Unicode) and CryptGetDefaultProviderA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: USERNAME_TARGET_CREDENTIAL_INFO, *PUSERNAME_TARGET_CREDENTIAL_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-Security-cryptoapi-l1-1-0.dll
 - cryptsp.dll
api_name:
 - CryptGetDefaultProvider
 - CryptGetDefaultProviderA
 - CryptGetDefaultProviderW
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CryptGetDefaultProviderW function


## -description


<div class="alert"><b>Important</b>  This API is deprecated. New and existing software should start using <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/aa376210%28v=vs.85%29.aspx">Cryptography Next Generation APIs.</a> Microsoft may remove this API in future releases.</div><div> </div>
			The <b>CryptGetDefaultProvider</b> function finds the default <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP) of a specified provider type for the local computer or current user. The name of the default CSP for the provider type specified in the <i>dwProvType</i> parameter is returned in the <i>pszProvName</i> buffer.


## -parameters




### -param dwProvType [in]

The provider type for which the default CSP name is to be found. 

Defined provider types are  as follows:

<ul>
<li>
<a href="https://msdn.microsoft.com/44b13a96-aba2-4b77-8e66-416aa0bcb8ad">PROV_RSA_FULL</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ebb6192b-f34e-4218-a1e8-308708ae5935">PROV_RSA_SIG</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b3b00f10-8f94-4c30-8267-db0c449e4d15">PROV_DSS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/2ad176e9-30c6-411a-b3ed-bc6656c96768">PROV_DSS_DH</a>
</li>
<li>
<a href="https://msdn.microsoft.com/56291983-995f-4b77-82ce-b165cfff6939">PROV_DH_SCHANNEL</a>
</li>
<li>
<a href="https://msdn.microsoft.com/220cb6f5-28a6-4ea8-b7ed-3a9f77752b7d">PROV_FORTEZZA</a>
</li>
<li>
<a href="https://msdn.microsoft.com/40b28dee-85b6-431c-834f-b1e5b3242d4b">PROV_MS_EXCHANGE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/f0c11a04-7931-424a-b085-0cc584ea7bb7">PROV_RSA_SCHANNEL</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c94d8584-f01b-469b-a0d6-5fb14796b93e">PROV_SSL</a>
</li>
</ul>

### -param pdwReserved [in]

This parameter is reserved for future use and must be <b>NULL</b>.


### -param dwFlags [in]

The following flag values are defined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_USER_DEFAULT"></a><a id="crypt_user_default"></a><dl>
<dt><b>CRYPT_USER_DEFAULT</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Returns the user-context default CSP of the specified type.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_MACHINE_DEFAULT"></a><a id="crypt_machine_default"></a><dl>
<dt><b>CRYPT_MACHINE_DEFAULT</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Returns the computer default CSP of the specified type.

</td>
</tr>
</table>
 


### -param pszProvName [out]

A pointer to a null-terminated character string buffer to receive the name of the default CSP.

To find the size of the buffer for memory allocation purposes, this parameter can be <b>NULL</b>. For more information, see 
<a href="https://msdn.microsoft.com/ef99edef-39b2-4d78-9c01-13720215d47f">Retrieving Data of Unknown Length</a>.


### -param pcbProvName [in, out]

A pointer to a <b>DWORD</b> value that specifies the size, in bytes, of the buffer pointed to by the <i>pszProvName</i> parameter. When the function returns, the <b>DWORD</b> value contains the number of bytes stored or to be stored in the buffer.

<div class="alert"><b>Note</b>  When processing the data returned in the buffer, applications must use the actual size of the data returned. The actual size can be slightly smaller than the size of the buffer specified on input. (On input, buffer sizes are usually specified large enough to ensure that the largest possible output data fits in the buffer.) On output, the variable pointed to by this parameter is updated to reflect the actual size of the data copied to the buffer.</div>
<div> </div>

## -returns




						If the function succeeds, the return value is nonzero (<b>TRUE</b>).
						

If the function fails, the return value is zero (<b>FALSE</b>). For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

The error code prefaced by NTE is generated by the particular CSP being used. Possible error codes include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters contains a value that is not valid. This is most often a pointer that is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The buffer for the name is not large enough.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
The operating system ran out of memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_FLAGS</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwFlags</i> parameter has an unrecognized value.

</td>
</tr>
</table>
 




## -remarks



This function determines which installed CSP is currently set as the default for the local computer or current user. This information is often displayed to the user.


#### Examples

The following example retrieves the name of the default CSP for the PROV_RSA_FULL provider type. For another example that uses this function, see <a href="https://msdn.microsoft.com/10a5210d-7992-4832-9435-67ac2b851a97">Example C Program: Enumerating CSP Providers and Provider Types</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;stdio.h&gt;
#include &lt;windows.h&gt;
#include &lt;Wincrypt.h&gt;
#pragma comment(lib, "crypt32.lib")

void main()
{

    DWORD       cbProvName=0;
    LPTSTR      pbProvName=NULL;
    // Copyright (C) Microsoft.  All rights reserved.
    // Get the length of the RSA_FULL default provider name.
    if (!(CryptGetDefaultProvider(
         PROV_RSA_FULL, 
         NULL, 
         CRYPT_MACHINE_DEFAULT,
         NULL, 
         &amp;cbProvName))) 
    { 
      printf("Error getting the length of the default "
          "provider name.\n");
      exit(1);
    }

    // Allocate local memory for the name of the default provider.
    if (!(pbProvName = (LPTSTR)LocalAlloc(LMEM_ZEROINIT, 
        cbProvName)))
    {
        printf("Error during memory allocation for "
            "provider name.\n");
        exit(1);
    }

    // Get the default provider name.
    if (CryptGetDefaultProvider(
        PROV_RSA_FULL, 
        NULL, 
        CRYPT_MACHINE_DEFAULT,
        pbProvName,
        &amp;cbProvName)) 
    {
        printf("The default provider name is %s\n",pbProvName);
    }
    else
    {
        printf("Getting the name of the provider failed.\n");
        exit(1);
    }

    // Free resources when done.
    LocalFree(pbProvName);

}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/44023a0c-3fb4-4746-a676-1671c3ad901b">CryptSetProvider</a>



<a href="https://msdn.microsoft.com/5f0c2724-5144-4a22-a7da-2a5162f06f5d">CryptSetProviderEx</a>



<a href="cryptography_functions.htm">Service Provider Functions</a>
 

 

