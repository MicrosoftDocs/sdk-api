---
UID: NF:mscat.CryptCATAdminAcquireContext2
title: CryptCATAdminAcquireContext2 function (mscat.h)
description: Acquires a handle to a catalog administrator context for a given hash algorithm and hash policy.
helpviewer_keywords: ["CryptCATAdminAcquireContext2","CryptCATAdminAcquireContext2 function [Security]","mscat/CryptCATAdminAcquireContext2","security.cryptcatadminacquirecontext2"]
old-location: security\cryptcatadminacquirecontext2.htm
tech.root: security
ms.assetid: B089217A-5C12-4C51-8E46-3A9243347B21
ms.date: 12/05/2018
ms.keywords: CryptCATAdminAcquireContext2, CryptCATAdminAcquireContext2 function [Security], mscat/CryptCATAdminAcquireContext2, security.cryptcatadminacquirecontext2
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
 - CryptCATAdminAcquireContext2
 - mscat/CryptCATAdminAcquireContext2
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
 - CryptCATAdminAcquireContext2
---

# CryptCATAdminAcquireContext2 function


## -description

The <b>CryptCATAdminAcquireContext2</b> function acquires a handle to a catalog administrator context for a given hash algorithm and hash policy.

 You can use this handle in subsequent calls to the following functions:
<ul>
<li>
<a href="/windows/desktop/api/mscat/nf-mscat-cryptcatadminaddcatalog">CryptCATAdminAddCatalog</a>
</li>
<li>
<a href="/windows/desktop/api/mscat/nf-mscat-cryptcatadminenumcatalogfromhash">CryptCATAdminEnumCatalogFromHash</a>
</li>
<li>
<a href="/windows/desktop/api/mscat/nf-mscat-cryptcatadminremovecatalog">CryptCATAdminRemoveCatalog</a>
</li>
</ul>This function has no associated import library. You must use the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> functions to dynamically link to Wintrust.dll.

## -parameters

### -param phCatAdmin [out]

A pointer to the catalog administrator context handle that is assigned by this function. When you have finished using the handle, close it by calling the <a href="/windows/desktop/api/mscat/nf-mscat-cryptcatadminreleasecontext">CryptCATAdminReleaseContext</a> function.

### -param pgSubsystem [in, optional]

A pointer to the <b>GUID</b> that identifies the subsystem. DRIVER_ACTION_VERIFY represents the subsystem for operating system components and third party drivers. This is the subsystem used by most implementations.

### -param pwszHashAlgorithm [in, optional]

Optional null-terminated Unicode string that specifies the name of the hash algorithm to use when calculating and verifying hashes. This value can be <b>NULL</b>. If it is <b>NULL</b>, the default hashing algorithm may be chosen, depending on the value you set for the <i>pStrongHashPolicy</i> parameter. The default algorithm in Windows 8 is SHA1. The default may change in future Windows versions. For more information, see Remarks.

### -param pStrongHashPolicy [in, optional]

Pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_strong_sign_para">CERT_STRONG_SIGN_PARA</a> structure that contains the parameters used to check for strong signatures. The function chooses the lowest common hashing algorithm that satisfies the specified policy and the algorithm specified by the <i>pwszHashAlgorithm</i> parameter or the system default algorithm (if no algorithm is specified).

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
The <i>phCatAdmin</i> parameter cannot be <b>NULL</b>.

The <i>dwFlags</i> parameter must be zero (0).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
There was insufficient memory to create a new catalog administrator object.

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

This function enables you to choose, or chooses for you, the hash algorithm to be used in  functions that require the catalog administrator context. Although you can set the name of the hashing algorithm, we recommend that you let the function determine the algorithm. Doing so protects your application from hard coding algorithms that may become untrusted in the future.

## -see-also

<a href="/windows/desktop/api/mscat/nf-mscat-cryptcatadminaddcatalog">CryptCATAdminAddCatalog</a>



<a href="/windows/desktop/api/mscat/nf-mscat-cryptcatadminreleasecontext">CryptCATAdminReleaseContext</a>



<a href="/windows/desktop/api/mscat/nf-mscat-cryptcatadminremovecatalog">CryptCATAdminRemoveCatalog</a>