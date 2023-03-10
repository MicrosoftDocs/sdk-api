---
UID: NF:ehstorapi.IEnhancedStorageSilo.GetInfo
title: IEnhancedStorageSilo::GetInfo (ehstorapi.h)
description: Returns the descriptive information associated with the silo object.
helpviewer_keywords: ["GetInfo","GetInfo method [Enhanced Storage]","GetInfo method [Enhanced Storage]","IEnhancedStorageSilo interface","IEnhancedStorageSilo interface [Enhanced Storage]","GetInfo method","IEnhancedStorageSilo.GetInfo","IEnhancedStorageSilo::GetInfo","ehstorapi/IEnhancedStorageSilo::GetInfo","enstor.ienhancedstoragesilo_getinfo"]
old-location: enstor\ienhancedstoragesilo_getinfo.htm
tech.root: enstor
ms.assetid: c3d84462-fb2c-4ad7-b539-1d6c775812dd
ms.date: 12/05/2018
ms.keywords: GetInfo, GetInfo method [Enhanced Storage], GetInfo method [Enhanced Storage],IEnhancedStorageSilo interface, IEnhancedStorageSilo interface [Enhanced Storage],GetInfo method, IEnhancedStorageSilo.GetInfo, IEnhancedStorageSilo::GetInfo, ehstorapi/IEnhancedStorageSilo::GetInfo, enstor.ienhancedstoragesilo_getinfo
req.header: ehstorapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: EhStorAPI.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnhancedStorageSilo::GetInfo
 - ehstorapi/IEnhancedStorageSilo::GetInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - EhStorAPI.h
api_name:
 - IEnhancedStorageSilo.GetInfo
---

# IEnhancedStorageSilo::GetInfo


## -description

Returns the descriptive information associated with the silo object.

## -parameters

### -param pSiloInfo [out]

Pointer to a <a href="/windows/desktop/api/ehstorapi/ns-ehstorapi-silo_info">SILO_INFO</a> object containing descriptive information associated with the silo.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK </b></dt>
</dl>
</td>
<td width="60%">
Silo information was retrieved successfully. 

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/ehstorapi/nn-ehstorapi-ienhancedstoragesilo">IEnhancedStorageSilo</a>