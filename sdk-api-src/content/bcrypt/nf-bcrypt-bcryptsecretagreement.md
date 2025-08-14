---
UID: NF:bcrypt.BCryptSecretAgreement
title: BCryptSecretAgreement function (bcrypt.h)
description: Creates a secret agreement value from a private and a public key. (BCryptSecretAgreement)
helpviewer_keywords: ["BCryptSecretAgreement","BCryptSecretAgreement function [Security]","bcrypt/BCryptSecretAgreement","security.bcryptsecretagreement"]
old-location: security\bcryptsecretagreement.htm
tech.root: security
ms.assetid: 96863d81-3643-4962-8abf-db1cc2acde07
ms.date: 12/05/2018
ms.keywords: BCryptSecretAgreement, BCryptSecretAgreement function [Security], bcrypt/BCryptSecretAgreement, security.bcryptsecretagreement
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
 - BCryptSecretAgreement
 - bcrypt/BCryptSecretAgreement
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
 - BCryptSecretAgreement
---

# BCryptSecretAgreement function


## -description

The <b>BCryptSecretAgreement</b> function creates a secret agreement value from a private and a public key.

## -parameters

### -param hPrivKey [in]

The handle of the <a href="/windows/desktop/SecGloss/p-gly">private key</a> to use to create the secret agreement value. This key and the <i>hPubKey</i> key must come from the same CNG cryptographic algorithm provider.

### -param hPubKey [in]

The handle of the <a href="/windows/desktop/SecGloss/p-gly">public key</a> to use to create the secret agreement value. This key and the <i>hPrivKey</i> key must come from the same CNG cryptographic algorithm provider.

### -param phAgreedSecret [out]

A pointer to a <b>BCRYPT_SECRET_HANDLE</b> that receives a handle that represents the secret agreement value. This handle must be released by passing it to the <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptdestroysecret">BCryptDestroySecret</a> function when it is no longer needed.

### -param dwFlags [in]

A set of flags that modify the behavior of this function. No flags are defined for this function.

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
The key handle in the <i>hPrivKey</i> or <i>hPubKey</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The key handle in the <i>hPrivKey</i> parameter is not a Diffie-Hellman key.

</td>
</tr>
</table>

## -remarks

When using a supported algorithm provider, <b>BCryptSecretAgreement</b> can be called either from user mode or kernel mode. Kernel mode callers can execute either at <b>PASSIVE_LEVEL</b> <a href="/windows/desktop/SecGloss/i-gly">IRQL</a> or <b>DISPATCH_LEVEL</b> IRQL. If the current IRQL level is <b>DISPATCH_LEVEL</b>, the handles provided in the <i>hPrivKey</i> and <i>hPubKey</i>  parameters must be derived from an algorithm handle returned by a provider that was opened by using the <b>BCRYPT_PROV_DISPATCH</b> flag, and any pointers passed to the <b>BCryptSecretAgreement</b> function must refer to nonpaged (or locked) memory.

To call this function in kernel mode, use Cng.lib, which is part of the Driver Development Kit (DDK). <b>Windows Server 2008 and Windows Vista:  </b>To call this function in kernel mode, use Ksecdd.lib.

## -see-also

<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptdestroysecret">BCryptDestroySecret</a>
