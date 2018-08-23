---
UID: NF:wincrypt.CryptContextAddRef
title: CryptContextAddRef function
author: windows-sdk-content
description: Adds one to the reference count of an HCRYPTPROV cryptographic service provider (CSP) handle.
old-location: security\cryptcontextaddref.htm
old-project: SecCrypto
ms.assetid: 074666a7-369c-43bc-97d9-3bcc9703976b
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: CryptContextAddRef, CryptContextAddRef function [Security], _crypto2_cryptcontextaddref, security.cryptcontextaddref, wincrypt/CryptContextAddRef
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wincrypt.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
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
 - CryptContextAddRef
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CryptContextAddRef function


## -description


<div class="alert"><b>Important</b>  This API is deprecated. New and existing software should start using <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/aa376210%28v=vs.85%29.aspx">Cryptography Next Generation APIs.</a> Microsoft may remove this API in future releases.</div><div> </div>The <b>CryptContextAddRef</b> function adds one to the <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">reference count</a> of an 
<a href="https://msdn.microsoft.com/8ec6b392-06bc-4717-8657-7ea9a43d03fb">HCRYPTPROV</a> <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP) handle. This function should be used if the CSP handle is included as a member of any structure passed to another function. The 
<a href="https://msdn.microsoft.com/c1e3e708-b543-4e87-8638-a9946a83e614">CryptReleaseContext</a> function should be called when the CSP handle is no longer needed.


## -parameters




### -param hProv [in]


<a href="https://msdn.microsoft.com/8ec6b392-06bc-4717-8657-7ea9a43d03fb">HCRYPTPROV</a> handle for which the <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">reference count</a> is being incremented. This handle must have already been created using 
<a href="https://msdn.microsoft.com/57e13662-3189-4f8d-b90a-d1fbdc09b63c">CryptAcquireContext</a>.


### -param pdwReserved [in]

Reserved for future use and must be <b>NULL</b>.


### -param dwFlags [in]

Reserved for future use and must be zero.


## -returns



If the function succeeds, the return value is nonzero (TRUE).

If the function fails, the return value is zero (FALSE). For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. One possible error code is the following.

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
</table>
 




## -remarks



This function increases the <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">reference count</a> on a 
<a href="https://msdn.microsoft.com/8ec6b392-06bc-4717-8657-7ea9a43d03fb">HCRYPTPROV</a> handle so that multiple calls to 
<a href="https://msdn.microsoft.com/c1e3e708-b543-4e87-8638-a9946a83e614">CryptReleaseContext</a> are required to actually release the handle.


#### Examples

The following example increments the <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">reference count</a> on an acquired CSP handle.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>//--------------------------------------------------------------------
// hCryptProv is a HCRYPTPROV variable that was previously acquired
// by using CryptAcquireContext or CryptAcquireCertificatePrivateKey.

if(CryptContextAddRef(
       hCryptProv, 
       NULL, 
       0)) 
{
    printf("CryptContextAddRef succeeded. \n");
}
else
{
   printf("Error during CryptContextAddRef!\n");
   exit(1);
}
//--------------------------------------------------------------------
//  The reference count on hCryptProv is now greater than one. The 
//  first call to CryptReleaseContext will not release the provider 
//  handle. A second call to CryptReleaseContext would be needed to 
//  release the context.</pre>
</td>
</tr>
</table></span></div>
For another example that uses this function, see <a href="https://msdn.microsoft.com/e8d2503c-a38f-44f6-a653-ae9c7bf903bd">Example C Program: Using CryptAcquireContext</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/57e13662-3189-4f8d-b90a-d1fbdc09b63c">CryptAcquireContext</a>



<a href="https://msdn.microsoft.com/c1e3e708-b543-4e87-8638-a9946a83e614">CryptReleaseContext</a>



<a href="cryptography_functions.htm">Service Provider Functions</a>
 

 

