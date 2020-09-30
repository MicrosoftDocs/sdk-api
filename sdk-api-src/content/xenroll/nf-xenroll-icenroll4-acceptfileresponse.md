---
UID: NF:xenroll.ICEnroll4.acceptFileResponse
title: ICEnroll4::acceptFileResponse (xenroll.h)
description: Accepts delivery of the credentials issued in response to an earlier call to createFileRequest, and it places the credentials in the appropriate store.
helpviewer_keywords: ["CEnroll object [Security]","acceptFileResponse method","ICEnroll4 interface [Security]","acceptFileResponse method","ICEnroll4.acceptFileResponse","ICEnroll4::acceptFileResponse","_xen_icenroll4_acceptfileresponse","acceptFileResponse","acceptFileResponse method [Security]","acceptFileResponse method [Security]","CEnroll object","acceptFileResponse method [Security]","ICEnroll4 interface","security.icenroll4_acceptfileresponse","xenroll/ICEnroll4::acceptFileResponse"]
old-location: security\icenroll4_acceptfileresponse.htm
tech.root: security
ms.assetid: 127863ca-843b-46c5-b375-fb0400e8b49b
ms.date: 12/05/2018
ms.keywords: CEnroll object [Security],acceptFileResponse method, ICEnroll4 interface [Security],acceptFileResponse method, ICEnroll4.acceptFileResponse, ICEnroll4::acceptFileResponse, _xen_icenroll4_acceptfileresponse, acceptFileResponse, acceptFileResponse method [Security], acceptFileResponse method [Security],CEnroll object, acceptFileResponse method [Security],ICEnroll4 interface, security.icenroll4_acceptfileresponse, xenroll/ICEnroll4::acceptFileResponse
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
 - ICEnroll4::acceptFileResponse
 - xenroll/ICEnroll4::acceptFileResponse
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
 - ICEnroll4.acceptFileResponse
 - CEnroll.acceptFileResponse
---

# ICEnroll4::acceptFileResponse


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>acceptFileResponse</b> method accepts delivery of the credentials issued in response to an earlier call to 
<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll4-createfilerequest">createFileRequest</a>, and it places the credentials in the appropriate store. This method was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll4">ICEnroll4</a> interface.

The response may be a <a href="/windows/desktop/SecGloss/p-gly">PKCS #7</a> message or a <a href="/windows/desktop/SecGloss/c-gly">Certificate Management over CMS</a> (CMC) response.

## -parameters

### -param strResponseFileName [in]

Specifies the name of the file that contains the base64-encoded response.

## -returns

<h3>VB</h3>
If the method succeeds, the method returns <b>S_OK</b>.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see 
<a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

The response named in the <i>strResponseFileName</i> parameter must contain exactly one certificate; a child certificate cannot be present.

The response may be either a PKCS #7 or a full CMC response; however, to accept a full CMC response, the <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> must support <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) encoding of CMC structures.

When this method is called from script, the method displays a user interface that asks whether the user will allow installation of a  certificate and whether the user will allow a read operation from the file system.