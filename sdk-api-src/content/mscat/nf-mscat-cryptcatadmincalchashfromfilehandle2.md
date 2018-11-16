---
UID: NF:mscat.CryptCATAdminCalcHashFromFileHandle2
title: CryptCATAdminCalcHashFromFileHandle2 function
author: windows-sdk-content
description: Calculates the hash for a file by using the specified algorithm.
old-location: security\cryptcatadmincalchashfromfilehandle2.htm
tech.root: SecCrypto
ms.assetid: CBFA60A8-5E5A-4FAD-8AD3-26539802CD53
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CryptCATAdminCalcHashFromFileHandle2, CryptCATAdminCalcHashFromFileHandle2 function [Security], mscat/CryptCATAdminCalcHashFromFileHandle2, security.cryptcatadmincalchashfromfilehandle2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mscat.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wintrust.lib
req.dll: Wintrust.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wintrust.dll
api_name:
 - CryptCATAdminCalcHashFromFileHandle2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- CryptCATAdminCalcHashFromFileHandle2
: 
---

# CryptCATAdminCalcHashFromFileHandle2 function


## -description


The <b>CryptCATAdminCalcHashFromFileHandle2</b> function calculates the hash for a file by using the specified algorithm.

This function has no associated import library. You must use the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to dynamically link to Wintrust.dll.


## -parameters




### -param hCatAdmin [in]

Handle of an open catalog administrator context. For more information, see <a href="https://msdn.microsoft.com/B089217A-5C12-4C51-8E46-3A9243347B21">CryptCATAdminAcquireContext2</a>.


### -param hFile [in]

A handle to the file whose hash is being calculated. This parameter cannot be <b>NULL</b> and must be a valid file handle.


### -param pcbHash [in, out]

Pointer to a <b>DWORD</b> variable that contains the number of bytes in the <i>pbHash</i> parameter. Upon input, set <i>pcbHash</i>  to the number of bytes allocated for <i>pbHash</i>. Upon return, <i>pcbHash</i> contains the number of returned bytes in  <i>pbHash</i>. If <i>pbHash</i> is set to <b>NULL</b>, then <i>pcbHash</i> contains the number of bytes to allocate for  <i>pbHash</i>.


### -param pbHash

Pointer to a <b>BYTE</b> buffer that receives the hash. If you set this parameter  to <b>NULL</b>, then <i>pcbHash</i> will contain the number of bytes to allocate for  <i>pbHash</i>, and a subsequent call can be made to retrieve the hash.


### -param dwFlags

Reserved. This value must be zero.


## -returns



If the function succeeds, the return value is nonzero (<b>TRUE</b>).

If the function fails, the return value is zero (<b>FALSE</b>). For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

The following table lists the error codes most commonly returned by the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.

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
The <i>hFile</i> parameter must not be <b>NULL</b>.

The <i>hFile</i> parameter must be a valid file handle.

The <i>pcbHash</i> parameter must not be <b>NULL</b>.

The <i>dwFlags</i> parameter must be zero (0).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The buffer pointed to by the <i>pbHash</i> parameter was not <b>NULL</b> but was not large enough to be written. The correct size of the required buffer is contained in the value pointed to by the <i>pcbHash</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_ALGID</b></dt>
</dl>
</td>
<td width="60%">
The hash algorithm specified by the <i>pwszHashAlgorithm</i> parameter cannot be found.

</td>
</tr>
</table>
 




## -remarks



The amount of time this function takes to execute depends on the length of the file being hashed, the algorithm being used, and the file location. For example, it takes several seconds to calculate the hash of a local file that is very large (a few hundred megabytes).




## -see-also




<a href="https://msdn.microsoft.com/4dc5688f-4b7a-4baf-9671-868cac7f1896">CryptCATAdminCalcHashFromFileHandle</a>



<a href="https://msdn.microsoft.com/CBFA60A8-5E5A-4FAD-8AD3-26539802CD53">CryptCATAdminCalcHashFromFileHandle2</a>
 

 

