---
UID: NF:bcrypt.BCryptDestroySecret
title: BCryptDestroySecret function (bcrypt.h)
description: Destroys a secret agreement handle that was created by using the BCryptSecretAgreement function.
helpviewer_keywords: ["BCryptDestroySecret","BCryptDestroySecret function [Security]","bcrypt/BCryptDestroySecret","security.bcryptdestroysecret"]
old-location: security\bcryptdestroysecret.htm
tech.root: security
ms.assetid: 237743ff-ecb1-4c01-b4f9-192f27716f2c
ms.date: 12/05/2018
ms.keywords: BCryptDestroySecret, BCryptDestroySecret function [Security], bcrypt/BCryptDestroySecret, security.bcryptdestroysecret
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
 - BCryptDestroySecret
 - bcrypt/BCryptDestroySecret
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
 - BCryptDestroySecret
---

# BCryptDestroySecret function


## -description

The <b>BCryptDestroySecret</b> function destroys a secret agreement handle that was created by using the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptsecretagreement">BCryptSecretAgreement</a> function.

## -parameters

### -param hSecret [in]

The <b>BCRYPT_SECRET_HANDLE</b> to be destroyed.

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
The handle in the <i>hSecret</i> parameter is not valid.

</td>
</tr>
</table>

## -remarks

When using a supported algorithm provider, <b>BCryptDestroySecret</b> can be called either from user mode or kernel mode. Kernel mode callers can execute either at <b>PASSIVE_LEVEL</b> <a href="/windows/desktop/SecGloss/i-gly">IRQL</a> or <b>DISPATCH_LEVEL</b> IRQL. If the current IRQL level is <b>DISPATCH_LEVEL</b>, the handle provided in the <i>hSecret</i> parameter must be derived from an algorithm handle returned by a provider that was opened by using the <b>BCRYPT_PROV_DISPATCH</b> flag.

To call this function in kernel mode, use Cng.lib, which is part of the Driver Development Kit (DDK). <b>Windows Server 2008 and Windows Vista:  </b>To call this function in kernel mode, use Ksecdd.lib.

## -see-also

<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptsecretagreement">BCryptSecretAgreement</a>