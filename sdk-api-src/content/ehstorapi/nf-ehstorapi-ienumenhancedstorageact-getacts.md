---
UID: NF:ehstorapi.IEnumEnhancedStorageACT.GetACTs
title: IEnumEnhancedStorageACT::GetACTs (ehstorapi.h)
description: Returns an enumeration of all the Addressable Command Targets (ACT) currently connected to the system. If at least one ACT is present, the Enhanced Storage API allocates an array of 1 or more IEnumEnhancedStorageACT pointers.
helpviewer_keywords: ["GetACTs","GetACTs method [Enhanced Storage]","GetACTs method [Enhanced Storage]","IEnumEnhancedStorageACT interface","IEnumEnhancedStorageACT interface [Enhanced Storage]","GetACTs method","IEnumEnhancedStorageACT.GetACTs","IEnumEnhancedStorageACT::GetACTs","ehstorapi/IEnumEnhancedStorageACT::GetACTs","enstor.ienumenhancedstorageact_getacts"]
old-location: enstor\ienumenhancedstorageact_getacts.htm
tech.root: enstor
ms.assetid: 139bb8ed-faca-4fe7-ab6f-63c71d25a711
ms.date: 12/05/2018
ms.keywords: GetACTs, GetACTs method [Enhanced Storage], GetACTs method [Enhanced Storage],IEnumEnhancedStorageACT interface, IEnumEnhancedStorageACT interface [Enhanced Storage],GetACTs method, IEnumEnhancedStorageACT.GetACTs, IEnumEnhancedStorageACT::GetACTs, ehstorapi/IEnumEnhancedStorageACT::GetACTs, enstor.ienumenhancedstorageact_getacts
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
 - IEnumEnhancedStorageACT::GetACTs
 - ehstorapi/IEnumEnhancedStorageACT::GetACTs
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
 - IEnumEnhancedStorageACT.GetACTs
---

# IEnumEnhancedStorageACT::GetACTs


## -description

Returns an enumeration of all the Addressable Command Targets (ACT) currently connected to the system. If at least one ACT is present, the Enhanced Storage API allocates an array of 1 or more <a href="/previous-versions/windows/desktop/api/ehstorapi/nn-ehstorapi-ienumenhancedstorageact">IEnumEnhancedStorageACT</a> pointers.

## -parameters

### -param pppIEnhancedStorageACTs [out]

Array of <a href="/previous-versions/windows/desktop/api/ehstorapi/nn-ehstorapi-ienhancedstorageact">IEnhancedStorageACT</a> interface pointers that represent the ACTs for all devices connected to the system. This array is allocated within the API.

### -param pcEnhancedStorageACTs

Count of <a href="/previous-versions/windows/desktop/api/ehstorapi/nn-ehstorapi-ienhancedstorageact">IEnhancedStorageACT</a> pointers returned. This is the dimension of the  array represented by <i>pppIEnhancedStorageACTs</i>.

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
pppIEnhancedStorageACTs or pcEnhancedStorageACTs is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Operation failed due to insufficient memory.

</td>
</tr>
</table>

## -remarks

The memory containing the array of <a href="/previous-versions/windows/desktop/api/ehstorapi/nn-ehstorapi-ienhancedstorageact">IEnhancedStorageACT</a> interfaces is allocated by the Enhanced Storage API and must be freed by passing the returned pointer to the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> method.

## -see-also

<a href="/previous-versions/windows/desktop/api/ehstorapi/nn-ehstorapi-ienumenhancedstorageact">IEnumEnhancedStorageACT</a>