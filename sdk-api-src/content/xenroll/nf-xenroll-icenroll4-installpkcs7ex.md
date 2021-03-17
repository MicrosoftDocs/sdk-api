---
UID: NF:xenroll.ICEnroll4.InstallPKCS7Ex
title: ICEnroll4::InstallPKCS7Ex (xenroll.h)
description: Processes a certificate or chain of certificates, placing them into the appropriate certificate stores.InstallPKCS7 except that it returns the number of certificates actually installed in local stores.
helpviewer_keywords: ["CEnroll object [Security]","InstallPKCS7Ex method","ICEnroll4 interface [Security]","InstallPKCS7Ex method","ICEnroll4.InstallPKCS7Ex","ICEnroll4::InstallPKCS7Ex","InstallPKCS7Ex","InstallPKCS7Ex method [Security]","InstallPKCS7Ex method [Security]","CEnroll object","InstallPKCS7Ex method [Security]","ICEnroll4 interface","_xen_icenroll4_installpkcs7ex","security.icenroll4_installpkcs7ex","xenroll/ICEnroll4::InstallPKCS7Ex"]
old-location: security\icenroll4_installpkcs7ex.htm
tech.root: security
ms.assetid: 886fd5f0-d91f-439f-b259-dfb0206d3078
ms.date: 12/05/2018
ms.keywords: CEnroll object [Security],InstallPKCS7Ex method, ICEnroll4 interface [Security],InstallPKCS7Ex method, ICEnroll4.InstallPKCS7Ex, ICEnroll4::InstallPKCS7Ex, InstallPKCS7Ex, InstallPKCS7Ex method [Security], InstallPKCS7Ex method [Security],CEnroll object, InstallPKCS7Ex method [Security],ICEnroll4 interface, _xen_icenroll4_installpkcs7ex, security.icenroll4_installpkcs7ex, xenroll/ICEnroll4::InstallPKCS7Ex
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
 - ICEnroll4::InstallPKCS7Ex
 - xenroll/ICEnroll4::InstallPKCS7Ex
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
 - ICEnroll4.InstallPKCS7Ex
 - CEnroll.InstallPKCS7Ex
---

# ICEnroll4::InstallPKCS7Ex


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>InstallPKCS7Ex</b> method processes a certificate or chain of certificates, placing them into the appropriate <a href="/windows/desktop/SecGloss/c-gly">certificate stores</a>. The <b>InstallPKCS7Ex</b> method is the same as 
<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll3-installpkcs7">InstallPKCS7</a> except that it returns the number of certificates actually installed in local stores. This method was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll4">ICEnroll4</a> interface.

## -parameters

### -param PKCS7 [in]

A string that contains a certificate or chain of certificates.

### -param plCertInstalled [out]

Returns the number of certificates installed into local stores.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 A <b>Long</b> that contains the number of certificates installed into local stores.

## -remarks

When this method is called from script, the method displays a user interface that asks whether the user will allow installation of a  certificate.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/aa376007(v=vs.85)">CEnroll</a>



<a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll4">ICEnroll4</a>



<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll3-installpkcs7">InstallPKCS7</a>



<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll-acceptpkcs7">acceptPKCS7</a>