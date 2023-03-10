---
UID: NF:cryptdlg.CertModifyCertificatesToTrust
title: CertModifyCertificatesToTrust function (cryptdlg.h)
description: Modifies the set of certificates in a certificate trust list (CTL) for a given purpose.
helpviewer_keywords: ["CertModifyCertificatesToTrust","CertModifyCertificatesToTrust function [Security]","cryptdlg/CertModifyCertificatesToTrust","security.certmodifycertificatestotrust"]
old-location: security\certmodifycertificatestotrust.htm
tech.root: security
ms.assetid: a23d968e-113f-470e-a629-18c22882c77f
ms.date: 12/05/2018
ms.keywords: CertModifyCertificatesToTrust, CertModifyCertificatesToTrust function [Security], cryptdlg/CertModifyCertificatesToTrust, security.certmodifycertificatestotrust
req.header: cryptdlg.h
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
req.dll: CryptDlg.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CertModifyCertificatesToTrust
 - cryptdlg/CertModifyCertificatesToTrust
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - CryptDlg.dll
api_name:
 - CertModifyCertificatesToTrust
---

# CertModifyCertificatesToTrust function


## -description

The <b>CertModifyCertificatesToTrust</b> function  modifies the set of certificates in a certificate trust list (CTL) for a given purpose.
<div class="alert"><b>Note</b>  This function has no associated import library. You must use the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> functions to dynamically link to CryptDlg.dll.</div><div> </div>

## -parameters

### -param cCerts [in]

The number of modification requests that are in the <i>rgCerts</i> parameter.

### -param rgCerts [in]

A pointer to a <a href="/windows/desktop/api/cryptdlg/ns-cryptdlg-ctl_modify_request">CTL_MODIFY_REQUEST</a> structure that contains an array of modification requests.

### -param szPurpose [in]

A pointer to a null-terminated string that contains the string representation of an object identifier (OID). The OID specifies the enhanced key usage (EKU) of the CTL to be modified.

### -param hwnd [in]

A handle to the parent window of the dialog boxes that this function generates.

### -param hcertstoreTrust [in, optional]

A handle to the certificate store in which to modify the list of trusted certificates.  If <b>NULL</b>, the Trusted People store is used with the Current User location.

### -param pccertSigner [in, optional]

A pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure that contains a certificate. It is used to sign the trust list. The certificate also restricts the set of trust lists that may be modified. If <b>NULL</b>, the trust list is not signed.

## -returns

An <b>HRESULT</b>. A value of S_OK indicates success.

## -see-also

<a href="/windows/desktop/api/cryptdlg/ns-cryptdlg-ctl_modify_request">CTL_MODIFY_REQUEST</a>