---
UID: NF:propidl.IPropertyStorage.SetTimes
title: IPropertyStorage::SetTimes (propidl.h)
description: The IPropertyStorage::SetTimes method sets the modification, access, and creation times of this property set, if supported by the implementation.
helpviewer_keywords: ["IPropertyStorage interface [Structured Storage]","SetTimes method","IPropertyStorage.SetTimes","IPropertyStorage::SetTimes","SetTimes","SetTimes method [Structured Storage]","SetTimes method [Structured Storage]","IPropertyStorage interface","_stg_ipropertystorage_settimes","propidl/IPropertyStorage::SetTimes","stg.ipropertystorage_settimes"]
old-location: stg\ipropertystorage_settimes.htm
tech.root: Stg
ms.assetid: 23c7040a-e648-4898-806d-ad01d7027cc6
ms.date: 08/02/2022
ms.keywords: IPropertyStorage interface [Structured Storage],SetTimes method, IPropertyStorage.SetTimes, IPropertyStorage::SetTimes, SetTimes, SetTimes method [Structured Storage], SetTimes method [Structured Storage],IPropertyStorage interface, _stg_ipropertystorage_settimes, propidl/IPropertyStorage::SetTimes, stg.ipropertystorage_settimes
req.header: propidl.h
req.include-header: Objbase.h, Propidlbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IPropertyStorage::SetTimes
 - propidl/IPropertyStorage::SetTimes
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
 - IPropertyStorage.SetTimes
---

# IPropertyStorage::SetTimes


## -description

The <b>SetTimes</b> method sets the modification, access, and creation times of this property set, if supported by the implementation. Not all implementations support all these time values.

## -parameters

### -param pctime [in]

Pointer to the new creation time for the property set. May be <b>NULL</b>, indicating that this time is not to be modified by this call.

### -param patime [in]

Pointer to the new access time for the property set. May be <b>NULL</b>, indicating that this time is not to be modified by this call.

### -param pmtime [in]

Pointer to the new modification time for the property set. May be <b>NULL</b>, indicating that this time is not to be modified by this call.

## -returns

This method supports the standard return value E_UNEXPECTED, in addition to the following:

## -remarks

Sets the modification, access, and creation times of the current open property set, if supported by the implementation (not all implementations support all these time values). Unsupported time stamps are always reported as zero, enabling the caller to test for support. A call to <a href="/windows/desktop/api/propidl/nf-propidl-ipropertystorage-stat">IPropertyStorage::Stat</a> supplies (among other data) time-stamp information.

Notice that this functionality is provided as an 
<a href="/windows/desktop/api/propidl/nn-propidl-ipropertystorage">IPropertyStorage</a> method on a property-storage object that is already open, in contrast to being provided as a method in 
<a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage">IPropertySetStorage</a>. Normally, when the 
<b>SetTimes</b> method is not explicitly called, the access and modification times are updated as a side effect of reading and writing the property set. When 
 <b>SetTimes</b> is used, the latest specified times supersede either default times or time values specified in previous calls to 
<b>SetTimes</b>.

## -see-also

<a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a>



<a href="/windows/desktop/api/propidl/nn-propidl-ipropertystorage">IPropertyStorage</a>



<a href="/windows/desktop/api/propidl/nf-propidl-ipropertystorage-stat">IPropertyStorage::Stat</a>
