---
UID: NF:wincrypt.CryptSetProviderW
title: CryptSetProviderW function
author: windows-sdk-content
description: Specifies the current user's default cryptographic service provider (CSP).
old-location: security\cryptsetprovider.htm
tech.root: seccrypto
ms.assetid: 44023a0c-3fb4-4746-a676-1671c3ad901b
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: CryptSetProvider, CryptSetProvider function [Security], CryptSetProviderA, CryptSetProviderW, _crypto2_cryptsetprovider, security.cryptsetprovider, wincrypt/CryptSetProvider, wincrypt/CryptSetProviderA, wincrypt/CryptSetProviderW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CryptSetProviderW (Unicode) and CryptSetProviderA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
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
 - CryptSetProvider
 - CryptSetProviderA
 - CryptSetProviderW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CryptSetProviderW function


## -description


<div class="alert"><b>Important</b>  This API is deprecated. New and existing software should start using <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/aa376210%28v=vs.85%29.aspx">Cryptography Next Generation APIs.</a> Microsoft may remove this API in future releases.</div><div> </div>The <b>CryptSetProvider</b> function specifies the current user's default <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP).

If a current user's default provider is set, that default provider is acquired by any call by that user to 
<a href="https://msdn.microsoft.com/57e13662-3189-4f8d-b90a-d1fbdc09b63c">CryptAcquireContext</a> specifying a <i>dwProvType</i> provider type but not a CSP name.

An enhanced version of this function, 
<a href="https://msdn.microsoft.com/5f0c2724-5144-4a22-a7da-2a5162f06f5d">CryptSetProviderEx</a>, is also available.
<div class="alert"><b>Note</b>  Typical applications do not use this function. It is intended for use solely by administrative applications.</div><div> </div>

## -parameters




### -param pszProvName [in]

Name of the new default CSP. The named CSP must be installed on the computer. For a list of available cryptographic providers, see 
<a href="https://msdn.microsoft.com/97e9a708-83b5-48b3-9d16-f7b54367dc4e">Cryptographic Provider Names</a>.


### -param dwProvType [in]

Provider type of the CSP specified by <i>pszProvName</i>.


## -returns



If the function succeeds, the return value is nonzero (TRUE).

If the function fails, the return value is zero (FALSE). For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. Some possible error codes are listed in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters specifies a handle that is not valid.

</td>
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
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
The operating system ran out of memory during the operation.

</td>
</tr>
</table>
 

Errors can also be propagated from internal calls to <a href="https://msdn.microsoft.com/e9ffad7f-c0b6-44ce-bf22-fbe45ca98bf4">RegCreateKeyEx</a> and <a href="https://msdn.microsoft.com/29b0e27c-4999-4e92-bd8b-bba74920bccc">RegSetValueEx</a>.




## -remarks



Typical applications do not specify a CSP name when calling 
<a href="https://msdn.microsoft.com/57e13662-3189-4f8d-b90a-d1fbdc09b63c">CryptAcquireContext</a>; however, an application does have the option of selecting a specific CSP. This gives a user the freedom to select a CSP with an appropriate level of security.

Since calling <b>CryptSetProvider</b> determines the CSP of a specified type used by all applications that run from that point on, this function must not be called without users' consent.




## -see-also




<a href="https://msdn.microsoft.com/57e13662-3189-4f8d-b90a-d1fbdc09b63c">CryptAcquireContext</a>



<a href="https://msdn.microsoft.com/97e9a708-83b5-48b3-9d16-f7b54367dc4e">Cryptographic Provider Names</a>



<a href="https://msdn.microsoft.com/e9ffad7f-c0b6-44ce-bf22-fbe45ca98bf4">RegCreateKeyEx</a>



<a href="https://msdn.microsoft.com/29b0e27c-4999-4e92-bd8b-bba74920bccc">RegSetValueEx</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa380252(v=VS.85).aspx">Service Provider Functions</a>
 

 

