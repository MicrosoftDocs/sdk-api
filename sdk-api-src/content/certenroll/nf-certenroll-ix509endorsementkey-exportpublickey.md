---
UID: NF:certenroll.IX509EndorsementKey.ExportPublicKey
title: IX509EndorsementKey::ExportPublicKey (certenroll.h)
description: Exports the endorsement public key.
helpviewer_keywords: ["ExportPublicKey","ExportPublicKey method [Security]","ExportPublicKey method [Security]","IX509EndorsementKey interface","IX509EndorsementKey interface [Security]","ExportPublicKey method","IX509EndorsementKey.ExportPublicKey","IX509EndorsementKey::ExportPublicKey","certenroll/IX509EndorsementKey::ExportPublicKey","security.ix509endorsementkey_exportpublickey"]
old-location: security\ix509endorsementkey_exportpublickey.htm
tech.root: security
ms.assetid: b38c6421-2918-4d0e-81ed-d9d575817efa
ms.date: 12/05/2018
ms.keywords: ExportPublicKey, ExportPublicKey method [Security], ExportPublicKey method [Security],IX509EndorsementKey interface, IX509EndorsementKey interface [Security],ExportPublicKey method, IX509EndorsementKey.ExportPublicKey, IX509EndorsementKey::ExportPublicKey, certenroll/IX509EndorsementKey::ExportPublicKey, security.ix509endorsementkey_exportpublickey
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
 - IX509EndorsementKey::ExportPublicKey
 - certenroll/IX509EndorsementKey::ExportPublicKey
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
 - IX509EndorsementKey.ExportPublicKey
---

# IX509EndorsementKey::ExportPublicKey


## -description

Exports the endorsement public key. You can only call the <b>ExportPublicKey</b> method after the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509endorsementkey-open">Open</a> method has been successfully called.

## -parameters

### -param ppPublicKey [out, retval]

The exported endorsement public key.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509endorsementkey">IX509EndorsementKey</a>