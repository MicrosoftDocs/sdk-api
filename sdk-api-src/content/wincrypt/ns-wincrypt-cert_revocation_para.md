---
UID: NS:wincrypt._CERT_REVOCATION_PARA
title: CERT_REVOCATION_PARA (wincrypt.h)
description: Is passed in calls to the CertVerifyRevocation function to assist in finding the issuer of the context to be verified.
helpviewer_keywords: ["*PCERT_REVOCATION_PARA","CERT_REVOCATION_PARA","CERT_REVOCATION_PARA structure [Security]","PCERT_REVOCATION_PARA","PCERT_REVOCATION_PARA structure pointer [Security]","_crypto2_cert_revocation_para","security.cert_revocation_para","wincrypt/CERT_REVOCATION_PARA","wincrypt/PCERT_REVOCATION_PARA"]
old-location: security\cert_revocation_para.htm
tech.root: security
ms.assetid: 730db593-c55f-4ecf-bcac-5de54ab90db6
ms.date: 12/05/2018
ms.keywords: '*PCERT_REVOCATION_PARA, CERT_REVOCATION_PARA, CERT_REVOCATION_PARA structure [Security], PCERT_REVOCATION_PARA, PCERT_REVOCATION_PARA structure pointer [Security], _crypto2_cert_revocation_para, security.cert_revocation_para, wincrypt/CERT_REVOCATION_PARA, wincrypt/PCERT_REVOCATION_PARA'
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
req.typenames: CERT_REVOCATION_PARA, *PCERT_REVOCATION_PARA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_REVOCATION_PARA
 - wincrypt/_CERT_REVOCATION_PARA
 - PCERT_REVOCATION_PARA
 - wincrypt/PCERT_REVOCATION_PARA
 - CERT_REVOCATION_PARA
 - wincrypt/CERT_REVOCATION_PARA
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
 - CERT_REVOCATION_PARA
---

# CERT_REVOCATION_PARA structure


## -description

The <b>CERT_REVOCATION_PARA</b> structure is passed in calls to 
the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifyrevocation">CertVerifyRevocation</a> function to assist in finding the issuer of the context to be verified. The <b>CERT_REVOCATION_PARA</b> structure is an optional parameter in the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifyrevocation">CertVerifyRevocation</a> function.

## -struct-fields

### -field cbSize

The size, in bytes, of this structure.

### -field pIssuerCert

A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure that contains the certificate of the issuer of a certificate specified in the <i>rgpvContext</i> array in the 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifyrevocation">CertVerifyRevocation</a> parameter list.

### -field cCertStore

When set, contains the number of elements in the <b>rgCertStore</b> array. Set to zero if you are not supplying  a list of store handles in the <i>rgCertStore</i> parameter.

### -field rgCertStore

An array of <a href="/windows/desktop/SecGloss/c-gly">certificate store</a> handles. Specifies a set of stores that are searched for issuer certificates.  If <i>rgCertStore</i> is not set, the default stores are searched.

### -field hCrlStore

Optional store handle. When specified, a handler that uses <a href="/windows/desktop/SecGloss/c-gly">certificate revocation lists</a> (CRLs) can search this store for CRLs.

### -field pftTimeToUse

A pointer to a <b>FILETIME</b> version of UTC time. When specified, the handler must, if possible, determine revocation status relative to the time given. If <b>NULL</b> or the handler cannot determine the status relative to the <b>pftTimeToUse</b> value, revocation status can be determined independent of time or relative to current time.

### -field dwUrlRetrievalTimeout

This member is defined only if <b>CERT_REVOCATION_PARA_HAS_EXTRA_FIELDS</b> is defined. The time-out, in milliseconds, that the revocation handler will wait when attempting to retrieve revocation information. If it is set to zero, the revocation handler's default time-out is used. If <b>CERT_REVOCATION_PARA_HAS_EXTRA_FIELDS</b> is defined, this member must be set to zero if it is unused.

### -field fCheckFreshnessTime

This member is defined only if <b>CERT_REVOCATION_PARA_HAS_EXTRA_FIELDS</b> is defined. If <b>TRUE</b>, an attempt is made to retrieve a new CRL if the issue date of the CRL is less than or equal to the Current Time minus <b>dwFreshnessTime</b>. If this flag is not set, the CRL's NextUpdate time is used. If <b>CERT_REVOCATION_PARA_HAS_EXTRA_FIELDS</b> is defined, this member must be set to <b>FALSE</b> if it is unused.

### -field dwFreshnessTime

This member is defined only if <b>CERT_REVOCATION_PARA_HAS_EXTRA_FIELDS</b> is defined. The time, in seconds, is used to determine whether an attempt will be made to retrieve a new CRL. If <b>CERT_REVOCATION_PARA_HAS_EXTRA_FIELDS</b> is defined, this member must be set to zero if it is unused.

### -field pftCurrentTime

This member is defined only if <b>CERT_REVOCATION_PARA_HAS_EXTRA_FIELDS</b> is defined. A pointer to a <b>FILETIME</b> structure that is used in the freshness time check. If the value of this pointer is null, the revocation handler uses the current time. If <b>CERT_REVOCATION_PARA_HAS_EXTRA_FIELDS</b> is defined, this member must be set to null if it is unused.

### -field pCrlInfo

This member is defined only if <b>CERT_REVOCATION_PARA_HAS_EXTRA_FIELDS</b> is defined.  This member contains a pointer to a PCERT_REVOCATION_CRL_INFO structure that contains CRL context information. The CRL information is only applicable to the last <a href="/windows/desktop/SecGloss/c-gly">context</a> checked. To access the information in this CRL, call the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifyrevocation">CertVerifyRevocation</a> function with <i>cContext</i> set to 1. If <b>CERT_REVOCATION_PARA_HAS_EXTRA_FIELDS</b> is defined, the member must be set to null if it is unused.

### -field pftCacheResync

This member is defined only if <b>CERT_REVOCATION_PARA_HAS_EXTRA_FIELDS</b> is defined. This member contains a pointer to a <b>FILETIME</b> structure that specifies the use of cached information. Any information cached  before the specified time is considered invalid and new information is retrieved. If <b>CERT_REVOCATION_PARA_HAS_EXTRA_FIELDS</b> is defined, this member must be set to null if it is unused.

<b>Windows Server 2003 and Windows XP:  </b>This member is not used.

### -field pChainPara

This member is defined only if <b>CERT_REVOCATION_PARA_HAS_EXTRA_FIELDS</b> is defined. This member contains a pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_revocation_chain_para">CERT_REVOCATION_CHAIN_PARA</a> structure that contains parameters used for building a chain for an independent OCSP signer certificate. If <b>CERT_REVOCATION_PARA_HAS_EXTRA_FIELDS</b> is defined, this member must be set to null if it is unused.

<b>Windows Vista, Windows Server 2003 and Windows XP:  </b>This member is not used in the listed systems. The member is available beginning with Windows Vista with SP1.

## -remarks

The <b>CERT_REVOCATION_PARA</b> structure provides additional information that the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifyrevocation">CertVerifyRevocation</a> function can use to determine the context issuer.

 If your application must check the freshness of the CRL or resynchronize the CRL cache, you can provide extra structure members to assist  the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifyrevocation">CertVerifyRevocation</a> function with this.  To include the additional structure members, define the constant <b>CERT_REVOCATION_PARA_HAS_EXTRA_FIELDS</b> in your application before including Wincrypt.h

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifyrevocation">CertVerifyRevocation</a>