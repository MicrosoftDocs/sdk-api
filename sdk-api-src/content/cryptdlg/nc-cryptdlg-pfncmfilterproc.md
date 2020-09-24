---
UID: NC:cryptdlg.PFNCMFILTERPROC
title: PFNCMFILTERPROC (cryptdlg.h)
description: Filters each certificate to determine whether it will appear in the certificate selection dialog box that is displayed by the CertSelectCertificate function.
helpviewer_keywords: ["PFNCMFILTERPROC","PFNCMFILTERPROC callback","PFNCMFILTERPROC callback function [Security]","cryptdlg/PFNCMFILTERPROC","security.pfncmfilterproc"]
old-location: security\pfncmfilterproc.htm
tech.root: security
ms.assetid: f870a8a7-c504-491a-b9ac-045766e46348
ms.date: 12/05/2018
ms.keywords: PFNCMFILTERPROC, PFNCMFILTERPROC callback, PFNCMFILTERPROC callback function [Security], cryptdlg/PFNCMFILTERPROC, security.pfncmfilterproc
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PFNCMFILTERPROC
 - cryptdlg/PFNCMFILTERPROC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - CryptDlg.h
api_name:
 - PFNCMFILTERPROC
---

## -description

The <b>PFNCMFILTERPROC</b> function is a filter procedure that filters each certificate to determine whether it will appear in the certificate selection dialog box that is displayed by the <a href="/windows/desktop/api/cryptdlg/nf-cryptdlg-certselectcertificatea">CertSelectCertificate</a> function. <b>PFNCMFILTERPROC</b> is an application-defined callback function that is specified in the <a href="/windows/win32/api/cryptdlg/ns-cryptdlg-cert_select_struct_a">CERT_SELECT_STRUCT</a> structure. The <b>CERT_SELECT_STRUCT</b> structure is a parameter in the <a href="/windows/desktop/api/cryptdlg/nf-cryptdlg-certselectcertificatea">CertSelectCertificate</a> function. The <b>PFNCMFILTERPROC</b> function must be implemented by the developer to suit each application.

## -parameters

### -param pCertContext [in]

A pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure that contains a certificate on which to make a filtering determination.

### -param LPARAM

*dwDisplayWell*. Reserved for future use.

### -param DWORD

See **Remarks**.

## -returns

Return a nonzero value (<b>TRUE</b>) to display the certificate. Return zero (<b>FALSE</b>) to not display the certificate.

## -remarks

The first **DWORD** parameter is *dwFlags*. The second is *lCustData*&mdash;the address of an array of byte values that holds custom data. <i>lCustData</i> is passed to the <b>PFNCMFILTERPROC</b> function by the <a href="/windows/desktop/api/cryptdlg/nf-cryptdlg-certselectcertificatea">CertSelectCertificate</a> function.

## -see-also

<a href="/windows/win32/api/cryptdlg/ns-cryptdlg-cert_select_struct_a">CERT_SELECT_STRUCT</a>

<a href="/windows/desktop/api/cryptdlg/nf-cryptdlg-certselectcertificatea">CertSelectCertificate</a>