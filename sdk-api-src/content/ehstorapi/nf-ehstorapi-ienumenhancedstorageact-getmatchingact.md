---
UID: NF:ehstorapi.IEnumEnhancedStorageACT.GetMatchingACT
title: IEnumEnhancedStorageACT::GetMatchingACT (ehstorapi.h)
description: Returns the Addressable Command Target (ACT) associated with the volume specified via the string supplied by the client.
helpviewer_keywords: ["GetMatchingACT","GetMatchingACT method [Enhanced Storage]","GetMatchingACT method [Enhanced Storage]","IEnumEnhancedStorageACT interface","IEnumEnhancedStorageACT interface [Enhanced Storage]","GetMatchingACT method","IEnumEnhancedStorageACT.GetMatchingACT","IEnumEnhancedStorageACT::GetMatchingACT","ehstorapi/IEnumEnhancedStorageACT::GetMatchingACT","enstor.ienumenhancedstorageact_getmatchingact"]
old-location: enstor\ienumenhancedstorageact_getmatchingact.htm
tech.root: enstor
ms.assetid: 13c0475e-a73a-4e26-b6ec-6b9cb19e23f3
ms.date: 12/05/2018
ms.keywords: GetMatchingACT, GetMatchingACT method [Enhanced Storage], GetMatchingACT method [Enhanced Storage],IEnumEnhancedStorageACT interface, IEnumEnhancedStorageACT interface [Enhanced Storage],GetMatchingACT method, IEnumEnhancedStorageACT.GetMatchingACT, IEnumEnhancedStorageACT::GetMatchingACT, ehstorapi/IEnumEnhancedStorageACT::GetMatchingACT, enstor.ienumenhancedstorageact_getmatchingact
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
 - IEnumEnhancedStorageACT::GetMatchingACT
 - ehstorapi/IEnumEnhancedStorageACT::GetMatchingACT
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
 - IEnumEnhancedStorageACT.GetMatchingACT
---

# IEnumEnhancedStorageACT::GetMatchingACT


## -description

Returns the Addressable Command Target (ACT) associated with the volume specified via the string supplied by the client.

## -parameters

### -param szVolume [in]

A string that specifies the volume for which a matching ACT is searched for.

### -param ppIEnhancedStorageACT [out]

Pointer to an <b>IEnhancedStorageACT</b> interface pointer that represents the matching ACT. If no matching ACT is found the error <b>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)</b> is returned.

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
A matching ACT was successfully found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>szVolume</i> or <i>ppIEnhancedStorageACT</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
A matching ACT wasn't found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)</b></dt>
</dl>
</td>
<td width="60%">
Enhanced storage is not supported on the device containing <i>szVolume</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_INVALID_FUNCTION)</b></dt>
</dl>
</td>
<td width="60%">
Enhanced storage is not supported on the device containing <i>szVolume</i>.

</td>
</tr>
</table>

## -remarks

This method can also be utilized by the client to determine if the specified volume resides on, and is represented by an IEEE 1667 ACT.

## -see-also

<a href="/previous-versions/windows/desktop/api/ehstorapi/nn-ehstorapi-ienumenhancedstorageact">IEnumEnhancedStorageACT</a>