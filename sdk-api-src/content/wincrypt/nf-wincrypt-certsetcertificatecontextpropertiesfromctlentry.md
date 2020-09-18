---
UID: NF:wincrypt.CertSetCertificateContextPropertiesFromCTLEntry
title: CertSetCertificateContextPropertiesFromCTLEntry function (wincrypt.h)
description: Sets the properties on the certificate context by using the attributes in the specified certificate trust list (CTL) entry.
helpviewer_keywords: ["CertSetCertificateContextPropertiesFromCTLEntry","CertSetCertificateContextPropertiesFromCTLEntry function [Security]","_crypto2_certsetcertificatecontextpropertiesfromctlentry","security.certsetcertificatecontextpropertiesfromctlentry","wincrypt/CertSetCertificateContextPropertiesFromCTLEntry"]
old-location: security\certsetcertificatecontextpropertiesfromctlentry.htm
tech.root: security
ms.assetid: b53b046a-68d4-4dc5-ab89-1b30ebd1de60
ms.date: 12/05/2018
ms.keywords: CertSetCertificateContextPropertiesFromCTLEntry, CertSetCertificateContextPropertiesFromCTLEntry function [Security], _crypto2_certsetcertificatecontextpropertiesfromctlentry, security.certsetcertificatecontextpropertiesfromctlentry, wincrypt/CertSetCertificateContextPropertiesFromCTLEntry
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
 - CertSetCertificateContextPropertiesFromCTLEntry
 - wincrypt/CertSetCertificateContextPropertiesFromCTLEntry
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
 - CertSetCertificateContextPropertiesFromCTLEntry
---

# CertSetCertificateContextPropertiesFromCTLEntry function


## -description

The <b>CertSetCertificateContextPropertiesFromCTLEntry</b> function sets the properties on the certificate context by using the attributes in the specified <a href="/windows/desktop/SecGloss/c-gly">certificate trust list</a> (CTL) entry.

## -parameters

### -param pCertContext [in]

A pointer to the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> whose attributes are to be set.

### -param pCtlEntry [in]

A pointer to the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_entry">CTL_ENTRY</a> structure used to set the attributes on the certificate.

### -param dwFlags [in]

 A <b>DWORD</b>. This parameter can be set to CERT_SET_PROPERTY_IGNORE_PERSIST_ERROR_FLAG to ignore any persisted error flags.

## -returns

If the function succeeds, the function returns nonzero.

  If the function fails, it returns zero.  For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_entry">CTL_ENTRY</a>



<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>