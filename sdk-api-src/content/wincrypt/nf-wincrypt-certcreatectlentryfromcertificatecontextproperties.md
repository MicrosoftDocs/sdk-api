---
UID: NF:wincrypt.CertCreateCTLEntryFromCertificateContextProperties
title: CertCreateCTLEntryFromCertificateContextProperties function (wincrypt.h)
description: The CertCreateCTLEntryFromCertificateContextProperties function creates a certificate trust list (CTL) entry whose attributes are the properties of the certificate context. The SubjectIdentifier in the CTL entry is the SHA1 hash of the certificate.
helpviewer_keywords: ["CertCreateCTLEntryFromCertificateContextProperties","CertCreateCTLEntryFromCertificateContextProperties function [Security]","_crypto2_certcreatectlentryfromcertificatecontextproperties","security.certcreatectlentryfromcertificatecontextproperties","wincrypt/CertCreateCTLEntryFromCertificateContextProperties"]
old-location: security\certcreatectlentryfromcertificatecontextproperties.htm
tech.root: security
ms.assetid: 90ac512f-3cbe-4543-9b34-8e384f730cfe
ms.date: 12/05/2018
ms.keywords: CertCreateCTLEntryFromCertificateContextProperties, CertCreateCTLEntryFromCertificateContextProperties function [Security], _crypto2_certcreatectlentryfromcertificatecontextproperties, security.certcreatectlentryfromcertificatecontextproperties, wincrypt/CertCreateCTLEntryFromCertificateContextProperties
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
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CertCreateCTLEntryFromCertificateContextProperties
 - wincrypt/CertCreateCTLEntryFromCertificateContextProperties
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CertCreateCTLEntryFromCertificateContextProperties
---

# CertCreateCTLEntryFromCertificateContextProperties function


## -description

The <b>CertCreateCTLEntryFromCertificateContextProperties</b> function creates a <a href="/windows/desktop/SecGloss/c-gly">certificate trust list</a> (CTL) entry whose attributes are the  properties of the certificate context. The SubjectIdentifier in the CTL entry is the SHA1 hash of the certificate.

The certificate properties are added as attributes. The property attribute OID is the decimal PROP_ID preceded by szOID_CERT_PROP_ID_PREFIX. Each property value is copied as a single attribute value.

Additional attributes can be included in the CTL entry by using the <i>cOptAttr</i> and <i>rgOptAttr</i> parameters.

## -parameters

### -param pCertContext [in]

A pointer to the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> used to create the CTL.

### -param cOptAttr [in]

A <b>DWORD</b> that specifies the number of additional attributes to be added.

### -param rgOptAttr [in]

A pointer to any array of <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_attribute">CRYPT_ATTRIBUTE</a> attributes to be added to the CTL.

### -param dwFlags [in]

A <b>DWORD</b>. Can be set to CTL_ENTRY_FROM_PROP_CHAIN_FLAG to force the inclusion of the chain building hash properties as attributes.

### -param pvReserved [in]

A pointer to a <b>VOID</b>. Reserved for future use.

### -param pCtlEntry [out]

Address of a pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_entry">CTL_ENTRY</a> structure. Call this function twice to retrieve a CTL entry. Set this parameter to <b>NULL</b> on the first call. When the function returns, use the number of bytes retrieved from the <i>pcbCtlEntry</i> parameter to allocate memory. Call the function again, setting this parameter to the address of the allocated memory.

### -param pcbCtlEntry [in, out]

 Pointer to a <b>DWORD</b> that contains the number of bytes that must be allocated for the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_entry">CTL_ENTRY</a> structure.  Call this function twice to retrieve the number of bytes. For the first call, set this parameter to the address of a <b>DWORD</b> value that contains zero and set the <i>pCtlEntry</i> parameter to <b>NULL</b>. If the first call succeeds, the <b>DWORD</b> value will contain the number of bytes that you must allocate for the <b>CTL_ENTRY</b> structure. Allocate the required memory and call the function again, supplying the address of the memory in the <i>pCtlEntry</i> parameter.

## -returns

If the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns  zero (<b>FALSE</b>). For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.