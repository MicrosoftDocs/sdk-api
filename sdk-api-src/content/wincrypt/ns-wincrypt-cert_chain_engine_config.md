---
UID: NS:wincrypt._CERT_CHAIN_ENGINE_CONFIG
title: CERT_CHAIN_ENGINE_CONFIG (wincrypt.h)
description: Sets parameters for building a non-default certificate chain engine. The engine used determines the ways that certificate chains are built.
helpviewer_keywords: ["*PCERT_CHAIN_ENGINE_CONFIG","CERT_CHAIN_CACHE_END_CERT","CERT_CHAIN_CACHE_ONLY_URL_RETRIEVAL","CERT_CHAIN_DISABLE_AIA","CERT_CHAIN_ENABLE_CACHE_AUTO_UPDATE","CERT_CHAIN_ENABLE_SHARE_STORE","CERT_CHAIN_ENGINE_CONFIG","CERT_CHAIN_ENGINE_CONFIG structure [Security]","CERT_CHAIN_EXCLUSIVE_ENABLE_CA_FLAG","CERT_CHAIN_USE_LOCAL_MACHINE_STORE","PCERT_CHAIN_ENGINE_CONFIG","PCERT_CHAIN_ENGINE_CONFIG structure pointer [Security]","_crypto2_cert_chain_engine_config","security.cert_chain_engine_config","wincrypt/CERT_CHAIN_ENGINE_CONFIG","wincrypt/PCERT_CHAIN_ENGINE_CONFIG"]
old-location: security\cert_chain_engine_config.htm
tech.root: security
ms.assetid: 9e010eb9-2cbb-4fca-ba5c-4a5a50f23786
ms.date: 12/05/2018
ms.keywords: '*PCERT_CHAIN_ENGINE_CONFIG, CERT_CHAIN_CACHE_END_CERT, CERT_CHAIN_CACHE_ONLY_URL_RETRIEVAL, CERT_CHAIN_DISABLE_AIA, CERT_CHAIN_ENABLE_CACHE_AUTO_UPDATE, CERT_CHAIN_ENABLE_SHARE_STORE, CERT_CHAIN_ENGINE_CONFIG, CERT_CHAIN_ENGINE_CONFIG structure [Security], CERT_CHAIN_EXCLUSIVE_ENABLE_CA_FLAG, CERT_CHAIN_USE_LOCAL_MACHINE_STORE, PCERT_CHAIN_ENGINE_CONFIG, PCERT_CHAIN_ENGINE_CONFIG structure pointer [Security], _crypto2_cert_chain_engine_config, security.cert_chain_engine_config, wincrypt/CERT_CHAIN_ENGINE_CONFIG, wincrypt/PCERT_CHAIN_ENGINE_CONFIG'
req.header: wincrypt.h
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
req.typenames: CERT_CHAIN_ENGINE_CONFIG, *PCERT_CHAIN_ENGINE_CONFIG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_CHAIN_ENGINE_CONFIG
 - wincrypt/_CERT_CHAIN_ENGINE_CONFIG
 - PCERT_CHAIN_ENGINE_CONFIG
 - wincrypt/PCERT_CHAIN_ENGINE_CONFIG
 - CERT_CHAIN_ENGINE_CONFIG
 - wincrypt/CERT_CHAIN_ENGINE_CONFIG
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CERT_CHAIN_ENGINE_CONFIG
---

# CERT_CHAIN_ENGINE_CONFIG structure


## -description

The <b>CERT_CHAIN_ENGINE_CONFIG</b> structure sets parameters for building a non-default certificate chain engine. The engine used determines the ways that certificate chains are built.

## -struct-fields

### -field cbSize

Size of this structure in bytes.

### -field hRestrictedRoot

This configuration parameter can be used to restrict the root store. If used, it can be the handle of any HCERTSTORE containing only a proper subset of the certificates in the root store.

### -field hRestrictedTrust

Store handle. If used, restricts the stores searched to find CTLs.

### -field hRestrictedOther

Store handle. If used, restricts the <a href="/windows/desktop/SecGloss/c-gly">stores</a> searched for certificates and <a href="/windows/desktop/SecGloss/c-gly">CRLs</a>.

### -field cAdditionalStore

Count of additional stores to be searched for certificates and CRLs needed to build chains.

### -field rghAdditionalStore

A pointer to an array of store handles for any additional stores to be searched in building chains.

### -field dwFlags

