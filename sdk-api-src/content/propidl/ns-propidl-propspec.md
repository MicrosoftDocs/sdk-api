---
UID: NS:propidl.tagPROPSPEC
title: PROPSPEC (propidl.h)
description: The PROPSPEC structure is used by many of the methods of IPropertyStorage to specify a property either by its property identifier (ID) or the associated string name. 
helpviewer_keywords: ["PROPSPEC","PROPSPEC [Strctd Stg]","PROPSPEC structure [Structured Storage]","PRSPEC_LPWSTR","PRSPEC_PROPID","_stg_propspec","propidlbase/PROPSPEC","stg.propspec","tagPROPSPEC"]
old-location: stg\propspec.htm
tech.root: Stg
ms.assetid: 5bb3b9c6-ab82-498c-94f9-13a9ffa7452b
ms.date: 08/02/2022
ms.keywords: PROPSPEC, PROPSPEC [Strctd Stg], PROPSPEC structure [Structured Storage], PRSPEC_LPWSTR, PRSPEC_PROPID, _stg_propspec, propidlbase/PROPSPEC, stg.propspec, tagPROPSPEC
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
req.typenames: PROPSPEC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagPROPSPEC
 - propidl/tagPROPSPEC
 - PROPSPEC
 - propidl/PROPSPEC
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
 - PROPSPEC
---

# PROPSPEC structure


## -description

The 
<b>PROPSPEC</b> structure is used by many of the methods of 
<a href="/windows/desktop/api/propidl/nn-propidl-ipropertystorage">IPropertyStorage</a> to specify a property either by its property identifier (ID) or the associated string name.

## -struct-fields

### -field ulKind

Indicates the union member used. This member can be one of the following values.

<table>
<tr>
<th>Name</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PRSPEC_LPWSTR"></a><a id="prspec_lpwstr"></a><dl>
<dt><b>PRSPEC_LPWSTR</b></dt>
<dt>Value:  0</dt>
</dl>
</td>
<td width="60%">
The <b>lpwstr</b> member is used and set to a string name.

</td>
</tr>
<tr>
<td width="40%"><a id="PRSPEC_PROPID"></a><a id="prspec_propid"></a><dl>
<dt><b>PRSPEC_PROPID</b></dt>
<dt>Value:  1</dt>
</dl>
</td>
<td width="60%">
The <b>propid</b> member is used and set to a property ID value.

</td>
</tr>
</table>

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.propid

Specifies the value of the property ID. Use either this value or the following <b>lpwstr</b>, not both.

### -field DUMMYUNIONNAME.lpwstr

Specifies the string name of the property as a null-terminated Unicode string.

## -remarks

String names are optional and can be assigned to a set of properties when the property is created with a call to <a href="/windows/desktop/api/propidl/nf-propidl-ipropertystorage-writemultiple">IPropertyStorage::WriteMultiple</a> or later with a call to <a href="/windows/desktop/api/propidl/nf-propidl-ipropertystorage-writepropertynames">IPropertyStorage::WritePropertyNames</a>.

## -see-also

<a href="/windows/desktop/api/propidl/nn-propidl-ipropertystorage">IPropertyStorage</a>
