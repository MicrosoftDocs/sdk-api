---
UID: NS:wincrypt._CERT_SELECT_CHAIN_PARA
title: CERT_SELECT_CHAIN_PARA (wincrypt.h)
description: Contains the parameters used for building and selecting chains.
helpviewer_keywords: ["*PCERT_SELECT_CHAIN_PARA","CERT_CHAIN_CACHE_ONLY_URL_RETRIEVAL","CERT_CHAIN_REVOCATION_CHECK_CACHE_ONLY","CERT_SELECT_CHAIN_PARA","CERT_SELECT_CHAIN_PARA structure [Security]","PCCERT_SELECT_CHAIN_PARA","PCCERT_SELECT_CHAIN_PARA structure pointer [Security]","PCERT_SELECT_CHAIN_PARA","PCERT_SELECT_CHAIN_PARA structure pointer [Security]","security.cert_select_chain_para","wincrypt/CERT_SELECT_CHAIN_PARA","wincrypt/PCCERT_SELECT_CHAIN_PARA","wincrypt/PCERT_SELECT_CHAIN_PARA"]
old-location: security\cert_select_chain_para.htm
tech.root: security
ms.assetid: 55c6c063-2a65-40ad-8d3f-7723b83cf021
ms.date: 12/05/2018
ms.keywords: '*PCERT_SELECT_CHAIN_PARA, CERT_CHAIN_CACHE_ONLY_URL_RETRIEVAL, CERT_CHAIN_REVOCATION_CHECK_CACHE_ONLY, CERT_SELECT_CHAIN_PARA, CERT_SELECT_CHAIN_PARA structure [Security], PCCERT_SELECT_CHAIN_PARA, PCCERT_SELECT_CHAIN_PARA structure pointer [Security], PCERT_SELECT_CHAIN_PARA, PCERT_SELECT_CHAIN_PARA structure pointer [Security], security.cert_select_chain_para, wincrypt/CERT_SELECT_CHAIN_PARA, wincrypt/PCCERT_SELECT_CHAIN_PARA, wincrypt/PCERT_SELECT_CHAIN_PARA'
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CERT_SELECT_CHAIN_PARA, *PCERT_SELECT_CHAIN_PARA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_SELECT_CHAIN_PARA
 - wincrypt/_CERT_SELECT_CHAIN_PARA
 - PCERT_SELECT_CHAIN_PARA
 - wincrypt/PCERT_SELECT_CHAIN_PARA
 - CERT_SELECT_CHAIN_PARA
 - wincrypt/CERT_SELECT_CHAIN_PARA
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
 - CERT_SELECT_CHAIN_PARA
---

# CERT_SELECT_CHAIN_PARA structure


## -description

The <b>CERT_SELECT_CHAIN_PARA</b> structure contains the parameters used for building and selecting chains. This structure is used by the   <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain">CertGetCertificateChain</a> and <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certselectcertificatechains">CertSelectCertificateChains</a> functions.

## -struct-fields

### -field hChainEngine

The handle of the chain engine to use to build the chain. If the value of the <i>hChainEngine</i> parameter is <b>NULL</b>, the default chain engine, <b>HCCE_CURRENT_USER</b>, is used.

### -field pTime

A pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that contains the time for which the chain is to be validated. If the  value of the <i>pTime</i> parameter is <b>NULL</b>, the current system time is passed to this parameter. 

<div class="alert"><b>Note</b>  The time does not affect trust list, revocation, or root store checking.</div>
<div> </div>

### -field hAdditionalStore

The handle of any additional store to search for supporting certificates and certificate trust lists (CTLs). This parameter can be <b>NULL</b> if no additional store is to be searched.

### -field pChainPara

A pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_para">CERT_CHAIN_PARA</a> structure that includes chain-building parameters.

### -field dwFlags

Flag values that indicate special processing during chain build. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_REVOCATION_CHECK_CACHE_ONLY"></a><a id="cert_chain_revocation_check_cache_only"></a><dl>
<dt><b>CERT_CHAIN_REVOCATION_CHECK_CACHE_ONLY</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Revocation checking only accesses cached URLs.


</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CHAIN_CACHE_ONLY_URL_RETRIEVAL"></a><a id="cert_chain_cache_only_url_retrieval"></a><dl>
<dt><b>CERT_CHAIN_CACHE_ONLY_URL_RETRIEVAL</b></dt>
<dt>0x80000000</dt>
</dl>
</td>
<td width="60%">
Use only cached URLs in building a certificate chain. The Internet and intranet are not searched for URL-based objects.


</td>
</tr>
</table>

## -remarks

Trust in a particular certificate being a trusted root is based on the current state of the root store and not the state of the root store at a time passed in by this parameter. For revocation, a certificate revocation list (CRL), itself, must be valid at the current time. The value of this parameter is used to determine whether a certificate listed in a CRL has been revoked.

The following remarks apply to strong signature checking:

<ul>
<li>You can enable strong signature checking by using the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_para">CERT_CHAIN_PARA</a> structure referenced by the <b>pChainPara</b> member. The <b>pStrongSignPara</b> member of the <b>CERT_CHAIN_PARA</b> structure points to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_strong_sign_para">CERT_STRONG_SIGN_PARA</a> structure that can be used to determine signature strength.</li>
<li>When you enable strong checking and a weak signature is encountered, the <b>CERT_TRUST_IS_NOT_SIGNATURE_VALID</b> and <b>CERT_TRUST_HAS_WEAK_SIGNATURE</b> errors are set in the <b>dwErrorStatus</b> field of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_trust_status">CERT_TRUST_STATUS</a> structure.</li>
</ul>