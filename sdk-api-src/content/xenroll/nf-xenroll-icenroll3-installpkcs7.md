---
UID: NF:xenroll.ICEnroll3.InstallPKCS7
title: ICEnroll3::InstallPKCS7 (xenroll.h)
description: Processes a certificate or chain of certificates, placing them into the appropriate certificate stores. This method differs from the acceptPKCS7 method in that InstallPKCS7 does not receive a request certificate.
helpviewer_keywords: ["CEnroll object [Security]","InstallPKCS7 method","ICEnroll3 interface [Security]","InstallPKCS7 method","ICEnroll3.InstallPKCS7","ICEnroll3::InstallPKCS7","ICEnroll4 interface [Security]","InstallPKCS7 method","ICEnroll4::InstallPKCS7","InstallPKCS7","InstallPKCS7 method [Security]","InstallPKCS7 method [Security]","CEnroll object","InstallPKCS7 method [Security]","ICEnroll3 interface","InstallPKCS7 method [Security]","ICEnroll4 interface","security.icenroll4_installpkcs7","xenroll/ICEnroll3::InstallPKCS7","xenroll/ICEnroll4::InstallPKCS7"]
old-location: security\icenroll4_installpkcs7.htm
tech.root: security
ms.assetid: 63482360-0d8a-4e23-8942-8276630778a3
ms.date: 12/05/2018
ms.keywords: CEnroll object [Security],InstallPKCS7 method, ICEnroll3 interface [Security],InstallPKCS7 method, ICEnroll3.InstallPKCS7, ICEnroll3::InstallPKCS7, ICEnroll4 interface [Security],InstallPKCS7 method, ICEnroll4::InstallPKCS7, InstallPKCS7, InstallPKCS7 method [Security], InstallPKCS7 method [Security],CEnroll object, InstallPKCS7 method [Security],ICEnroll3 interface, InstallPKCS7 method [Security],ICEnroll4 interface, security.icenroll4_installpkcs7, xenroll/ICEnroll3::InstallPKCS7, xenroll/ICEnroll4::InstallPKCS7
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
 - ICEnroll3::InstallPKCS7
 - xenroll/ICEnroll3::InstallPKCS7
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
 - ICEnroll4.InstallPKCS7
 - ICEnroll3.InstallPKCS7
 - CEnroll.InstallPKCS7
---

# ICEnroll3::InstallPKCS7


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>InstallPKCS7</b> method processes a certificate or chain of certificates, placing them into the appropriate <a href="/windows/desktop/SecGloss/c-gly">certificate stores</a>. This method differs from the  <a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll-acceptpkcs7">acceptPKCS7</a> method in that  <b>InstallPKCS7</b> does not receive a request certificate. This method was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll3">ICEnroll3</a> interface.

## -parameters

### -param PKCS7 [in]

A string that contains a certificate or chain of certificates.

## -returns

<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

When this method is called from script, the method displays a user interface that asks whether the user will allow installation of a  certificate.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/aa376007(v=vs.85)">CEnroll</a>



<a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll3">ICEnroll3</a>



<a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll4">ICEnroll4</a>



<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll-acceptpkcs7">ICEnroll::acceptPKCS7</a>