The following flags are defined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_CACHE_END_CERT"></a><a id="cert_chain_cache_end_cert"></a><dl>
<dt><b>CERT_CHAIN_CACHE_END_CERT</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Information in the end certificate is cached. By default, information in all certificates except the end certificate is cached as a chain is built. Setting this flag extends the caching to the end certificate.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_CACHE_ONLY_URL_RETRIEVAL"></a><a id="cert_chain_cache_only_url_retrieval"></a><dl>
<dt><b>CERT_CHAIN_CACHE_ONLY_URL_RETRIEVAL</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Use only cached URLs in building a certificate chain. The Internet and intranet are not searched for URL-based objects.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_USE_LOCAL_MACHINE_STORE"></a><a id="cert_chain_use_local_machine_store"></a><dl>
<dt><b>CERT_CHAIN_USE_LOCAL_MACHINE_STORE</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
Build the chain using the LocalMachine registry location as opposed to the CurrentUser location.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_ENABLE_CACHE_AUTO_UPDATE"></a><a id="cert_chain_enable_cache_auto_update"></a><dl>
<dt><b>CERT_CHAIN_ENABLE_CACHE_AUTO_UPDATE</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
Enable automatic updating of the cache as a chain is being built.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_ENABLE_SHARE_STORE"></a><a id="cert_chain_enable_share_store"></a><dl>
<dt><b>CERT_CHAIN_ENABLE_SHARE_STORE</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
Allow certificate stores used to build the chain to be shared.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_DISABLE_AIA"></a><a id="cert_chain_disable_aia"></a><dl>
<dt><b>CERT_CHAIN_DISABLE_AIA</b></dt>
<dt>0x00002000</dt>
</dl>
</td>
<td width="60%">
Turn off  Authority Information Access (AIA) retrievals explicitly.

</td>
</tr>
</table>

### -field dwUrlRetrievalTimeout

Number of milliseconds before a time-out for network based–URL object retrievals. Can be set to zero to use the default limit.

### -field MaximumCachedCertificates

Limit on the number of certificates that can be cached as a chain is built. Can be set to 0 to use the default limit.

### -field CycleDetectionModulus

Number of certificates added to the chain before a check is made to determine whether there is a cycle of certificates in the chain. A cycle may be defined as having the same certificate in two different places in a chain. 




The lower the number, the more frequently checks will be made. Extra checking for cycles of certificates will slow the process considerably. This parameter can be set to zero to use the default limit.

### -field hExclusiveRoot

Handle to a  certificate store that contains exclusive trust anchors.  If either the <b>hExclusiveRoot</b> or <b>hExclusiveTrustedPeople</b> member points to a valid store, exclusive trust mode is used for the chain building.

<b>Windows 7 and Windows Server 2008 R2:  </b>Support for this member begins.

### -field hExclusiveTrustedPeople

Handle to a certificate store that contains  application-specific peer trusted certificates. If either the <b>hExclusiveRoot</b> or <b>hExclusiveTrustedPeople</b> member points to a valid store, exclusive trust mode is used for the chain building.

<b>Windows 7 and Windows Server 2008 R2:  </b>Support for this member begins.

### -field dwExclusiveFlags

The following flag can be set. The flag applies only if the <b>hExclusiveRoot</b> or <b>hExclusiveTrustedPeople</b> or both are not <b>NULL</b>.

<b>Windows 8 and Windows Server 2012:  </b>Support for this member begins.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_EXCLUSIVE_ENABLE_CA_FLAG"></a><a id="cert_chain_exclusive_enable_ca_flag"></a><dl>
<dt><b>CERT_CHAIN_EXCLUSIVE_ENABLE_CA_FLAG</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Indicates that a non-self-signed intermediate CA certificate in the <b>hExclusiveRoot</b> store should be treated as a trust anchor during certificate validation. If a certificate chains up to this CA, chain building is terminated and the certificate is considered trusted. No signature verification or revocation checking is performed on the CA certificate.

By default, if this flag is not set, only self-signed certificates in the <b>hExclusiveRoot</b> store are treated as trust anchors.

See also the <b>CERT_TRUST_IS_CA_TRUSTED</b> value in the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_trust_status">CERT_TRUST_STATUS</a> structure.

</td>
</tr>
</table>

## -remarks

The chain-building engine uses four certificate stores in building chains. These are hRoot, hWorld, hTrust, and hOther. These stores' handles are established by using information in this structure when a chain engine is created.

hRoot is the store handle from <b>hRestrictedRoot</b> or, if <b>hRestrictedRoot</b> is <b>NULL</b>, the handle for System Store "Root."

hWorld is a collection certificate store including sibling stores hRoot, "CA," "My," "Trust," and any additional stores whose handles are in the array pointed to by <b>rghAdditionalStore</b>.

hTrust is the store handle from <b>hRestrictedTrust</b> or, if <b>hRestrictedTrust</b> is <b>NULL</b>, hWorld.

hOther is <b>hRestrictedOther</b> plus hRoot or, if <b>hRestrictedTrust</b> is non-<b>NULL</b>, the hWorld collection store plus the store handle from <b>hRestrictedTrust</b>.

Exclusive trust mode allows applications to specify trust anchors and peer-trusted certificates  for certificate chain validation. In the exclusive trust mode, the root store and the trusted people store on the system are ignored, and the anchors and certificates pointed to by the <b>hExclusiveRoot</b> and <b>hExclusiveTrustedPeople</b> members are used instead.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_trust_status">CERT_TRUST_STATUS</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certcreatecertificatechainengine">CertCreateCertificateChainEngine</a>