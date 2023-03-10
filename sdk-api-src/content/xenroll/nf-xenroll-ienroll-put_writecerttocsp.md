---
UID: NF:xenroll.IEnroll.put_WriteCertToCSP
title: IEnroll::put_WriteCertToCSP (xenroll.h)
description: Sets or retrieves a Boolean value that determines whether a certificate should be written to the cryptographic service provider (CSP). (Put)
helpviewer_keywords: ["IEnroll interface [Security]","WriteCertToCSP property","IEnroll.WriteCertToCSP","IEnroll.put_WriteCertToCSP","IEnroll::WriteCertToCSP","IEnroll::get_WriteCertToCSP","IEnroll::put_WriteCertToCSP","WriteCertToCSP property [Security]","WriteCertToCSP property [Security]","IEnroll interface","put_WriteCertToCSP","security.ienroll4_writecerttocsp","xenroll/IEnroll::WriteCertToCSP","xenroll/IEnroll::get_WriteCertToCSP","xenroll/IEnroll::put_WriteCertToCSP"]
old-location: security\ienroll4_writecerttocsp.htm
tech.root: security
ms.assetid: 07463f0d-f46c-4bc3-8170-0a480b826049
ms.date: 12/05/2018
ms.keywords: IEnroll interface [Security],WriteCertToCSP property, IEnroll.WriteCertToCSP, IEnroll.put_WriteCertToCSP, IEnroll::WriteCertToCSP, IEnroll::get_WriteCertToCSP, IEnroll::put_WriteCertToCSP, WriteCertToCSP property [Security], WriteCertToCSP property [Security],IEnroll interface, put_WriteCertToCSP, security.ienroll4_writecerttocsp, xenroll/IEnroll::WriteCertToCSP, xenroll/IEnroll::get_WriteCertToCSP, xenroll/IEnroll::put_WriteCertToCSP
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
 - IEnroll::put_WriteCertToCSP
 - xenroll/IEnroll::put_WriteCertToCSP
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
 - IEnroll.WriteCertToCSP
 - IEnroll.get_WriteCertToCSP
 - IEnroll.put_WriteCertToCSP
---

# IEnroll::put_WriteCertToCSP


## -description

<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>WriteCertToCSP</b> property sets or retrieves a Boolean value that determines whether a certificate should be written to the <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP).

This property was first defined by the <a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll">IEnroll</a> interface.

This property is read/write.

## -parameters

## -remarks

This property is typically used with smart cards, where the certificate is written to the smart card in addition to being written to the "MY" store.

The default value is <b>true</b>, which means that the Certificate Enrollment Control will try to write the certificate to the CSP but will not fail unless a hardware token error is encountered. If this value is <b>true</b>, but no smart card or other hardware-dependent CSP is installed, then hardware token errors will be ignored.

To explicitly force that the Certificate Enrollment Control not attempt to write to the CSP, set this value to false.


<b>WriteCertToCSP</b> affects the behavior of the following methods:

<ul>
<li>
<a href="/windows/desktop/api/xenroll/nf-xenroll-ienroll-acceptpkcs7blob">acceptPKCS7Blob</a>
</li>
<li>
<a href="/windows/desktop/api/xenroll/nf-xenroll-ienroll-acceptfilepkcs7wstr">acceptFilePKCS7WStr</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll</a>
