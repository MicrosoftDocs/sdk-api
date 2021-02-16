---
UID: NF:xenroll.ICEnroll.getCertFromPKCS7
title: ICEnroll::getCertFromPKCS7 (xenroll.h)
description: Retrieves the certificate, contained in a PKCS
helpviewer_keywords: ["CEnroll object [Security]","getCertFromPKCS7 method","ICEnroll interface [Security]","getCertFromPKCS7 method","ICEnroll.getCertFromPKCS7","ICEnroll2 interface [Security]","getCertFromPKCS7 method","ICEnroll2::getCertFromPKCS7","ICEnroll3 interface [Security]","getCertFromPKCS7 method","ICEnroll3::getCertFromPKCS7","ICEnroll4 interface [Security]","getCertFromPKCS7 method","ICEnroll4::getCertFromPKCS7","ICEnroll::getCertFromPKCS7","getCertFromPKCS7","getCertFromPKCS7 method [Security]","getCertFromPKCS7 method [Security]","CEnroll object","getCertFromPKCS7 method [Security]","ICEnroll interface","getCertFromPKCS7 method [Security]","ICEnroll2 interface","getCertFromPKCS7 method [Security]","ICEnroll3 interface","getCertFromPKCS7 method [Security]","ICEnroll4 interface","security.icenroll4_getcertfrompkcs7","xenroll/ICEnroll2::getCertFromPKCS7","xenroll/ICEnroll3::getCertFromPKCS7","xenroll/ICEnroll4::getCertFromPKCS7","xenroll/ICEnroll::getCertFromPKCS7"]
old-location: security\icenroll4_getcertfrompkcs7.htm
tech.root: security
ms.assetid: 3094cd58-d123-40f1-ac81-dffdfb56d47d
ms.date: 12/05/2018
ms.keywords: CEnroll object [Security],getCertFromPKCS7 method, ICEnroll interface [Security],getCertFromPKCS7 method, ICEnroll.getCertFromPKCS7, ICEnroll2 interface [Security],getCertFromPKCS7 method, ICEnroll2::getCertFromPKCS7, ICEnroll3 interface [Security],getCertFromPKCS7 method, ICEnroll3::getCertFromPKCS7, ICEnroll4 interface [Security],getCertFromPKCS7 method, ICEnroll4::getCertFromPKCS7, ICEnroll::getCertFromPKCS7, getCertFromPKCS7, getCertFromPKCS7 method [Security], getCertFromPKCS7 method [Security],CEnroll object, getCertFromPKCS7 method [Security],ICEnroll interface, getCertFromPKCS7 method [Security],ICEnroll2 interface, getCertFromPKCS7 method [Security],ICEnroll3 interface, getCertFromPKCS7 method [Security],ICEnroll4 interface, security.icenroll4_getcertfrompkcs7, xenroll/ICEnroll2::getCertFromPKCS7, xenroll/ICEnroll3::getCertFromPKCS7, xenroll/ICEnroll4::getCertFromPKCS7, xenroll/ICEnroll::getCertFromPKCS7
req.header: xenroll.h
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
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICEnroll::getCertFromPKCS7
 - xenroll/ICEnroll::getCertFromPKCS7
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Xenroll.dll
api_name:
 - ICEnroll4.getCertFromPKCS7
 - ICEnroll3.getCertFromPKCS7
 - ICEnroll2.getCertFromPKCS7
 - ICEnroll.getCertFromPKCS7
 - CEnroll.getCertFromPKCS7
---

# ICEnroll::getCertFromPKCS7


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>getCertFromPKCS7</b> method retrieves the certificate, contained in a PKCS #7 message, that was  issued in response to a PKCS #10 certificate request. This method was first defined by the <a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a> interface.

This method retrieves the single certificate that was issued even though a PKCS #7 message may contain many certificates that specify the certification chain of authority that issued the certificate.

## -parameters

### -param wszPKCS7 [in]

Specifies the PKCS #7 from which the issued certificate is being retrieved.

### -param pbstrCert [out]

A pointer to a <b>BSTR</b> variable to receive the issued certificate. When you have finished using the <b>BSTR</b>, free it by calling the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 The string that contains the issued certificate.