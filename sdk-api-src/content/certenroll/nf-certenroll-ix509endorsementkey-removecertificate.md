---
UID: NF:certenroll.IX509EndorsementKey.RemoveCertificate
title: IX509EndorsementKey::RemoveCertificate
author: windows-sdk-content
description: Removes an endorsement certificate related to the endorsement key from the key storage provider. You can only call the RemoveCertificate method after the Open method has been successfully called.
old-location: security\ix509endorsementkey_removecertificate.htm
tech.root: seccertenroll
ms.assetid: 40c5d77c-9b0d-4ee4-a02e-cec9b2f1b392
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IX509EndorsementKey interface [Security],RemoveCertificate method, IX509EndorsementKey.RemoveCertificate, IX509EndorsementKey::RemoveCertificate, RemoveCertificate, RemoveCertificate method [Security], RemoveCertificate method [Security],IX509EndorsementKey interface, certenroll/IX509EndorsementKey::RemoveCertificate, security.ix509endorsementkey_removecertificate
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
 - IX509EndorsementKey.RemoveCertificate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509EndorsementKey::RemoveCertificate


## -description


Removes an endorsement certificate related to the endorsement key from the key storage provider. You can only call the <b>RemoveCertificate</b> method after the <a href="https://msdn.microsoft.com/en-us/library/Dn379364(v=VS.85).aspx">Open</a> method has been successfully called.


## -parameters




### -param Encoding [in]

An <a href="https://msdn.microsoft.com/en-us/library/Aa374936(v=VS.85).aspx">EncodingType</a> enumeration value that specifies the type of Unicode-encoding applied to the  endorsement certificate. The default value is XCN_CRYPT_STRING_BASE64.


### -param strCertificate [in]

The certificate to remove from the store.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Only non-manufacturer certificates can be removed from the key storage provider.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn379356(v=VS.85).aspx">IX509EndorsementKey</a>
 

 

