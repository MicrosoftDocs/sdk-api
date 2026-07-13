---
UID: NC:cryptdlg.PFNCMFILTERPROC
title: PFNCMFILTERPROC (cryptdlg.h)
description: Filters each certificate to determine whether it will appear in the certificate selection dialog box that is displayed by the CertSelectCertificate function.
helpviewer_keywords: ["PFNCMFILTERPROC","PFNCMFILTERPROC callback","PFNCMFILTERPROC callback function [Security]","cryptdlg/PFNCMFILTERPROC","security.pfncmfilterproc"]
old-location: security\pfncmfilterproc.htm
tech.root: security
ms.assetid: f870a8a7-c504-491a-b9ac-045766e46348
ms.date: 03/22/2023
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

The **PFNCMFILTERPROC** function is a filter procedure that filters each certificate to determine whether it will appear in the certificate selection dialog box that is displayed by the [CertSelectCertificate](nf-cryptdlg-certselectcertificatea.md) function. **PFNCMFILTERPROC** is an application-defined callback function that is specified in the [CERT_SELECT_STRUCT](ns-cryptdlg-cert_select_struct_a.md) structure. The **CERT_SELECT_STRUCT** structure is a parameter in the [CertSelectCertificate](nf-cryptdlg-certselectcertificatea.md) function. The **PFNCMFILTERPROC** function must be implemented by the developer to suit each application.

## -parameters

### -param pCertContext

A pointer to a [CERT_CONTEXT](/windows/win32/api/wincrypt/ns-wincrypt-cert_context) structure that contains a certificate on which to make a filtering determination.

### -param unnamedParam2

*dwDisplayWell*. Reserved for future use.

### -param unnamedParam3

This `DWORD` parameter is *dwFlags*.

### -param unnamedParam4

This `DWORD` parameter is *lCustData*. It is the address of an array of byte values that holds custom data. *lCustData* is passed to the **PFNCMFILTERPROC** function by the [CertSelectCertificate](nf-cryptdlg-certselectcertificatea.md) function.

## -returns

Return a nonzero value (**TRUE**) to display the certificate. Return zero (**FALSE**) to not display the certificate.

## -remarks

## -see-also

[CERT_SELECT_STRUCT](ns-cryptdlg-cert_select_struct_a.md)

[CertSelectCertificate](nf-cryptdlg-certselectcertificatea.md)
