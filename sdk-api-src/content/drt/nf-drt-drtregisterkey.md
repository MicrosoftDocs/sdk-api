---
UID: NF:drt.DrtRegisterKey
title: DrtRegisterKey function (drt.h)
description: The DrtRegisterKey function registers a key in the DRT.
helpviewer_keywords: ["DrtRegisterKey","DrtRegisterKey function [Peer Networking]","drt/DrtRegisterKey","p2p.drtregisterkey"]
old-location: p2p\drtregisterkey.htm
tech.root: p2p
ms.assetid: 9aa1ee16-648d-4769-a464-4659dea14dba
ms.date: 12/05/2018
ms.keywords: DrtRegisterKey, DrtRegisterKey function [Peer Networking], drt/DrtRegisterKey, p2p.drtregisterkey
req.header: drt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Drt.lib
req.dll: Drt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DrtRegisterKey
 - drt/DrtRegisterKey
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - drt.dll
api_name:
 - DrtRegisterKey
---

# DrtRegisterKey function


## -description

The <b>DrtRegisterKey</b> function registers a key in the DRT.

## -parameters

### -param hDrt [in]

A pointer to a handle returned by the <a href="/windows/desktop/api/drt/nf-drt-drtopen">DrtOpen</a> function.

### -param pRegistration [in]

A pointer to a handle to the <a href="/windows/desktop/api/drt/ns-drt-drt_registration">DRT_REGISTRATION</a> structure.

### -param pvKeyContext [in, optional]

Pointer to the context data associated with the key in the DRT. This data is passed to the key-specific functions of the security provider.

### -param phKeyRegistration [out]

Pointer to a handle for a key that has been registered.

## -returns

This function returns S_OK on success. Other possible values include:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<ul>
<li><i>pRegistration</i> is <b>NULL</b></li>
<li>The <b>cb</b> value  of the <b>appData</b> member of the <a href="/windows/desktop/api/drt/ns-drt-drt_registration">DRT_REGISTRATION</a> structure is too large (ie. less than 1).</li>
<li>The <b>cb</b> value  of the <b>appData</b> member of the    <a href="/windows/desktop/api/drt/ns-drt-drt_registration">DRT_REGISTRATION</a> structure is too large (ie. more than 5120).</li>
<li>The <b>pb</b> value  of the <b>key</b> member   of the <a href="/windows/desktop/api/drt/ns-drt-drt_registration">DRT_REGISTRATION</a> structure is <b>NULL</b>.</li>
<li><i>phKeyRegistration</i> is <b>NULL</b></li>
</ul>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
<i>hDrt</i> is an invalid handle or <i>phKeyRegistration</i> is an invalid handle

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_INVALID_KEY_SIZE</b></dt>
</dl>
</td>
<td width="60%">
The size of cb value of the  key member of the DRT_REGISTRATION structure  is not equal to 256 bits or the <b>pb</b> value  of the <b>key</b> member   of the <a href="/windows/desktop/api/drt/ns-drt-drt_registration">DRT_REGISTRATION</a> structure is <b>NULL</b>..

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_FAULTED</b></dt>
</dl>
</td>
<td width="60%">
The DRT cloud is in the faulted state.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_DUPLICATE_KEY</b></dt>
</dl>
</td>
<td width="60%">
The key is already registered.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_INVALID_CERT_CHAIN</b></dt>
</dl>
</td>
<td width="60%">
The provided certification chain is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_CAPABILITY_MISMATCH</b></dt>
</dl>
</td>
<td width="60%">
Supplied certificate provider is not AES capable.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_INVALID_KEY</b></dt>
</dl>
</td>
<td width="60%">
Supplied key does not match generated key.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_TRANSPORT_NO_DEST_ADDRESSES</b></dt>
</dl>
</td>
<td width="60%">
Valid address not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_TRANSPORT_SHUTTING_DOWN</b></dt>
</dl>
</td>
<td width="60%">
Transport is shutting down.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_INVALID_TRANSPORT_PROVIDER</b></dt>
</dl>
</td>
<td width="60%">
Transport provider is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_TRANSPORTPROVIDER_NOT_ATTACHED</b></dt>
</dl>
</td>
<td width="60%">
Transport is not attached.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_SECURITYPROVIDER_NOT_ATTACHED</b></dt>
</dl>
</td>
<td width="60%">
Security provider is not attached.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_TRANSPORT_NOT_BOUND</b></dt>
</dl>
</td>
<td width="60%">
Transport is not currently bound.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The system is out of memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
<ul>
<li>The GlobalControl.HandleTable is <b>NULL</b>.</li>
<li>The cloud is shutting down.</li>
<li>The DRT is shutting down.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unexpected fatal error has occurred.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  <b>DrtRegisterKey</b> may also surface errors from underlying calls to <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgetprovparam">CryptGetProvParam</a>, <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain">CertGetCertificateChain</a>, <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certopenstore">CertOpenStore</a>, <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certaddcertificatecontexttostore">CertAddCertificateContextToStore</a>, <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptcontextaddref">CryptContextAddRef</a>, <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecertificateprivatekey">CryptAcquireCertificatePrivateKey</a>, <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certsavestore">CertSaveStore</a>, <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl">WSAIoctl</a>, <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptimportpublickeyinfoex2">CryptImportPublicKeyInfoEx2</a>, <a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncryptsignhash">NCryptSignHash</a>, <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certenumcertificatesinstore">CertEnumCertificatesInStore</a>, <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptgetproperty">BCryptGetProperty</a>, <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptgenrandom">BCryptGenRandom</a>, <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptgeneratesymmetrickey">BCryptGenerateSymmetricKey</a> and <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptencrypt">BCryptEncrypt</a>.</div>
<div> </div>

## -remarks

 A node can register keys while in the <b>DRT_ACTIVE</b>, <b>DRT_ALONE</b>, or <b>DRT_NO_NETWORK</b> state.   However, keys registered in <b>DRT_ALONE</b> and <b>DRT_NO_NETWORK</b> states can only be recognized by other DRTs after the local node has transitioned to <b>DRT_ACTIVE</b>.

 To update an existing key, an application must first deregister the key with <a href="/windows/desktop/api/drt/nf-drt-drtunregisterkey">DrtUnregisterKey</a> before calling <b>DrtRegisterKey</b> to register the updated key.

## -see-also

<a href="/windows/desktop/api/drt/ns-drt-drt_registration">DRT_REGISTRATION</a>



<a href="/windows/desktop/api/drt/nf-drt-drtopen">DrtOpen</a>



<a href="/windows/desktop/api/drt/nf-drt-drtunregisterkey">DrtUnregisterKey</a>