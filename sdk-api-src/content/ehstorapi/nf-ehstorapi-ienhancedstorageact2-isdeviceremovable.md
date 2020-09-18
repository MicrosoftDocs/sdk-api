---
UID: NF:ehstorapi.IEnhancedStorageACT2.IsDeviceRemovable
title: IEnhancedStorageACT2::IsDeviceRemovable (ehstorapi.h)
description: IEnhancedStorageACT2::IsDeviceRemovable method returns information that indicates if the device associated with the ACT is removable.
helpviewer_keywords: ["IEnhancedStorageACT2 interface [Enhanced Storage]","IsDeviceRemovable method","IEnhancedStorageACT2.IsDeviceRemovable","IEnhancedStorageACT2::IsDeviceRemovable","IsDeviceRemovable","IsDeviceRemovable method [Enhanced Storage]","IsDeviceRemovable method [Enhanced Storage]","IEnhancedStorageACT2 interface","ehstorapi/IEnhancedStorageACT2::IsDeviceRemovable","enstor.ienhancedstorageact2_isdeviceremovable"]
old-location: enstor\ienhancedstorageact2_isdeviceremovable.htm
tech.root: enstor
ms.assetid: 1118756d-56d7-4f59-8e2a-2cb970a7a62a
ms.date: 12/05/2018
ms.keywords: IEnhancedStorageACT2 interface [Enhanced Storage],IsDeviceRemovable method, IEnhancedStorageACT2.IsDeviceRemovable, IEnhancedStorageACT2::IsDeviceRemovable, IsDeviceRemovable, IsDeviceRemovable method [Enhanced Storage], IsDeviceRemovable method [Enhanced Storage],IEnhancedStorageACT2 interface, ehstorapi/IEnhancedStorageACT2::IsDeviceRemovable, enstor.ienhancedstorageact2_isdeviceremovable
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
 - IEnhancedStorageACT2::IsDeviceRemovable
 - ehstorapi/IEnhancedStorageACT2::IsDeviceRemovable
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
 - IEnhancedStorageACT2.IsDeviceRemovable
---

# IEnhancedStorageACT2::IsDeviceRemovable


## -description

The <b>IEnhancedStorageACT2::IsDeviceRemovable</b> method returns information that indicates if the device associated with the ACT is removable.

## -parameters

### -param pIsDeviceRemovable

Pointer to a boolean value that indicates if the device associated with the ACT is removable.

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
The information was successfully retrieved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pIsDeviceRemovable</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/ehstorapi/nn-ehstorapi-ienhancedstorageact2">IEnhancedStorageACT2</a>