---
UID: NS:objidl.tagSTATSTG
title: STATSTG (objidl.h)
description: Contains statistical data about an open storage, stream, or byte-array object.
helpviewer_keywords: ["STATSTG","STATSTG [Strctd Stg]","STATSTG structure [Structured Storage]","_stg_statstg","objidl/STATSTG","stg.statstg","tagSTATSTG"]
old-location: stg\statstg.htm
tech.root: Stg
ms.assetid: 54e1df08-de8f-430a-bf76-e66594df4839
ms.date: 12/05/2018
ms.keywords: STATSTG, STATSTG [Strctd Stg], STATSTG structure [Structured Storage], _stg_statstg, objidl/STATSTG, stg.statstg, tagSTATSTG
req.header: objidl.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: STATSTG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagSTATSTG
 - objidl/tagSTATSTG
 - STATSTG
 - objidl/STATSTG
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Objidl.h
api_name:
 - STATSTG
---

# STATSTG structure


## -description

The 
<b>STATSTG</b> structure contains statistical data about an open storage, stream, or byte-array object. This structure is used in the 
<a href="/windows/desktop/api/objidl/nn-objidl-ienumstatstg">IEnumSTATSTG</a>, 
<a href="/windows/desktop/api/objidl/nn-objidl-ilockbytes">ILockBytes</a>, 
<a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a>, and 
<a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> interfaces.

## -struct-fields

### -field pwcsName

A pointer to a <b>NULL</b>-terminated Unicode string that contains the name. Space for this string is allocated by the method called and freed by the caller (for more information, see 
<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>). To  not return this member, specify the STATFLAG_NONAME value when you call a method that returns a 
<b>STATSTG</b> structure, except for calls to <a href="/windows/desktop/api/objidl/nn-objidl-ienumstatstg">IEnumSTATSTG::Next</a>, which provides no way to specify this value.

### -field type

Indicates the type of storage object. This is one of the values from the 
<a href="/windows/desktop/api/objidl/ne-objidl-stgty">STGTY</a> enumeration.

### -field cbSize

Specifies the size, in bytes, of the stream or byte array.

### -field mtime

Indicates the last modification time for this storage, stream, or byte array.

### -field ctime

Indicates the creation time for this storage, stream, or byte array.

### -field atime

Indicates the last access time for this storage, stream, or byte array.

### -field grfMode

Indicates the access mode specified when the object was opened. This member is only valid in calls to 
<b>Stat</b> methods.

### -field grfLocksSupported

Indicates the types of region locking supported by the stream or byte array. For more information about the values available, see the 
<a href="/windows/desktop/api/objidl/ne-objidl-locktype">LOCKTYPE</a> enumeration. This member is not used for storage objects.

### -field clsid

Indicates the class identifier for the storage object; set to CLSID_NULL for new storage objects. This member is not used for streams or byte arrays.

### -field grfStateBits

Indicates the current state bits of the storage object; that is, the value most recently set by the 
<a href="/windows/desktop/api/objidl/nf-objidl-istorage-setstatebits">IStorage::SetStateBits</a> method. This member is not valid for streams or byte arrays.

### -field reserved

Reserved for future use.

## -see-also

<a href="/windows/desktop/api/objidl/nf-objidl-istorage-setelementtimes">IStorage::SetElementTimes</a>