---
UID: NF:certenroll.IX509EndorsementKey.GetCertificateCount
title: IX509EndorsementKey::GetCertificateCount
author: windows-sdk-content
description: Gets the count of the endorsement certificates in the key storage provider.
old-location: security\ix509endorsementkey_getcertificatecount.htm
tech.root: SecCertEnroll
ms.assetid: 1a8ae8f9-c4df-4701-845d-7f9a42593d57
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetCertificateCount, GetCertificateCount method [Security], GetCertificateCount method [Security],IX509EndorsementKey interface, IX509EndorsementKey interface [Security],GetCertificateCount method, IX509EndorsementKey.GetCertificateCount, IX509EndorsementKey::GetCertificateCount, certenroll/IX509EndorsementKey::GetCertificateCount, security.ix509endorsementkey_getcertificatecount
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
 - IX509EndorsementKey.GetCertificateCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- certenroll.h
: 
- IX509EndorsementKey.GetCertificateCount
: 
---

# IX509EndorsementKey::GetCertificateCount


## -description


Gets the count of the endorsement certificates in the key storage provider. You can only call the <b>GetCertificateCount</b> method after the <a href="https://msdn.microsoft.com/en-us/library/Dn379364(v=VS.85).aspx">Open</a> method has been successfully called.


## -parameters




### -param ManufacturerOnly [in]

True to return the count for only manufacturer certificates. False to return the count for only non-manufacturer certificates.


### -param pCount [out, retval]

The count of endorsement certificates from the key storage provider.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn379356(v=VS.85).aspx">IX509EndorsementKey</a>
 

 

