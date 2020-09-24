---
UID: NF:xenroll.ICEnroll.acceptFilePKCS7
title: ICEnroll::acceptFilePKCS7 (xenroll.h)
description: Accepts and processes a file that contains a PKCS
helpviewer_keywords: ["CEnroll object [Security]","acceptFilePKCS7 method","ICEnroll interface [Security]","acceptFilePKCS7 method","ICEnroll.acceptFilePKCS7","ICEnroll2 interface [Security]","acceptFilePKCS7 method","ICEnroll2::acceptFilePKCS7","ICEnroll3 interface [Security]","acceptFilePKCS7 method","ICEnroll3::acceptFilePKCS7","ICEnroll4 interface [Security]","acceptFilePKCS7 method","ICEnroll4::acceptFilePKCS7","ICEnroll::acceptFilePKCS7","acceptFilePKCS7","acceptFilePKCS7 method [Security]","acceptFilePKCS7 method [Security]","CEnroll object","acceptFilePKCS7 method [Security]","ICEnroll interface","acceptFilePKCS7 method [Security]","ICEnroll2 interface","acceptFilePKCS7 method [Security]","ICEnroll3 interface","acceptFilePKCS7 method [Security]","ICEnroll4 interface","security.icenroll4_acceptfilepkcs7","xenroll/ICEnroll2::acceptFilePKCS7","xenroll/ICEnroll3::acceptFilePKCS7","xenroll/ICEnroll4::acceptFilePKCS7","xenroll/ICEnroll::acceptFilePKCS7"]
old-location: security\icenroll4_acceptfilepkcs7.htm
tech.root: security
ms.assetid: dae9f6b8-6690-47cc-9397-168c1ff54c55
ms.date: 12/05/2018
ms.keywords: CEnroll object [Security],acceptFilePKCS7 method, ICEnroll interface [Security],acceptFilePKCS7 method, ICEnroll.acceptFilePKCS7, ICEnroll2 interface [Security],acceptFilePKCS7 method, ICEnroll2::acceptFilePKCS7, ICEnroll3 interface [Security],acceptFilePKCS7 method, ICEnroll3::acceptFilePKCS7, ICEnroll4 interface [Security],acceptFilePKCS7 method, ICEnroll4::acceptFilePKCS7, ICEnroll::acceptFilePKCS7, acceptFilePKCS7, acceptFilePKCS7 method [Security], acceptFilePKCS7 method [Security],CEnroll object, acceptFilePKCS7 method [Security],ICEnroll interface, acceptFilePKCS7 method [Security],ICEnroll2 interface, acceptFilePKCS7 method [Security],ICEnroll3 interface, acceptFilePKCS7 method [Security],ICEnroll4 interface, security.icenroll4_acceptfilepkcs7, xenroll/ICEnroll2::acceptFilePKCS7, xenroll/ICEnroll3::acceptFilePKCS7, xenroll/ICEnroll4::acceptFilePKCS7, xenroll/ICEnroll::acceptFilePKCS7
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
 - ICEnroll::acceptFilePKCS7
 - xenroll/ICEnroll::acceptFilePKCS7
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
 - ICEnroll4.acceptFilePKCS7
 - ICEnroll3.acceptFilePKCS7
 - ICEnroll2.acceptFilePKCS7
 - ICEnroll.acceptFilePKCS7
 - CEnroll.acceptFilePKCS7
---

# ICEnroll::acceptFilePKCS7


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>acceptFilePKCS7</b> method accepts and processes a file that contains a PKCS #7 message containing a certificate. This method was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a> interface.

## -parameters

### -param wszPKCS7FileName [in]

Specifies the name of the file that contains the PKCS #7 message.

## -returns

<h3>VB</h3>
The return value is an <b>HRESULT</b>. A value of S_OK indicates success. Upon successful completion of this function, the PKCS #7 message in the file will be accepted.

## -remarks

By default, the My, Ca, Root, and Request system stores are used to store the certificates. However, you can specify other stores by assigning the following properties before calling this method:

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


The <b>acceptFilePKCS7</b> method differs from 
<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll-acceptpkcs7">acceptPKCS7</a> only in that a file supplies the certificate.


#### Examples


```cpp
HRESULT  hr;
BSTR     bstrFileName;

// Allocate a BSTR referencing an existing file, 
// for example, "myPKCS7.fil".
bstrFileName = SysAllocString(TEXT("<FILENAMEHERE>"));
if (NULL == bstrFileName)
{
    //handle error
}

// pEnroll is a previously instantiated ICEnroll interface pointer.
hr = pEnroll->acceptFilePKCS7( bstrFileName );
if (FAILED(hr))
    printf("Failed acceptFilePKCS7 - %x\n", hr );
else
	printf("Accepted PKCS #7 from file %ws successfully\n", 
	bstrFileName );

// Free BSTR when done.
if (bstrFileName)
    SysFreeString(bstrFileName);
```

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



<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll-acceptpkcs7">acceptPKCS7</a>