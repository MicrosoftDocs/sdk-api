---
UID: NF:mscat.CryptCATAdminCalcHashFromFileHandle2
title: CryptCATAdminCalcHashFromFileHandle2 function (mscat.h)
description: Calculates the hash for a file by using the specified algorithm.
helpviewer_keywords: ["CryptCATAdminCalcHashFromFileHandle2","CryptCATAdminCalcHashFromFileHandle2 function [Security]","mscat/CryptCATAdminCalcHashFromFileHandle2","security.cryptcatadmincalchashfromfilehandle2"]
old-location: security\cryptcatadmincalchashfromfilehandle2.htm
tech.root: security
ms.assetid: CBFA60A8-5E5A-4FAD-8AD3-26539802CD53
ms.date: 12/05/2018
ms.keywords: CryptCATAdminCalcHashFromFileHandle2, CryptCATAdminCalcHashFromFileHandle2 function [Security], mscat/CryptCATAdminCalcHashFromFileHandle2, security.cryptcatadmincalchashfromfilehandle2
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CryptCATAdminCalcHashFromFileHandle2
 - mscat/CryptCATAdminCalcHashFromFileHandle2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wintrust.dll
api_name:
 - CryptCATAdminCalcHashFromFileHandle2
---

# CryptCATAdminCalcHashFromFileHandle2 function


## -description

The <b>CryptCATAdminCalcHashFromFileHandle2</b> function calculates the hash for a file by using the specified algorithm.

This function has no associated import library. You must use the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> functions to dynamically link to Wintrust.dll.

## -parameters

### -param hCatAdmin [in]

Handle of an open catalog administrator context. For more information, see <a href="/windows/desktop/api/mscat/nf-mscat-cryptcatadminacquirecontext2">CryptCATAdminAcquireContext2</a>.

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
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

The following table lists the error codes most commonly returned by the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

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

<a href="/windows/desktop/api/mscat/nf-mscat-cryptcatadmincalchashfromfilehandle">CryptCATAdminCalcHashFromFileHandle</a>



<a href="/windows/desktop/api/mscat/nf-mscat-cryptcatadmincalchashfromfilehandle2">CryptCATAdminCalcHashFromFileHandle2</a>