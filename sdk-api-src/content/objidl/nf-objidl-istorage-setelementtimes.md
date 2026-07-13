---
UID: NF:objidl.IStorage.SetElementTimes
title: IStorage::SetElementTimes (objidl.h)
description: The SetElementTimes method sets the modification, access, and creation times of the specified storage element, if the underlying file system supports this method.
helpviewer_keywords: ["IStorage interface [Structured Storage]","SetElementTimes method","IStorage.SetElementTimes","IStorage::SetElementTimes","SetElementTimes","SetElementTimes method [Structured Storage]","SetElementTimes method [Structured Storage]","IStorage interface","_stg_istorage_setelementtimes","objidl/IStorage::SetElementTimes","stg.istorage_setelementtimes"]
old-location: stg\istorage_setelementtimes.htm
tech.root: Stg
ms.assetid: f6a1fba4-0444-4de3-a838-2d339878fe24
ms.date: 12/05/2018
ms.keywords: IStorage interface [Structured Storage],SetElementTimes method, IStorage.SetElementTimes, IStorage::SetElementTimes, SetElementTimes, SetElementTimes method [Structured Storage], SetElementTimes method [Structured Storage],IStorage interface, _stg_istorage_setelementtimes, objidl/IStorage::SetElementTimes, stg.istorage_setelementtimes
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Objidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IStorage::SetElementTimes
 - objidl/IStorage::SetElementTimes
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ole32.dll
api_name:
 - IStorage.SetElementTimes
---

# IStorage::SetElementTimes


## -description

The <b>SetElementTimes</b>  method sets the modification, access, and creation times of the specified storage element, if the underlying file system supports this method.

## -parameters

### -param pwcsName [in]

The name of the storage object element whose times are to be modified. If <b>NULL</b>, the time is set on the root storage rather than one of its elements.

### -param pctime [in]

Either the new creation time for the element or <b>NULL</b> if the creation time is not to be modified.

### -param patime [in]

Either the new access time for the element or <b>NULL</b> if the access time is not to be modified.

### -param pmtime [in]

Either the new modification time for the element or <b>NULL</b> if the modification time is not to be modified.

## -returns

This method can return one of these values.

| Return code | Description |
|----------------|---------------|
|S_OK | The time values were successfully set.|
|E_PENDING | Asynchronous Storage only: Part or all of the element's data is currently unavailable.|
|STG_E_ACCESSDENIED | The caller does not have enough permissions for changing the element.|
|STG_E_FILENOTFOUND | The element with the specified name does not exist.|
|STG_E_INSUFFICIENTMEMORY | The element was not changed due to a lack of memory.|
|STG_E_INVALIDNAME | Not a valid value for the element name.|
|STG_E_INVALIDPOINTER | The pointer specified for the element was not valid.|
|STG_E_INVALIDPARAMETER | One of the parameters was not valid.|
|STG_E_TOOMANYOPENFILES | The element was not changed because there are too many open files.|
|STG_E_REVERTED | The storage object has been invalidated by a revert operation above it in the transaction tree.|

## -remarks

<b>SetElementTimes</b>  sets time statistics for the specified storage element within this storage object.

Not all file systems support all the time values. This method sets those times that are supported and ignores the rest. Each time-value parameter can be <b>NULL</b>; indicating that no modification should occur.

Call the 
<a href="/windows/desktop/api/objidl/nf-objidl-istorage-stat">IStorage::Stat</a> method to retrieve these time values.

## -see-also

<a href="/windows/desktop/Stg/istorage-compound-file-implementation">IStorage - Compound File Implementation</a>



<a href="/windows/desktop/api/objidl/nf-objidl-istorage-stat">IStorage::Stat</a>