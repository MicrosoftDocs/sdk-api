---
UID: NF:xenroll.IEnroll4.getCertContextFromResponseBlob
title: IEnroll4::getCertContextFromResponseBlob (xenroll.h)
description: Retrieves the certificate from a certification authority's response.
helpviewer_keywords: ["IEnroll4 interface [Security]","getCertContextFromResponseBlob method","IEnroll4.getCertContextFromResponseBlob","IEnroll4::getCertContextFromResponseBlob","getCertContextFromResponseBlob","getCertContextFromResponseBlob method [Security]","getCertContextFromResponseBlob method [Security]","IEnroll4 interface","security.ienroll4_getcertcontextfromresponseblob","xenroll/IEnroll4::getCertContextFromResponseBlob"]
old-location: security\ienroll4_getcertcontextfromresponseblob.htm
tech.root: security
ms.assetid: 824626bf-a20d-4d34-a061-9f54b142e0fc
ms.date: 12/05/2018
ms.keywords: IEnroll4 interface [Security],getCertContextFromResponseBlob method, IEnroll4.getCertContextFromResponseBlob, IEnroll4::getCertContextFromResponseBlob, getCertContextFromResponseBlob, getCertContextFromResponseBlob method [Security], getCertContextFromResponseBlob method [Security],IEnroll4 interface, security.ienroll4_getcertcontextfromresponseblob, xenroll/IEnroll4::getCertContextFromResponseBlob
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
 - IEnroll4::getCertContextFromResponseBlob
 - xenroll/IEnroll4::getCertContextFromResponseBlob
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
 - IEnroll4.getCertContextFromResponseBlob
---

# IEnroll4::getCertContextFromResponseBlob


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>getCertContextFromResponseBlob</b> method retrieves the certificate from a <a href="/windows/desktop/SecGloss/c-gly">certification authority's</a> response.This method was first defined by the <a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll4</a> interface.

## -parameters

### -param pblobResponse [in]

A pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure that represents the response.

### -param ppCertContext [out]

A pointer to a pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure  that receives the certificate retrieved from the response.

## -remarks

The response contained in <i>pblobResponse</i> must contain exactly one certificate; a child certificate cannot be present.

The response may be either a PKCS #7 or a full <a href="/windows/desktop/SecGloss/c-gly">Certificate Management over CMS</a> (CMC) response. However, to accept a full CMC response, the <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> must support <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) encoding of CMC structures.

## -see-also

<a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll4</a>