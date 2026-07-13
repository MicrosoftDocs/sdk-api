---
UID: NF:bcrypt.BCryptDestroyKey
title: BCryptDestroyKey function (bcrypt.h)
description: Destroys a key.
helpviewer_keywords: ["BCryptDestroyKey","BCryptDestroyKey function [Security]","bcrypt/BCryptDestroyKey","security.bcryptdestroykey_func"]
old-location: security\bcryptdestroykey_func.htm
tech.root: security
ms.assetid: 98c02e55-6489-4901-8a7a-021baac41965
ms.date: 12/05/2018
ms.keywords: BCryptDestroyKey, BCryptDestroyKey function [Security], bcrypt/BCryptDestroyKey, security.bcryptdestroykey_func
req.header: bcrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - BCryptDestroyKey
 - bcrypt/BCryptDestroyKey
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Bcrypt.dll
 - Ksecdd.sys
api_name:
 - BCryptDestroyKey
---

# BCryptDestroyKey function


## -description

The <b>BCryptDestroyKey</b> function destroys a key.

## -parameters

### -param hKey [in, out]

The handle of the key to destroy.

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
The key handle in the <i>hKey</i> parameter is not valid.

</td>
</tr>
</table>

## -remarks

When using a supported algorithm provider, <b>BCryptDestroyKey</b> can be called either from user mode or kernel mode. Kernel mode callers can execute either at <b>PASSIVE_LEVEL</b> <a href="/windows/desktop/SecGloss/i-gly">IRQL</a> or <b>DISPATCH_LEVEL</b> IRQL. If the current IRQL level is <b>DISPATCH_LEVEL</b>, the handle provided in the <i>hKey</i> parameter must be derived from an algorithm handle returned by a provider that was opened with the <b>BCRYPT_PROV_DISPATCH</b> flag.

To call this function in kernel mode, use Cng.lib, which is part of the Driver Development Kit (DDK). <b>Windows Server 2008 and Windows Vista:  </b>To call this function in kernel mode, use Ksecdd.lib.

## -see-also

<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptgeneratekeypair">BCryptGenerateKeyPair</a>



<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptgeneratesymmetrickey">BCryptGenerateSymmetricKey</a>



<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptimportkey">BCryptImportKey</a>



<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptimportkeypair">BCryptImportKeyPair</a>