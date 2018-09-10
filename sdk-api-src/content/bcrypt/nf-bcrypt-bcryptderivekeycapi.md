---
UID: NF:bcrypt.BCryptDeriveKeyCapi
title: BCryptDeriveKeyCapi function
author: windows-sdk-content
description: Derives a key from a hash value.
old-location: security\bcryptderivekeycapi.htm
tech.root: SecCNG
ms.assetid: bebb0767-8c54-48b7-864c-f53caea7120d
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: BCryptDeriveKeyCapi, BCryptDeriveKeyCapi function [Security], bcrypt/BCryptDeriveKeyCapi, security.bcryptderivekeycapi
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: bcrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bcrypt.lib
req.dll: Bcrypt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Bcrypt.dll
api_name:
 - BCryptDeriveKeyCapi
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# BCryptDeriveKeyCapi function


## -description


The <b>BCryptDeriveKeyCapi</b> function derives a key from a hash value.

This function is  provided as a helper function to assist in migrating legacy Cryptography API (CAPI)–based applications to use Cryptography API: Next Generation (CNG).  The <b>BCryptDeriveKeyCapi</b> function performs the key derivation in a manner that is compatible with the CAPI <a href="https://msdn.microsoft.com/en-us/library/Aa379916(v=VS.85).aspx">CryptDeriveKey</a> function.


## -parameters




### -param hHash [in]

The handle of the hash object. The handle is obtained by calling the <a href="https://msdn.microsoft.com/en-us/library/Aa375383(v=VS.85).aspx">BCryptCreateHash</a> function. When you have finished using the handle, you must free it by calling the <a href="https://msdn.microsoft.com/067dac61-98b9-478c-ac4d-e141961865e9">BCryptDestroyHash</a> function.


### -param hTargetAlg [in, optional]

The handle of the algorithm object.  This can be an <a href="https://msdn.microsoft.com/557436b4-f7f1-4708-acc7-c6b47e6322ad">ALG_ID</a> value that is compatible with the <a href="https://msdn.microsoft.com/en-us/library/Aa379916(v=VS.85).aspx">CryptDeriveKey</a> function.

<div class="alert"><b>Note</b>  Limitations in CAPI and key expansion prevent the use of any hash algorithm that generates an output that is larger than 512 bits.</div>
<div> </div>

### -param pbDerivedKey [out]

A pointer to the buffer that receives the derived key.


### -param cbDerivedKey [in]

The size, in characters, of the derived key pointed to by the <i>pbDerivedKey</i> parameter.


### -param dwFlags [in]

This parameter is reserved and must be set to zero.


## -returns



Returns a status code that indicates the success or failure of the function.


Possible return codes include, but are not limited to, the following.



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle in the <i>hHash</i> or  <i>hTargetAlg</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The value in  the <i>cbDerivedKey</i> parameter is larger than twice the output size of the hash function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NO_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.
 

</td>
</tr>
</table>
 




## -remarks



This function does not support the PK salt functionality of the CAPI <a href="https://msdn.microsoft.com/en-us/library/Aa379916(v=VS.85).aspx">CryptDeriveKey</a> function. 



