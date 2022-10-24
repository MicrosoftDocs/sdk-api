---
UID: NS:propidl.tagSTATPROPSETSTG
title: STATPROPSETSTG (propidl.h)
description: The STATPROPSETSTG structure contains information about a property set. (STATPROPSETSTG structure)
helpviewer_keywords: ["STATPROPSETSTG","STATPROPSETSTG structure [Structured Storage]","_stg_statpropsetstg","propidlbase/STATPROPSETSTG","stg.statpropsetstg","tagSTATPROPSETSTG"]
old-location: stg\statpropsetstg.htm
tech.root: Stg
ms.assetid: 8e5cc502-9f96-4f4b-8729-cac4a1ffcd6f
ms.date: 08/02/2022
ms.keywords: STATPROPSETSTG, STATPROPSETSTG structure [Structured Storage], _stg_statpropsetstg, propidlbase/STATPROPSETSTG, stg.statpropsetstg, tagSTATPROPSETSTG
req.header: propidl.h
req.include-header: Propidl.h
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
req.typenames: STATPROPSETSTG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagSTATPROPSETSTG
 - propidl/tagSTATPROPSETSTG
 - STATPROPSETSTG
 - propidl/STATPROPSETSTG
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - propidlbase.h
api_name:
 - STATPROPSETSTG
---

# STATPROPSETSTG structure


## -description

The 
<b>STATPROPSETSTG</b> structure contains information about a property set. To get this information, call 
<a href="/windows/desktop/api/propidl/nf-propidl-ipropertystorage-stat">IPropertyStorage::Stat</a>, which fills in a buffer containing the information describing the current property set. To enumerate the 
<b>STATPROPSETSTG</b> structures for the property sets in the current property-set storage, call 
<a href="/windows/desktop/api/propidl/nf-propidl-ipropertysetstorage-enum">IPropertySetStorage::Enum</a> to get a pointer to an enumerator. You can then call the enumeration methods of the 
<a href="/windows/desktop/api/propidl/nn-propidl-ienumstatpropsetstg">IEnumSTATPROPSETSTG</a> interface on the enumerator. The structure is defined as follows:

## -struct-fields

### -field fmtid

FMTID of the current property set, specified when the property set was initially created.

### -field clsid

<b>CLSID</b> associated with this property set, specified when the property set was initially created and possibly modified thereafter with 
<a href="/windows/desktop/api/propidl/nf-propidl-ipropertystorage-setclass">IPropertyStorage::SetClass</a>. If not set, the value will be <b>CLSID_NULL</b>.

### -field grfFlags

Flag values of the property set, as specified in 
<a href="/windows/desktop/api/propidl/nf-propidl-ipropertysetstorage-create">IPropertySetStorage::Create</a>.

### -field mtime

Time in Universal Coordinated Time (UTC) when the property set was last modified.

### -field ctime

Time in UTC when this property set was created.

### -field atime

Time in UTC when this property set was last accessed.

### -field dwOSVersion

## -see-also

<a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a>



<a href="/windows/desktop/api/propidl/nn-propidl-ienumstatpropsetstg">IEnumSTATPROPSETSTG</a>



<a href="/windows/desktop/api/propidl/nf-propidl-ipropertysetstorage-create">IPropertySetStorage::Create</a>



<a href="/windows/desktop/api/propidl/nf-propidl-ipropertystorage-stat">IPropertyStorage::Stat</a>
