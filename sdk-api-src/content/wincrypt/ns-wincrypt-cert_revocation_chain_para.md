---
UID: NS:wincrypt._CERT_REVOCATION_CHAIN_PARA
title: CERT_REVOCATION_CHAIN_PARA (wincrypt.h)
description: Contains parameters used for building a chain for an independent online certificate status protocol (OCSP) response signer certificate.
helpviewer_keywords: ["*PCERT_REVOCATION_CHAIN_PARA","CERT_CHAIN_REVOCATION_CHECK_OCSP_CERT","CERT_REVOCATION_CHAIN_PARA","CERT_REVOCATION_CHAIN_PARA structure [Security]","PCERT_REVOCATION_CHAIN_PARA","PCERT_REVOCATION_CHAIN_PARA structure pointer [Security]","security.cert_revocation_chain_para","wincrypt/CERT_REVOCATION_CHAIN_PARA","wincrypt/PCERT_REVOCATION_CHAIN_PARA"]
old-location: security\cert_revocation_chain_para.htm
tech.root: security
ms.assetid: 9cdcc81a-aef1-4a1e-94f8-7aa461225dae
ms.date: 12/05/2018
ms.keywords: '*PCERT_REVOCATION_CHAIN_PARA, CERT_CHAIN_REVOCATION_CHECK_OCSP_CERT, CERT_REVOCATION_CHAIN_PARA, CERT_REVOCATION_CHAIN_PARA structure [Security], PCERT_REVOCATION_CHAIN_PARA, PCERT_REVOCATION_CHAIN_PARA structure pointer [Security], security.cert_revocation_chain_para, wincrypt/CERT_REVOCATION_CHAIN_PARA, wincrypt/PCERT_REVOCATION_CHAIN_PARA'
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: CERT_REVOCATION_CHAIN_PARA, *PCERT_REVOCATION_CHAIN_PARA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_REVOCATION_CHAIN_PARA
 - wincrypt/_CERT_REVOCATION_CHAIN_PARA
 - PCERT_REVOCATION_CHAIN_PARA
 - wincrypt/PCERT_REVOCATION_CHAIN_PARA
 - CERT_REVOCATION_CHAIN_PARA
 - wincrypt/CERT_REVOCATION_CHAIN_PARA
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
 - CERT_REVOCATION_CHAIN_PARA
---

# CERT_REVOCATION_CHAIN_PARA structure


## -description

The <b>CERT_REVOCATION_CHAIN_PARA</b> structure contains parameters used for building a chain for an independent <a href="/windows/win32/api/wincrypt/ns-wincrypt-crypt_get_time_valid_object_extra_info">online certificate status protocol</a> (OCSP) response signer certificate. The <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_revocation_para">CERT_REVOCATION_PARA</a> and <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_get_time_valid_object_extra_info">CRYPT_GET_TIME_VALID_OBJECT_EXTRA_INFO</a> structure definitions include optional pointers to this structure.

## -struct-fields

### -field cbSize

The size, in bytes, of this structure.

### -field hChainEngine

A handle to the chain engine used by the caller.

### -field hAdditionalStore

A handle to a store that contains the certificates used to build the original chain. The handle can be <b>NULL</b>.

### -field dwChainFlags

A value for the <i>dwFlags</i> parameter passed to the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain">CertGetCertificateChain</a> function.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_REVOCATION_CHECK_OCSP_CERT"></a><a id="cert_chain_revocation_check_ocsp_cert"></a><dl>
<dt><b>CERT_CHAIN_REVOCATION_CHECK_OCSP_CERT</b></dt>
<dt>0x04000000</dt>
</dl>
</td>
<td width="60%">
This flag will be set by the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifyrevocation">CertVerifyRevocation</a> provider when it
calls <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain">CertGetCertificateChain</a> with an independent OCSP signer certificate.
When set, <b>CertGetCertificateChain</b> will call <b>CertVerifyRevocation</b> without
setting the pointer to the above <b>CERT_REVOCATION_CHAIN_PARA</b> data structure; this helps to prevent circular revocation checking.

</td>
</tr>
</table>

### -field dwUrlRetrievalTimeout

A value that contains the time-out limit, in milliseconds. If zero, the revocation handler's default time-out is used.

### -field pftCurrentTime

A pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure used in the freshness time check. If this pointer is <b>NULL</b>, the revocation handler uses the current time.

### -field pftCacheResync

A pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that governs the use of cached information. Any information cached  before this time is considered invalid and new information is retrieved. When set, this value overrides
    the registry configuration CacheResync time.

### -field cbMaxUrlRetrievalByteCount

A <b>DWORD</b> value that specifies the maximum number of bytes to download from the URL object. A value of 0 specifies no limit.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This member is not supported.