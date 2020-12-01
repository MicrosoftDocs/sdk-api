---
UID: NF:drt.DrtCreateDerivedKeySecurityProvider
title: DrtCreateDerivedKeySecurityProvider function (drt.h)
description: DrtCreateDerivedKeySecurityProvider function creates the derived key security provider for a Distributed Routing Table.
helpviewer_keywords: ["DrtCreateDerivedKeySecurityProvider","DrtCreateDerivedKeySecurityProvider function [Peer Networking]","drt/DrtCreateDerivedKeySecurityProvider","p2p.drtcreatederivedkeysecurityprovider"]
old-location: p2p\drtcreatederivedkeysecurityprovider.htm
tech.root: p2p
ms.assetid: e4cc8326-e2bc-459f-97dd-a00cfd1ed35e
ms.date: 12/05/2018
ms.keywords: DrtCreateDerivedKeySecurityProvider, DrtCreateDerivedKeySecurityProvider function [Peer Networking], drt/DrtCreateDerivedKeySecurityProvider, p2p.drtcreatederivedkeysecurityprovider
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
req.lib: Drtprov.lib
req.dll: Drt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DrtCreateDerivedKeySecurityProvider
 - drt/DrtCreateDerivedKeySecurityProvider
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
 - DrtCreateDerivedKeySecurityProvider
---

# DrtCreateDerivedKeySecurityProvider function


## -description

The <b>DrtCreateDerivedKeySecurityProvider</b> function creates the derived key security provider for a Distributed Routing Table.

## -parameters

### -param pRootCert [in]

Pointer to the certificate that is the "root" portion of the chain. This is used to ensure that keys derived from the same chain can be verified.

### -param pLocalCert [out]

Pointer to the <a href="/windows/desktop/api/drt/ns-drt-drt_security_provider">DRT_SECURITY_PROVIDER</a> module to be included in the <a href="/windows/desktop/api/drt/ns-drt-drt_settings">DRT_SETTINGS</a> structure.

### -param ppSecurityProvider

Receives a pointer to the created security provider.

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
<i>pRootCert</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The system could not allocate memory for the security provider.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_CAPABILITY_MISMATCH</b></dt>
</dl>
</td>
<td width="60%">
<ul>
<li>The requested security algorithms are not available ( ie. BCRYPT_SHA256_ALGORITHM or  BCRYPT_AES_ALGORITHM).</li>
<li>The <a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptopenalgorithmprovider">BCryptOpenAlgorithmProvider</a> operation failed.</li>
<li>The <i>dwProvType</i> parameter  indicates that the certificate provider is not AES capable.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_INVALID_CERT_CHAIN</b></dt>
</dl>
</td>
<td width="60%">
No certificate store attached or there is an error in the certificate chain.

</td>
</tr>
</table>

## -remarks

The security provider created by this function is specific to the DRT it was created for. It cannot be shared by multiple DRT instances.

## -see-also

<a href="/windows/desktop/api/drt/ns-drt-drt_registration">DRT_REGISTRATION</a>



<a href="/windows/desktop/api/drt/ns-drt-drt_settings">DRT_SETTINGS</a>



<a href="/windows/desktop/api/drt/nf-drt-drtcreatederivedkey">DrtCreateDerivedKey</a>



<a href="/windows/desktop/api/drt/nf-drt-drtdeletederivedkeysecurityprovider">DrtDeleteDerivedKeySecurityProvider</a>