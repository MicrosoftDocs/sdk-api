---
UID: NF:certenroll.IX509EndorsementKey.GetCertificateByIndex
title: IX509EndorsementKey::GetCertificateByIndex (certenroll.h)
description: Gets the endorsement certificate associated with the endorsement key from the key storage provider for the specified index.
helpviewer_keywords: ["GetCertificateByIndex","GetCertificateByIndex method [Security]","GetCertificateByIndex method [Security]","IX509EndorsementKey interface","IX509EndorsementKey interface [Security]","GetCertificateByIndex method","IX509EndorsementKey.GetCertificateByIndex","IX509EndorsementKey::GetCertificateByIndex","certenroll/IX509EndorsementKey::GetCertificateByIndex","security.ix509endorsementkey_getcertificatebyindex"]
old-location: security\ix509endorsementkey_getcertificatebyindex.htm
tech.root: seccertenroll
ms.assetid: ab1eb37a-d79e-4d02-8e60-6c093f42c68f
ms.date: 12/05/2018
ms.keywords: GetCertificateByIndex, GetCertificateByIndex method [Security], GetCertificateByIndex method [Security],IX509EndorsementKey interface, IX509EndorsementKey interface [Security],GetCertificateByIndex method, IX509EndorsementKey.GetCertificateByIndex, IX509EndorsementKey::GetCertificateByIndex, certenroll/IX509EndorsementKey::GetCertificateByIndex, security.ix509endorsementkey_getcertificatebyindex
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
 - IX509EndorsementKey::GetCertificateByIndex
 - certenroll/IX509EndorsementKey::GetCertificateByIndex
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
 - IX509EndorsementKey.GetCertificateByIndex
---

# IX509EndorsementKey::GetCertificateByIndex


## -description

Gets the endorsement certificate associated with the endorsement key from the key storage provider for the specified index. You can only call the <b>GetCertificateByIndex</b> method after the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509endorsementkey-open">Open</a> method has been successfully called.

## -parameters

### -param ManufacturerOnly [in]

True to get manufacturer endorsement keys only; otherwise false. The default is false.

### -param dwIndex [in]

The index of the requested endorsement certificate.

### -param Encoding [in]

An <a href="/windows/desktop/api/certenroll/ne-certenroll-encodingtype">EncodingType</a> enumeration value that specifies the type of Unicode-encoding applied to the  endorsement certificate. The default value is XCN_CRYPT_STRING_BASE64.

### -param pValue [out, retval]

The endorsement certificate requested.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509endorsementkey">IX509EndorsementKey</a>