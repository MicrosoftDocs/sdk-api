---
UID: NF:xenroll.ICEnroll4.getCertFromFileResponse
title: ICEnroll4::getCertFromFileResponse (xenroll.h)
description: Retrieves the certificate from a file containing a response from a certification authority. This method was first defined in the ICEnroll4 interface.
helpviewer_keywords: ["CEnroll object [Security]","getCertFromFileResponse method","ICEnroll4 interface [Security]","getCertFromFileResponse method","ICEnroll4.getCertFromFileResponse","ICEnroll4::getCertFromFileResponse","_xen_icenroll4_getcertfromfileresponse","getCertFromFileResponse","getCertFromFileResponse method [Security]","getCertFromFileResponse method [Security]","CEnroll object","getCertFromFileResponse method [Security]","ICEnroll4 interface","security.icenroll4_getcertfromfileresponse","xenroll/ICEnroll4::getCertFromFileResponse"]
old-location: security\icenroll4_getcertfromfileresponse.htm
tech.root: security
ms.assetid: 0e89465b-4525-4b36-b0c7-7f34dc4a34aa
ms.date: 12/05/2018
ms.keywords: CEnroll object [Security],getCertFromFileResponse method, ICEnroll4 interface [Security],getCertFromFileResponse method, ICEnroll4.getCertFromFileResponse, ICEnroll4::getCertFromFileResponse, _xen_icenroll4_getcertfromfileresponse, getCertFromFileResponse, getCertFromFileResponse method [Security], getCertFromFileResponse method [Security],CEnroll object, getCertFromFileResponse method [Security],ICEnroll4 interface, security.icenroll4_getcertfromfileresponse, xenroll/ICEnroll4::getCertFromFileResponse
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
 - ICEnroll4::getCertFromFileResponse
 - xenroll/ICEnroll4::getCertFromFileResponse
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
 - ICEnroll4.getCertFromFileResponse
 - CEnroll.getCertFromFileResponse
---

# ICEnroll4::getCertFromFileResponse


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>getCertFromFileResponse</b> method retrieves the certificate from a file containing a response from a <a href="/windows/desktop/SecGloss/c-gly">certification authority</a>.
			 This method was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll4">ICEnroll4</a> interface.

## -parameters

### -param strResponseFileName [in]

Specifies the name of the file that contains the response.

### -param pstrCert [out]

A pointer to a <b>BSTR</b> value that receives the certificate retrieved from the response. When you have finished using the <b>BSTR</b>, free it by calling the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is a <b>String</b> that contains a certificate.

## -remarks

The response contained in <i>strResponseFileName</i> must contain exactly one certificate; a child certificate cannot be present.

The response may be either a <a href="/windows/desktop/SecGloss/p-gly">PKCS #7</a> or a full <a href="/windows/desktop/SecGloss/c-gly">Certificate Management over CMS</a> (CMC) response. However, to accept a full CMC response, the <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP) must support <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) encoding of CMC structures.

When this method is called from script, the method displays a user interface that asks whether the user will allow a read operation from the file system.