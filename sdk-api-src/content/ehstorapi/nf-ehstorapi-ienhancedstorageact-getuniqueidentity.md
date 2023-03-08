---
UID: NF:ehstorapi.IEnhancedStorageACT.GetUniqueIdentity
title: IEnhancedStorageACT::GetUniqueIdentity (ehstorapi.h)
description: Retrieves the unique identity of the Addressable Command Target (ACT).
helpviewer_keywords: ["GetUniqueIdentity","GetUniqueIdentity method [Enhanced Storage]","GetUniqueIdentity method [Enhanced Storage]","IEnhancedStorageACT interface","IEnhancedStorageACT interface [Enhanced Storage]","GetUniqueIdentity method","IEnhancedStorageACT.GetUniqueIdentity","IEnhancedStorageACT::GetUniqueIdentity","ehstorapi/IEnhancedStorageACT::GetUniqueIdentity","enstor.ienhancedstorageact_getuniqueidentity"]
old-location: enstor\ienhancedstorageact_getuniqueidentity.htm
tech.root: enstor
ms.assetid: 0f8d33af-a771-4cbd-9740-a72fbb7e9b42
ms.date: 12/05/2018
ms.keywords: GetUniqueIdentity, GetUniqueIdentity method [Enhanced Storage], GetUniqueIdentity method [Enhanced Storage],IEnhancedStorageACT interface, IEnhancedStorageACT interface [Enhanced Storage],GetUniqueIdentity method, IEnhancedStorageACT.GetUniqueIdentity, IEnhancedStorageACT::GetUniqueIdentity, ehstorapi/IEnhancedStorageACT::GetUniqueIdentity, enstor.ienhancedstorageact_getuniqueidentity
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
 - IEnhancedStorageACT::GetUniqueIdentity
 - ehstorapi/IEnhancedStorageACT::GetUniqueIdentity
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
 - IEnhancedStorageACT.GetUniqueIdentity
---

# IEnhancedStorageACT::GetUniqueIdentity


## -description

Retrieves the unique identity of the Addressable Command Target (ACT).

## -parameters

### -param ppwszIdentity [out]

Pointer to a string that represents the unique identity of the ACT.

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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The unique identity was retrieved successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>ppwszIdentity</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The memory containing the unique identity of the ACT is allocated by the Enhanced Storage API and must be freed by passing the returned pointer to <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/ehstorapi/nn-ehstorapi-ienhancedstorageact">IEnhancedStorageACT</a>