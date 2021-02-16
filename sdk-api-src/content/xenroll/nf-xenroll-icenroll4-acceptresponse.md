---
UID: NF:xenroll.ICEnroll4.acceptResponse
title: ICEnroll4::acceptResponse (xenroll.h)
description: Accepts delivery of the credentials issued in response to an earlier call to createRequest and places the credentials in the appropriate store.
helpviewer_keywords: ["CEnroll object [Security]","acceptResponse method","ICEnroll4 interface [Security]","acceptResponse method","ICEnroll4.acceptResponse","ICEnroll4::acceptResponse","_xen_icenroll4_acceptresponse","acceptResponse","acceptResponse method [Security]","acceptResponse method [Security]","CEnroll object","acceptResponse method [Security]","ICEnroll4 interface","security.icenroll4_acceptresponse","xenroll/ICEnroll4::acceptResponse"]
old-location: security\icenroll4_acceptresponse.htm
tech.root: security
ms.assetid: 1149a76e-e714-4bc7-842c-6fcbe220cd24
ms.date: 12/05/2018
ms.keywords: CEnroll object [Security],acceptResponse method, ICEnroll4 interface [Security],acceptResponse method, ICEnroll4.acceptResponse, ICEnroll4::acceptResponse, _xen_icenroll4_acceptresponse, acceptResponse, acceptResponse method [Security], acceptResponse method [Security],CEnroll object, acceptResponse method [Security],ICEnroll4 interface, security.icenroll4_acceptresponse, xenroll/ICEnroll4::acceptResponse
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
 - ICEnroll4::acceptResponse
 - xenroll/ICEnroll4::acceptResponse
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
 - ICEnroll4.acceptResponse
 - CEnroll.acceptResponse
---

# ICEnroll4::acceptResponse


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>acceptResponse</b> method accepts delivery of the credentials issued in response to an earlier call to 
<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll4-createrequest">createRequest</a> and places the credentials in the appropriate store.  This method was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll4">ICEnroll4</a> interface.

The response may be a <a href="/windows/desktop/SecGloss/p-gly">PKCS #7</a> format or a full <a href="/windows/desktop/SecGloss/c-gly">Certificate Management over CMS</a> (CMC) response.

## -parameters

### -param strResponse [in]

A string that represents the base64-encoded response.

## -returns

<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see 
<a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

The response must contain exactly one certificate; a child certificate cannot be present.

The response may be either a PKCS #7 or a full CMC response; however, to accept a full CMC response, the <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> must support <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) encoding of CMC structures.

When this method is called from script, the method displays a user interface that asks whether the user will allow installation of a  certificate.