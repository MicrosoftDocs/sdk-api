---
UID: NF:ehstorapi.IEnhancedStorageACT2.GetDeviceName
title: IEnhancedStorageACT2::GetDeviceName (ehstorapi.h)
description: IEnhancedStorageACT2::GetDeviceName method returns the device name associated with the Addressable Command Target (ACT).
helpviewer_keywords: ["GetDeviceName","GetDeviceName method [Enhanced Storage]","GetDeviceName method [Enhanced Storage]","IEnhancedStorageACT2 interface","IEnhancedStorageACT2 interface [Enhanced Storage]","GetDeviceName method","IEnhancedStorageACT2.GetDeviceName","IEnhancedStorageACT2::GetDeviceName","ehstorapi/IEnhancedStorageACT2::GetDeviceName","enstor.ienhancedstorageact2_getdevicename"]
old-location: enstor\ienhancedstorageact2_getdevicename.htm
tech.root: enstor
ms.assetid: 8603a7c3-b3b9-4b84-9f74-96b639c6c961
ms.date: 12/05/2018
ms.keywords: GetDeviceName, GetDeviceName method [Enhanced Storage], GetDeviceName method [Enhanced Storage],IEnhancedStorageACT2 interface, IEnhancedStorageACT2 interface [Enhanced Storage],GetDeviceName method, IEnhancedStorageACT2.GetDeviceName, IEnhancedStorageACT2::GetDeviceName, ehstorapi/IEnhancedStorageACT2::GetDeviceName, enstor.ienhancedstorageact2_getdevicename
req.header: ehstorapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
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
 - IEnhancedStorageACT2::GetDeviceName
 - ehstorapi/IEnhancedStorageACT2::GetDeviceName
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
 - IEnhancedStorageACT2.GetDeviceName
---

# IEnhancedStorageACT2::GetDeviceName


## -description

The <b>IEnhancedStorageACT2::GetDeviceName</b> method returns the device name associated with the Addressable Command Target (ACT).

## -parameters

### -param ppwszDeviceName [out]

Pointer to a string that represents the device name associated with the ACT.

## -returns

This method can return one of the following values:

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
The associated volume was successfully returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>ppwszDeviceName</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The operation failed due to insufficient memory allocation.

</td>
</tr>
</table>

## -remarks

The memory containing the device name string is allocated by the Enhanced Storage API and must be freed by passing the returned pointer to <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/ehstorapi/nn-ehstorapi-ienhancedstorageact2">IEnhancedStorageACT2</a>