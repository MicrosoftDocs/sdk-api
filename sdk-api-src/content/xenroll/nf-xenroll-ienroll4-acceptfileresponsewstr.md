---
UID: NF:xenroll.IEnroll4.acceptFileResponseWStr
title: IEnroll4::acceptFileResponseWStr (xenroll.h)

description: Accepts delivery of the credentials issued in response to an earlier call to createFileRequestWStr, and it places the credentials in the appropriate store.
old-location: security\ienroll4_acceptfileresponsewstr.htm
tech.root: SecCrypto
ms.assetid: b9c92f20-5f23-4dda-9e80-df9bf400ac08

ms.date: 12/05/2018
ms.keywords: IEnroll4 interface [Security],acceptFileResponseWStr method, IEnroll4.acceptFileResponseWStr, IEnroll4::acceptFileResponseWStr, acceptFileResponseWStr, acceptFileResponseWStr method [Security], acceptFileResponseWStr method [Security],IEnroll4 interface, security.ienroll4_acceptfileresponsewstr, xenroll/IEnroll4::acceptFileResponseWStr
ms.topic: method
f1_keywords: 
 - "xenroll/IEnroll4.acceptFileResponseWStr"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Xenroll.dll
api_name:
 - IEnroll4.acceptFileResponseWStr
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnroll4::acceptFileResponseWStr


## -description


<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>acceptFileResponseWStr</b> method accepts delivery of the credentials issued in response to an earlier call to 
<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createfilerequestwstr">createFileRequestWStr</a>, and it places the credentials in the appropriate store.

The response may be a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/p-gly">PKCS #7</a> message or a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">Certificate Management over CMS</a> (CMC) response. This method was first defined in the <a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll4</a> interface.


## -parameters




### -param pwszResponseFileName [in]

A pointer to a null-terminated wide character string that represents the name of the file that contains the response.


## -remarks



The response named in the <i>pwszResponseFileName</i> parameter must contain exactly one certificate; a child certificate cannot be present.

The response may be either a PKCS #7 or a full CMC response; however, to accept a full CMC response, the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> must support <a href="https://docs.microsoft.com/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) encoding of CMC structures.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll4</a>
 

 

