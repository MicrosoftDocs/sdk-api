---
UID: NF:xenroll.IEnroll.acceptFilePKCS7WStr
title: IEnroll::acceptFilePKCS7WStr (xenroll.h)
description: Accepts and processes a PKCS (IEnroll.acceptFilePKCS7WStr)
helpviewer_keywords: ["IEnroll interface [Security]","acceptFilePKCS7WStr method","IEnroll.acceptFilePKCS7WStr","IEnroll::acceptFilePKCS7WStr","acceptFilePKCS7WStr","acceptFilePKCS7WStr method [Security]","acceptFilePKCS7WStr method [Security]","IEnroll interface","security.ienroll4_acceptfilepkcs7wstr","xenroll/IEnroll::acceptFilePKCS7WStr"]
old-location: security\ienroll4_acceptfilepkcs7wstr.htm
tech.root: security
ms.assetid: 9c2b99df-769b-457b-b5c5-7690b73d6f84
ms.date: 12/05/2018
ms.keywords: IEnroll interface [Security],acceptFilePKCS7WStr method, IEnroll.acceptFilePKCS7WStr, IEnroll::acceptFilePKCS7WStr, acceptFilePKCS7WStr, acceptFilePKCS7WStr method [Security], acceptFilePKCS7WStr method [Security],IEnroll interface, security.ienroll4_acceptfilepkcs7wstr, xenroll/IEnroll::acceptFilePKCS7WStr
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
 - IEnroll::acceptFilePKCS7WStr
 - xenroll/IEnroll::acceptFilePKCS7WStr
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
 - IEnroll.acceptFilePKCS7WStr
---

# IEnroll::acceptFilePKCS7WStr


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>acceptFilePKCS7WStr</b> method  accepts and processes a PKCS #7 message containing a certificate, then stores the message to a file. This method was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll">IEnroll</a> interface.

## -parameters

### -param wszPKCS7FileName [in]

Specifies the name of the file containing the PKCS #7.

## -returns

The return value is an <b>HRESULT</b>. A value of S_OK indicates success. Upon successful completion of this function, the PKCS #7 in the file will be accepted.

## -remarks

By default, the MY, CA, ROOT, and REQUEST system stores are used to store the certificates. However, you can specify other stores by assigning the following properties before calling this method:

<ul>
<li>
<a href="/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_mystorenamewstr">MyStoreNameWStr</a>
</li>
<li>
<a href="/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_castorenamewstr">CAStoreNameWStr</a>
</li>
<li>
<a href="/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_rootstorenamewstr">RootStoreNameWStr</a>
</li>
<li>
<a href="/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_requeststorenamewstr">RequestStoreNameWStr</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll</a>
