---
UID: NF:ncrypt.NCryptSecretAgreement
title: NCryptSecretAgreement function (ncrypt.h)
description: Creates a secret agreement value from a private and a public key. (NCryptSecretAgreement)
helpviewer_keywords: ["NCRYPT_SILENT_FLAG","NCryptSecretAgreement","NCryptSecretAgreement function [Security]","ncrypt/NCryptSecretAgreement","security.ncryptsecretagreement"]
old-location: security\ncryptsecretagreement.htm
tech.root: security
ms.assetid: b5bf3eac-1fae-43e2-84b6-e8e5e255d7c5
ms.date: 12/05/2018
ms.keywords: NCRYPT_SILENT_FLAG, NCryptSecretAgreement, NCryptSecretAgreement function [Security], ncrypt/NCryptSecretAgreement, security.ncryptsecretagreement
req.header: ncrypt.h
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
req.lib: Ncrypt.lib
req.dll: Ncrypt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NCryptSecretAgreement
 - ncrypt/NCryptSecretAgreement
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ncrypt.dll
api_name:
 - NCryptSecretAgreement
---

# NCryptSecretAgreement function


## -description

The <b>NCryptSecretAgreement</b> function creates a secret agreement value from a private and a public key.

## -parameters

### -param hPrivKey [in]

The handle of the <a href="/windows/desktop/SecGloss/p-gly">private key</a> to use to create the secret agreement value. This key and the <i>hPubKey</i> key must come from the same key storage provider.

### -param hPubKey [in]

The handle of the <a href="/windows/desktop/SecGloss/p-gly">public key</a> to use to create the secret agreement value. This key and the <i>hPrivKey</i> key must come from the same key storage provider.

### -param phAgreedSecret [out]

A pointer to an <b>NCRYPT_SECRET_HANDLE</b> variable that receives a handle that represents the secret agreement value. When this handle is no longer needed, release it by passing it to the <a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncryptfreeobject">NCryptFreeObject</a> function.

### -param dwFlags [in]

Flags that modify function behavior. This can be zero or a combination of one or more of the following values.  The set of valid flags is specific to each key storage provider. The following flag applies to all providers.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NCRYPT_SILENT_FLAG"></a><a id="ncrypt_silent_flag"></a><dl>
<dt><b>NCRYPT_SILENT_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Requests that the key storage provider (KSP) not display any user interface. If the provider must display the UI to operate, the call fails and the KSP should set the <b>NTE_SILENT_CONTEXT</b> error code as the last error.

</td>
</tr>
</table>

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
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The <i>hPrivKey</i> or the <i>hPubKey</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_NO_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

</td>
</tr>
</table>

## -remarks

A service must not call this function from its <a href="/windows/win32/api/winsvc/nf-winsvc-startservicea">StartService Function</a>. If a service calls this function from its StartService function, a deadlock can occur, and the service may stop responding.

## -see-also

<a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncryptfreeobject">NCryptFreeObject</a>
