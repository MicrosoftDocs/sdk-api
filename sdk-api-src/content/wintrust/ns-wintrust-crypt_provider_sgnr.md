---
UID: NS:wintrust._CRYPT_PROVIDER_SGNR
title: CRYPT_PROVIDER_SGNR (wintrust.h)
description: Provides information about a signer or countersigner.
helpviewer_keywords: ["*PCRYPT_PROVIDER_SGNR","CRYPT_PROVIDER_SGNR","CRYPT_PROVIDER_SGNR structure [Security]","PCRYPT_PROVIDER_SGNR","PCRYPT_PROVIDER_SGNR structure pointer [Security]","SGNR_TYPE_TIMESTAMP","security.crypt_provider_sgnr","wintrust/CRYPT_PROVIDER_SGNR","wintrust/PCRYPT_PROVIDER_SGNR"]
old-location: security\crypt_provider_sgnr.htm
tech.root: security
ms.assetid: 39cf9a03-768d-4ae0-a19d-17652181dbe4
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_PROVIDER_SGNR, CRYPT_PROVIDER_SGNR, CRYPT_PROVIDER_SGNR structure [Security], PCRYPT_PROVIDER_SGNR, PCRYPT_PROVIDER_SGNR structure pointer [Security], SGNR_TYPE_TIMESTAMP, security.crypt_provider_sgnr, wintrust/CRYPT_PROVIDER_SGNR, wintrust/PCRYPT_PROVIDER_SGNR'
req.header: wintrust.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CRYPT_PROVIDER_SGNR, *PCRYPT_PROVIDER_SGNR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_PROVIDER_SGNR
 - wintrust/_CRYPT_PROVIDER_SGNR
 - PCRYPT_PROVIDER_SGNR
 - wintrust/PCRYPT_PROVIDER_SGNR
 - CRYPT_PROVIDER_SGNR
 - wintrust/CRYPT_PROVIDER_SGNR
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wintrust.h
api_name:
 - CRYPT_PROVIDER_SGNR
---

# CRYPT_PROVIDER_SGNR structure


## -description

<p class="CCE_Message">[The  <b>CRYPT_PROVIDER_SGNR</b> structure is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CRYPT_PROVIDER_SGNR</b> structure provides information about a signer or countersigner.

## -struct-fields

### -field cbStruct

The size, in bytes, of this structure.

### -field sftVerifyAsOf

The current time, or the time stamp.

### -field csCertChain

Number of elements in the <b>pasCertChain</b> array.

### -field pasCertChain

Array of <a href="/windows/desktop/api/wintrust/ns-wintrust-crypt_provider_cert">CRYPT_PROVIDER_CERT</a> structures.

### -field dwSignerType

Signer type, if known by the policy. This value is zero, if the signer type is unknown, or the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SGNR_TYPE_TIMESTAMP"></a><a id="sgnr_type_timestamp"></a><dl>
<dt><b>SGNR_TYPE_TIMESTAMP</b></dt>
<dt>     0x00000010</dt>
</dl>
</td>
<td width="60%">
Time stamp signer.

</td>
</tr>
</table>

### -field psSigner

A pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_signer_info">CMSG_SIGNER_INFO</a> structure.

### -field dwError

Error value, if any, while building or verifying the signer.

### -field csCounterSigners

Number of elements in the <b>pasCounterSigners</b>  array.

### -field pasCounterSigners

A pointer to an array of <b>CRYPT_PROVIDER_SGNR</b> structures that represent the countersigners.

### -field pChainContext

A pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context">CERT_CHAIN_CONTEXT</a> structure.