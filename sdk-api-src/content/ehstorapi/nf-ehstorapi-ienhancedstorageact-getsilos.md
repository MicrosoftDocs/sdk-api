---
UID: NF:ehstorapi.IEnhancedStorageACT.GetSilos
title: IEnhancedStorageACT::GetSilos (ehstorapi.h)
description: Returns an enumeration of all silos associated with the Addressable Command Target (ACT).
helpviewer_keywords: ["GetSilos","GetSilos method [Enhanced Storage]","GetSilos method [Enhanced Storage]","IEnhancedStorageACT interface","IEnhancedStorageACT interface [Enhanced Storage]","GetSilos method","IEnhancedStorageACT.GetSilos","IEnhancedStorageACT::GetSilos","ehstorapi/IEnhancedStorageACT::GetSilos","enstor.ienhancedstorageact_getsilos"]
old-location: enstor\ienhancedstorageact_getsilos.htm
tech.root: enstor
ms.assetid: 823da812-b3f5-4c61-bb33-cd970695879f
ms.date: 12/05/2018
ms.keywords: GetSilos, GetSilos method [Enhanced Storage], GetSilos method [Enhanced Storage],IEnhancedStorageACT interface, IEnhancedStorageACT interface [Enhanced Storage],GetSilos method, IEnhancedStorageACT.GetSilos, IEnhancedStorageACT::GetSilos, ehstorapi/IEnhancedStorageACT::GetSilos, enstor.ienhancedstorageact_getsilos
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
 - IEnhancedStorageACT::GetSilos
 - ehstorapi/IEnhancedStorageACT::GetSilos
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
 - IEnhancedStorageACT.GetSilos
---

# IEnhancedStorageACT::GetSilos


## -description

Returns an enumeration of all  silos associated with the Addressable Command Target (ACT).

## -parameters

### -param pppIEnhancedStorageSilos [out]

Returns an array of one or more <a href="/previous-versions/windows/desktop/api/ehstorapi/nn-ehstorapi-ienhancedstoragesilo">IEnhancedStorageSilo</a> interface pointers associated with  the ACT.

### -param pcEnhancedStorageSilos [out]

Count of <a href="/previous-versions/windows/desktop/api/ehstorapi/nn-ehstorapi-ienhancedstoragesilo">IEnhancedStorageSilo</a> pointers returned. This value indicates the dimension of the  array represented by <i>pppIEnhancedStorageSilos</i>.

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
Command was sent successfully and all associated silos have been enumerated. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Command failed due to insufficient memory allocation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pppIEnhancedStorageSilos</i> or <i>pcEnhancedStorageSilos</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The memory containing the array of <a href="/previous-versions/windows/desktop/api/ehstorapi/nn-ehstorapi-ienhancedstoragesilo">IEnhancedStorageSilo</a> interfaces is allocated by the Enhanced Storage API and must be freed by passing the returned pointer to <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/ehstorapi/nn-ehstorapi-ienhancedstorageact">IEnhancedStorageACT</a>



<a href="/previous-versions/windows/desktop/api/ehstorapi/nn-ehstorapi-ienhancedstoragesilo">IEnhancedStorageSilo</a>