---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# CryptSetProviderExW function


## -description


<div class="alert"><b>Important</b>  This API is deprecated. New and existing software should start using <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/aa376210%28v=vs.85%29.aspx">Cryptography Next Generation APIs.</a> Microsoft may remove this API in future releases.</div><div> </div>The <b>CryptSetProviderEx</b> function specifies the default <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP) of a specified provider type for the local computer or current user.
<div class="alert"><b>Note</b>  Typical applications do not use this function. It is intended for use solely by administrative applications.</div><div> </div>

## -parameters




### -param pszProvName [in]

The name of the new default CSP. This must be a CSP installed on the computer. For a list of available cryptographic providers, see 
<a href="https://msdn.microsoft.com/97e9a708-83b5-48b3-9d16-f7b54367dc4e">Cryptographic Provider Names</a>.


### -param dwProvType [in]

The provider type of the CSP specified by <i>pszProvName</i>.


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
<td width="40%"><a id="CRYPT_DELETE_DEFAULT"></a><a id="crypt_delete_default"></a><dl>
<dt><b>CRYPT_DELETE_DEFAULT</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Can be used in conjunction with CRYPT_MACHINE_DEFAULT or CRYPT_USER_DEFAULT to delete the default.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_USER_DEFAULT"></a><a id="crypt_user_default"></a><dl>
<dt><b>CRYPT_USER_DEFAULT</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Causes the user-context default CSP of the specified type to be set.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_MACHINE_DEFAULT"></a><a id="crypt_machine_default"></a><dl>
<dt><b>CRYPT_MACHINE_DEFAULT</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Causes the computer default CSP of the specified type to be set.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the return value is nonzero (<b>TRUE</b>).

If the function fails, the return value is zero (<b>FALSE</b>). For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. Possible error codes include those shown in the following table.

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
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
The operating system ran out of memory.

</td>
</tr>
</table>
 




## -remarks



Most applications do not specify a CSP name when calling the 
<a href="https://msdn.microsoft.com/57e13662-3189-4f8d-b90a-d1fbdc09b63c">CryptAcquireContext</a> function; however, an application can specify a CSP name and thereby select a CSP with an appropriate level of security. Because calls to <b>CryptSetProviderEx</b> determine the CSP of a specified type used by all applications from that point on, <b>CryptSetProviderEx</b> must never be called without a user's consent.




## -see-also




<a href="https://msdn.microsoft.com/57e13662-3189-4f8d-b90a-d1fbdc09b63c">CryptAcquireContext</a>



<a href="https://msdn.microsoft.com/44023a0c-3fb4-4746-a676-1671c3ad901b">CryptSetProvider</a>



<a href="cryptography_functions.htm">Service Provider Functions</a>
 

 

