---
UID: NF:drt.DrtCreateDerivedKey
title: DrtCreateDerivedKey function (drt.h)
description: DrtCreateDerivedKey function creates a key that can be utilized by DrtRegisterKey when the DRT is using a derived key security provider.
helpviewer_keywords: ["DrtCreateDerivedKey","DrtCreateDerivedKey function [Peer Networking]","drt/DrtCreateDerivedKey","p2p.drtcreatederivedkey"]
old-location: p2p\drtcreatederivedkey.htm
tech.root: p2p
ms.assetid: 069358e0-4b61-44ed-b235-37f1d038feff
ms.date: 12/05/2018
ms.keywords: DrtCreateDerivedKey, DrtCreateDerivedKey function [Peer Networking], drt/DrtCreateDerivedKey, p2p.drtcreatederivedkey
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
 - DrtCreateDerivedKey
 - drt/DrtCreateDerivedKey
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
 - DrtCreateDerivedKey
---

## -description

The <b>DrtCreateDerivedKey</b> function creates a key that can be utilized by <a href="/windows/desktop/api/drt/nf-drt-drtregisterkey">DrtRegisterKey</a> when the DRT is using a derived key security provider.

## -parameters

### -param pLocalCert [in]

Pointer to the certificate that is the "local" portion of the chain.  The root of this chain must match the root specified by <i>pRootCert</i> in <a href="/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider">DrtCreateDerivedKeySecurityProvider</a>. This certificate is used to generate a key that is used to register and prove "key ownership" with the DRT.

### -param pKey [out]

Pointer to the created key.

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
<li><i>pLocalCert</i> is <b>NULL</b>.</li>
<li><i>pKey</i> is <b>NULL</b>.</li>
<li>The <b>pb</b> member in the <a href="/windows/desktop/api/drt/ns-drt-drt_data">DRT_DATA</a> structure  is <b>NULL</b>.</li>
<li>The <b>cb</b> member in the <a href="/windows/desktop/api/drt/ns-drt-drt_data">DRT_DATA</a> structure is not equal to 32 bytes.</li>
</ul>
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
</table>

## -see-also

<a href="/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider">DrtCreateDerivedKeySecurityProvider</a>



<a href="/windows/desktop/api/drt/nf-drt-drtdeletederivedkeysecurityprovider">DrtDeleteDerivedKeySecurityProvider</a>



<a href="/windows/desktop/api/drt/nf-drt-drtregisterkey">DrtRegisterKey</a>