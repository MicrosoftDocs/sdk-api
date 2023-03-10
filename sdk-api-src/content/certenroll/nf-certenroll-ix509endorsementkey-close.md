---
UID: NF:certenroll.IX509EndorsementKey.Close
title: IX509EndorsementKey::Close (certenroll.h)
description: Closes the endorsement key. You can only call the Close method after the Open method has been successfully called.
helpviewer_keywords: ["Close","Close method [Security]","Close method [Security]","IX509EndorsementKey interface","IX509EndorsementKey interface [Security]","Close method","IX509EndorsementKey.Close","IX509EndorsementKey::Close","certenroll/IX509EndorsementKey::Close","security.ix509endorsementkey_close"]
old-location: security\ix509endorsementkey_close.htm
tech.root: security
ms.assetid: 71855c96-a828-4bb6-849a-53be8269277d
ms.date: 12/05/2018
ms.keywords: Close, Close method [Security], Close method [Security],IX509EndorsementKey interface, IX509EndorsementKey interface [Security],Close method, IX509EndorsementKey.Close, IX509EndorsementKey::Close, certenroll/IX509EndorsementKey::Close, security.ix509endorsementkey_close
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
 - IX509EndorsementKey::Close
 - certenroll/IX509EndorsementKey::Close
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
 - IX509EndorsementKey.Close
---

# IX509EndorsementKey::Close


## -description

Closes the endorsement key. You can only call the <b>Close</b> method after the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509endorsementkey-open">Open</a> method has been successfully called.



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <b>Close</b> method releases any resources held
    by the object except for the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509endorsementkey-get_providername">ProviderName</a>.
    The <b>ProviderName</b> is released when it is re-assigned
    or when this object is destroyed.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509endorsementkey">IX509EndorsementKey</a>
