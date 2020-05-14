---
UID: NF:cryptdlg.CertSelectCertificateA
title: CertSelectCertificateA function (cryptdlg.h)
description: Presents a dialog box that allows the user to select certificates from a set of certificates that match the given criteria.
helpviewer_keywords: ["CertSelectCertificate","CertSelectCertificate function [Security]","CertSelectCertificateA","CertSelectCertificateW","cryptdlg/CertSelectCertificate","cryptdlg/CertSelectCertificateA","cryptdlg/CertSelectCertificateW","security.certselectcertificate"]
old-location: security\certselectcertificate.htm
tech.root: SecCrypto
ms.assetid: 8160ea08-c7c0-40f5-8771-6603f768744b
ms.date: 12/05/2018
ms.keywords: CertSelectCertificate, CertSelectCertificate function [Security], CertSelectCertificateA, CertSelectCertificateW, cryptdlg/CertSelectCertificate, cryptdlg/CertSelectCertificateA, cryptdlg/CertSelectCertificateW, security.certselectcertificate
f1_keywords:
- cryptdlg/CertSelectCertificate
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- CryptDlg.dll
api_name:
- CertSelectCertificate
- CertSelectCertificateA
- CertSelectCertificateW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CertSelectCertificateA function


## -description


The <b>CertSelectCertificate</b> function  presents a dialog box that allows the user to select certificates from a set of certificates that match the given criteria.
<div class="alert"><b>Note</b>  This function has no associated import library. You must use the <a href="https://docs.microsoft.com/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="https://docs.microsoft.com/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> functions to dynamically link to CryptDlg.dll.</div><div> </div>

## -parameters




### -param pCertSelectInfo [in, out]

A pointer to a <a href="/windows/win32/api/cryptdlg/ns-cryptdlg-cert_select_struct_a">CERT_SELECT_STRUCT</a> structure that contains criteria that control the displayed certificates for selection and receives the selected certificate.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. For extended error information, call the 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.




## -see-also




<a href="/windows/win32/api/cryptdlg/ns-cryptdlg-cert_select_struct_a">CERT_SELECT_STRUCT</a>
 

 

