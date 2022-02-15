---
UID: NN:certenroll.ICertificateAttestationChallenge
title: ICertificateAttestationChallenge (certenroll.h)
description: Allows applications to decrypt a key attestation challenge received from a server.
helpviewer_keywords: ["ICertificateAttestationChallenge","ICertificateAttestationChallenge interface [Security]","ICertificateAttestationChallenge interface [Security]","described","certenroll/ICertificateAttestationChallenge","security.icertificateattestationchallenge"]
old-location: security\icertificateattestationchallenge.htm
tech.root: security
ms.assetid: 3b8d3104-5824-4801-9b74-59307e650662
ms.date: 12/05/2018
ms.keywords: ICertificateAttestationChallenge, ICertificateAttestationChallenge interface [Security], ICertificateAttestationChallenge interface [Security],described, certenroll/ICertificateAttestationChallenge, security.icertificateattestationchallenge
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
 - ICertificateAttestationChallenge
 - certenroll/ICertificateAttestationChallenge
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
 - ICertificateAttestationChallenge
---

# ICertificateAttestationChallenge interface


## -description

Allows applications to decrypt a key attestation challenge received from a server.

## -inheritance

The <b>ICertificateAttestationChallenge</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ICertificateAttestationChallenge</b> also has these types of members:

## -remarks

If the challenge is successfully decrypted, the decrypted secret needs to be sent back to the server so that an attested end entity certificate can be issued.
