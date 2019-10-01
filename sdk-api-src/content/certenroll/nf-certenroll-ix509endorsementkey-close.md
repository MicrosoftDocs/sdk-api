---
UID: NF:certenroll.IX509EndorsementKey.Close
title: IX509EndorsementKey::Close (certenroll.h)
author: windows-sdk-content
description: Closes the endorsement key. You can only call the Close method after the Open method has been successfully called.
old-location: security\ix509endorsementkey_close.htm
tech.root: seccertenroll
ms.assetid: 71855c96-a828-4bb6-849a-53be8269277d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Close, Close method [Security], Close method [Security],IX509EndorsementKey interface, IX509EndorsementKey interface [Security],Close method, IX509EndorsementKey.Close, IX509EndorsementKey::Close, certenroll/IX509EndorsementKey::Close, security.ix509endorsementkey_close
ms.topic: method
f1_keywords: 
 - "certenroll/IX509EndorsementKey.Close"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certenroll.dll
api_name:
 - IX509EndorsementKey.Close
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IX509EndorsementKey::Close


## -description


Closes the endorsement key. You can only call the <b>Close</b> method after the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509endorsementkey-open">Open</a> method has been successfully called.


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <b>Close</b> method releases any resources held
    by the object except for the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509endorsementkey-get_providername">ProviderName</a>.
    The <b>ProviderName</b> is released when it is re-assigned
    or when this object is destroyed.





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509endorsementkey">IX509EndorsementKey</a>
 

 

