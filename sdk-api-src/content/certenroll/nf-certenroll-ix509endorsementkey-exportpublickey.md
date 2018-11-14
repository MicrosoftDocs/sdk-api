---
UID: NF:certenroll.IX509EndorsementKey.ExportPublicKey
title: IX509EndorsementKey::ExportPublicKey
author: windows-sdk-content
description: Exports the endorsement public key.
old-location: security\ix509endorsementkey_exportpublickey.htm
tech.root: SecCertEnroll
ms.assetid: b38c6421-2918-4d0e-81ed-d9d575817efa
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ExportPublicKey, ExportPublicKey method [Security], ExportPublicKey method [Security],IX509EndorsementKey interface, IX509EndorsementKey interface [Security],ExportPublicKey method, IX509EndorsementKey.ExportPublicKey, IX509EndorsementKey::ExportPublicKey, certenroll/IX509EndorsementKey::ExportPublicKey, security.ix509endorsementkey_exportpublickey
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
 - IX509EndorsementKey.ExportPublicKey
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
- IX509EndorsementKey.ExportPublicKey
: 
---

# IX509EndorsementKey::ExportPublicKey


## -description


Exports the endorsement public key. You can only call the <b>ExportPublicKey</b> method after the <a href="https://msdn.microsoft.com/06855fc0-0d87-4fe7-9525-55eb60bffcd1">Open</a> method has been successfully called.


## -parameters




### -param ppPublicKey [out, retval]

The exported endorsement public key.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/24f063a7-02e3-47cf-89ca-ebc63bf3e2dc">IX509EndorsementKey</a>
 

 

