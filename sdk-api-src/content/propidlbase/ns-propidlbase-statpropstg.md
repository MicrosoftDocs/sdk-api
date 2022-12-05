---
UID: NS:propidlbase.tagSTATPROPSTG
title: STATPROPSTG (propidlbase.h)
description: The STATPROPSTG structure contains data about a single property in a property set. This data is the property ID and type tag, and the optional string name that may be associated with the property. 
helpviewer_keywords: ["STATPROPSTG","STATPROPSTG [Strctd Stg]","STATPROPSTG structure [Structured Storage]","_stg_statpropstg","propidlbase/STATPROPSTG","stg.statpropstg","tagSTATPROPSTG"]
old-location: stg\statpropstg.htm
tech.root: Stg
ms.assetid: 3b8de6d3-18a3-4c0a-94d1-04bcec05d41a
ms.date: 08/02/2022
ms.keywords: STATPROPSTG, STATPROPSTG [Strctd Stg], STATPROPSTG structure [Structured Storage], _stg_statpropstg, propidlbase/STATPROPSTG, stg.statpropstg, tagSTATPROPSTG
req.header: propidlbase.h
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
req.typenames: STATPROPSTG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagSTATPROPSTG
 - propidlbase/tagSTATPROPSTG
 - STATPROPSTG
 - propidlbase/STATPROPSTG
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
 - STATPROPSTG
---

# STATPROPSTG structure


## -description

The 
<b>STATPROPSTG</b> structure contains data about a single property in a property set. This data is the property ID and type tag, and the optional string name that may be associated with the property.


<a href="/windows/desktop/api/propidl/nf-propidl-ipropertystorage-enum">IPropertyStorage::Enum</a> supplies a pointer to the 
<a href="/windows/desktop/api/propidl/nn-propidl-ienumstatpropstg">IEnumSTATPROPSTG</a> interface on an enumerator object that can be used to enumerate the 
<b>STATPROPSTG</b> structures for the properties in the current property set. 
<b>STATPROPSTG</b> is defined as:

## -struct-fields

### -field lpwstrName

A wide-character null-terminated Unicode string that contains the optional string name associated with the property. May be <b>NULL</b>. This member must be freed using 
<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

### -field propid

A 32-bit identifier that uniquely identifies the property within the property set. All properties within property sets must have unique property identifiers.

### -field vt

The property type.

## -see-also

<a href="/windows/desktop/api/propidl/nn-propidl-ienumstatpropstg">IEnumSTATPROPSTG</a>



<a href="/windows/desktop/api/propidl/nf-propidl-ipropertystorage-enum">IPropertyStorage::Enum</a>
