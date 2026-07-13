---
UID: NF:xenroll.ICEnroll.acceptPKCS7
title: ICEnroll::acceptPKCS7 (xenroll.h)
description: Accepts and processes a PKCS (ICEnroll.acceptPKCS7)
helpviewer_keywords: ["CEnroll object [Security]","acceptPKCS7 method","ICEnroll interface [Security]","acceptPKCS7 method","ICEnroll.acceptPKCS7","ICEnroll2 interface [Security]","acceptPKCS7 method","ICEnroll2::acceptPKCS7","ICEnroll3 interface [Security]","acceptPKCS7 method","ICEnroll3::acceptPKCS7","ICEnroll4 interface [Security]","acceptPKCS7 method","ICEnroll4::acceptPKCS7","ICEnroll::acceptPKCS7","acceptPKCS7","acceptPKCS7 method [Security]","acceptPKCS7 method [Security]","CEnroll object","acceptPKCS7 method [Security]","ICEnroll interface","acceptPKCS7 method [Security]","ICEnroll2 interface","acceptPKCS7 method [Security]","ICEnroll3 interface","acceptPKCS7 method [Security]","ICEnroll4 interface","security.icenroll4_acceptpkcs7","xenroll/ICEnroll2::acceptPKCS7","xenroll/ICEnroll3::acceptPKCS7","xenroll/ICEnroll4::acceptPKCS7","xenroll/ICEnroll::acceptPKCS7"]
old-location: security\icenroll4_acceptpkcs7.htm
tech.root: security
ms.assetid: 5a428d83-c846-4f44-a682-58c3e025c353
ms.date: 12/05/2018
ms.keywords: CEnroll object [Security],acceptPKCS7 method, ICEnroll interface [Security],acceptPKCS7 method, ICEnroll.acceptPKCS7, ICEnroll2 interface [Security],acceptPKCS7 method, ICEnroll2::acceptPKCS7, ICEnroll3 interface [Security],acceptPKCS7 method, ICEnroll3::acceptPKCS7, ICEnroll4 interface [Security],acceptPKCS7 method, ICEnroll4::acceptPKCS7, ICEnroll::acceptPKCS7, acceptPKCS7, acceptPKCS7 method [Security], acceptPKCS7 method [Security],CEnroll object, acceptPKCS7 method [Security],ICEnroll interface, acceptPKCS7 method [Security],ICEnroll2 interface, acceptPKCS7 method [Security],ICEnroll3 interface, acceptPKCS7 method [Security],ICEnroll4 interface, security.icenroll4_acceptpkcs7, xenroll/ICEnroll2::acceptPKCS7, xenroll/ICEnroll3::acceptPKCS7, xenroll/ICEnroll4::acceptPKCS7, xenroll/ICEnroll::acceptPKCS7
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
 - ICEnroll::acceptPKCS7
 - xenroll/ICEnroll::acceptPKCS7
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
 - ICEnroll4.acceptPKCS7
 - ICEnroll3.acceptPKCS7
 - ICEnroll2.acceptPKCS7
 - ICEnroll.acceptPKCS7
 - CEnroll.acceptPKCS7
---

# ICEnroll::acceptPKCS7


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>acceptPKCS7</b> method accepts and processes a PKCS #7 message that contains a certificate. The PKCS #7 is input as a parameter. This method was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a> interface.

## -parameters

### -param PKCS7 [in]

Represents the base64-encoded PKCS #7 that contains the certificate and the chain of certificates that identifies the issuer.

## -returns

<h3>VB</h3>
The return value is an <b>HRESULT</b>. A value of S_OK indicates success. Upon successful completion of this function, the PKCS #7 will be accepted.

## -remarks

The PKCS #7 input as a parameter for <b>acceptPKCS7</b> contains the request certificate and the chain of certificates identifying the issuer of the certificate. Typically, but not always, the chain of certificates does not include the root. The PKCS #7 can be in base64-encoded, binary, or <a href="/windows/desktop/SecGloss/x-gly">X.509</a> certificate format (with or without the begin cert / end cert tags). The certificate and the associated keys generated for it are put in the MY store. A <a href="/windows/desktop/SecGloss/r-gly">root certificate</a> is placed in the ROOT store and the rest of the chain of certificates are placed in the <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA) store. If any ROOT certificates found in the PKCS #7 are accepted, Crypt32 will notify the user that a ROOT certificate is being added to his store. The user has the option of declining the ROOT certificate. This option is provided so that the user can decline to place an untrusted root in the ROOT store. Declining to place the ROOT in the ROOT store will not cause Certificate Enrollment Control to fail acceptance.


By default, the system stores MY, CA, ROOT, and REQUEST are used to store the certificates. However, you can specify other stores by assigning the following properties before calling this method:

<ul>
<li>
<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_mystorename">MyStoreName</a>
</li>
<li>
<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_castorename">CAStoreName</a>
</li>
<li>
<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_rootstorename">RootStoreName</a>
</li>
<li>
<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_requeststorename">RequestStoreName</a>
</li>
</ul>


When this method is called from script, the method displays a user interface that asks whether the user will allow installation of a  certificate.

## -see-also

<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_castorename">CAStoreName</a>



<a href="/previous-versions/windows/desktop/legacy/aa376007(v=vs.85)">CEnroll</a>



<a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>



<a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll2">ICEnroll2</a>



<a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll3">ICEnroll3</a>



<a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll4">ICEnroll4</a>



<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_mystorename">MyStoreName</a>



<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_requeststorename">RequestStoreName</a>



<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_rootstorename">RootStoreName</a>



<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll-acceptfilepkcs7">acceptFilePKCS7</a>
