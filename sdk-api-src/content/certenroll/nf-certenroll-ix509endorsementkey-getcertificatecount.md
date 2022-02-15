---
UID: NF:certenroll.IX509EndorsementKey.GetCertificateCount
title: IX509EndorsementKey::GetCertificateCount (certenroll.h)
description: Gets the count of the endorsement certificates in the key storage provider.
helpviewer_keywords: ["GetCertificateCount","GetCertificateCount method [Security]","GetCertificateCount method [Security]","IX509EndorsementKey interface","IX509EndorsementKey interface [Security]","GetCertificateCount method","IX509EndorsementKey.GetCertificateCount","IX509EndorsementKey::GetCertificateCount","certenroll/IX509EndorsementKey::GetCertificateCount","security.ix509endorsementkey_getcertificatecount"]
old-location: security\ix509endorsementkey_getcertificatecount.htm
tech.root: security
ms.assetid: 1a8ae8f9-c4df-4701-845d-7f9a42593d57
ms.date: 12/05/2018
ms.keywords: GetCertificateCount, GetCertificateCount method [Security], GetCertificateCount method [Security],IX509EndorsementKey interface, IX509EndorsementKey interface [Security],GetCertificateCount method, IX509EndorsementKey.GetCertificateCount, IX509EndorsementKey::GetCertificateCount, certenroll/IX509EndorsementKey::GetCertificateCount, security.ix509endorsementkey_getcertificatecount
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
 - IX509EndorsementKey::GetCertificateCount
 - certenroll/IX509EndorsementKey::GetCertificateCount
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
 - IX509EndorsementKey.GetCertificateCount
---

# IX509EndorsementKey::GetCertificateCount


## -description

Gets the count of the endorsement certificates in the key storage provider. You can only call the <b>GetCertificateCount</b> method after the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509endorsementkey-open">Open</a> method has been successfully called.

## -parameters

### -param ManufacturerOnly [in]

True to return the count for only manufacturer certificates. False to return the count for only non-manufacturer certificates.

### -param pCount [out, retval]

The count of endorsement certificates from the key storage provider.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509endorsementkey">IX509EndorsementKey</a>