---
UID: NF:certenroll.IX509EndorsementKey.Close
title: IX509EndorsementKey::Close
author: windows-driver-content
description: Closes the endorsement key. You can only call the Close method after the Open method has been successfully called.
old-location: security\ix509endorsementkey_close.htm
old-project: SecCertEnroll
ms.assetid: 71855c96-a828-4bb6-849a-53be8269277d
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: Close, Close method [Security], Close method [Security],IX509EndorsementKey interface, IX509EndorsementKey interface [Security],Close method, IX509EndorsementKey.Close, IX509EndorsementKey::Close, certenroll/IX509EndorsementKey::Close, security.ix509endorsementkey_close
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: X509RequestType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Certenroll.dll
api_name:
-	IX509EndorsementKey.Close
product: Windows
targetos: Windows
req.lib: 
req.dll: Certenroll.dll
req.irql: 
---

# IX509EndorsementKey::Close


## -description


Closes the endorsement key. You can only call the <b>Close</b> method after the <a href="https://msdn.microsoft.com/library/windows/hardware/hh451153">Open</a> method has been successfully called.


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <b>Close</b> method releases any resources held
    by the object except for the <a href="https://msdn.microsoft.com/library/windows/hardware/dn915743">ProviderName</a>.
    The <b>ProviderName</b> is released when it is re-assigned
    or when this object is destroyed.





## -see-also




<a href="https://msdn.microsoft.com/24f063a7-02e3-47cf-89ca-ebc63bf3e2dc">IX509EndorsementKey</a>
 

 

