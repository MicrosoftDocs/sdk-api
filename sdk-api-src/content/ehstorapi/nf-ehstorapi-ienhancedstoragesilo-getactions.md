---
UID: NF:ehstorapi.IEnhancedStorageSilo.GetActions
title: IEnhancedStorageSilo::GetActions (ehstorapi.h)
description: Returns an enumeration of all actions available to the silo object.
helpviewer_keywords: ["GetActions","GetActions method [Enhanced Storage]","GetActions method [Enhanced Storage]","IEnhancedStorageSilo interface","IEnhancedStorageSilo interface [Enhanced Storage]","GetActions method","IEnhancedStorageSilo.GetActions","IEnhancedStorageSilo::GetActions","ehstorapi/IEnhancedStorageSilo::GetActions","enstor.ienhancedstoragesilo_getactions"]
old-location: enstor\ienhancedstoragesilo_getactions.htm
tech.root: enstor
ms.assetid: eaf24814-b47a-4f33-ac17-d3b5b344f234
ms.date: 12/05/2018
ms.keywords: GetActions, GetActions method [Enhanced Storage], GetActions method [Enhanced Storage],IEnhancedStorageSilo interface, IEnhancedStorageSilo interface [Enhanced Storage],GetActions method, IEnhancedStorageSilo.GetActions, IEnhancedStorageSilo::GetActions, ehstorapi/IEnhancedStorageSilo::GetActions, enstor.ienhancedstoragesilo_getactions
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
 - IEnhancedStorageSilo::GetActions
 - ehstorapi/IEnhancedStorageSilo::GetActions
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
 - IEnhancedStorageSilo.GetActions
---

# IEnhancedStorageSilo::GetActions


## -description

Returns an enumeration of all actions available to the silo object.

## -parameters

### -param pppIEnhancedStorageSiloActions [out]

Array of pointers to <a href="/previous-versions/windows/desktop/api/ehstorapi/nn-ehstorapi-ienhancedstoragesiloaction">IEnhancedStorageAction</a> interface objects that represent the actions available for the silo object. This array is allocated within the API when at least one action is available to the silo.

### -param pcEnhancedStorageSiloActions [out]

Count of <a href="/previous-versions/windows/desktop/api/ehstorapi/nn-ehstorapi-ienhancedstoragesiloaction">IEnhancedStorageAction</a> pointers returned. This value indicates the dimension of the  array represented by <i>pppIEnhancedStorageSilos</i>.

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
One or more ACTs were found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pppIEnhancedStorageSiloActions</i> or  <i>pcEnhancedStorageSiloActions</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The memory containing the <a href="/previous-versions/windows/desktop/api/ehstorapi/nn-ehstorapi-ienhancedstoragesiloaction">IEnhancedStorageAction</a> interface pointers is allocated by the Enhanced Storage API and must be freed by passing the returned pointer to <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/ehstorapi/nn-ehstorapi-ienhancedstoragesilo">IEnhancedStorageSilo</a>