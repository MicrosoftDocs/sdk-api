---
UID: NF:certenroll.ICertificateAttestationChallenge.Initialize
title: ICertificateAttestationChallenge::Initialize (certenroll.h)
description: Initialize using the full Certificate Management over CMS (CMC) response returned from the CA.
helpviewer_keywords: ["ICertificateAttestationChallenge interface [Security]","Initialize method","ICertificateAttestationChallenge.Initialize","ICertificateAttestationChallenge::Initialize","Initialize","Initialize method [Security]","Initialize method [Security]","ICertificateAttestationChallenge interface","certenroll/ICertificateAttestationChallenge::Initialize","security.icertificateattestationchallenge_initialize"]
old-location: security\icertificateattestationchallenge_initialize.htm
tech.root: security
ms.assetid: d4dbda92-4523-4adb-9b88-b2bc763570fd
ms.date: 12/05/2018
ms.keywords: ICertificateAttestationChallenge interface [Security],Initialize method, ICertificateAttestationChallenge.Initialize, ICertificateAttestationChallenge::Initialize, Initialize, Initialize method [Security], Initialize method [Security],ICertificateAttestationChallenge interface, certenroll/ICertificateAttestationChallenge::Initialize, security.icertificateattestationchallenge_initialize
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Certenroll.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Certenroll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertificateAttestationChallenge::Initialize
 - certenroll/ICertificateAttestationChallenge::Initialize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certenroll.dll
api_name:
 - ICertificateAttestationChallenge.Initialize
---

# ICertificateAttestationChallenge::Initialize


## -description

Initialize using the full <a href="/windows/desktop/SecGloss/c-gly">Certificate Management over CMS</a> (CMC) response returned from the CA.

## -parameters

### -param Encoding [in]

An <a href="/windows/desktop/api/certenroll/ne-certenroll-encodingtype">EncodingType</a> enumeration value that specifies the type of Unicode-encoding applied to the  response. The default value is XCN_CRYPT_STRING_BASE64.

### -param strPendingFullCmcResponseWithChallenge [in]

The pending CMC response from the CA.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The CA should have returned a pending CMC response. The content of the CMC response should contain a challenge. There must be only one CMC response and it must contain pending information.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icertificateattestationchallenge">ICertificateAttestationChallenge</a>