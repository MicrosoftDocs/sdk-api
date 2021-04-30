---
UID: NS:resapi.RESUTIL_PROPERTY_ITEM
title: RESUTIL_PROPERTY_ITEM (resapi.h)
description: Contains information about a cluster object property. An array of RESUTIL_PROPERTY_ITEM structures forms a property table which can be used in property operations.
helpviewer_keywords: ["*PRESUTIL_PROPERTY_ITEM","PRESUTIL_PROPERTY_ITEM","PRESUTIL_PROPERTY_ITEM structure pointer [Failover Cluster]","RESUTIL_PROPERTY_ITEM","RESUTIL_PROPERTY_ITEM structure [Failover Cluster]","RESUTIL_PROPITEM_READ_ONLY","RESUTIL_PROPITEM_REQUIRED","RESUTIL_PROPITEM_SIGNED","_wolf_resutil_property_item","mscs.resutil_property_item","resapi/PRESUTIL_PROPERTY_ITEM","resapi/RESUTIL_PROPERTY_ITEM"]
old-location: mscs\resutil_property_item.htm
tech.root: MsCS
ms.assetid: f65ee50f-59f7-44db-ad69-b29b3e693c7e
ms.date: 12/05/2018
ms.keywords: '*PRESUTIL_PROPERTY_ITEM, PRESUTIL_PROPERTY_ITEM, PRESUTIL_PROPERTY_ITEM structure pointer [Failover Cluster], RESUTIL_PROPERTY_ITEM, RESUTIL_PROPERTY_ITEM structure [Failover Cluster], RESUTIL_PROPITEM_READ_ONLY, RESUTIL_PROPITEM_REQUIRED, RESUTIL_PROPITEM_SIGNED, _wolf_resutil_property_item, mscs.resutil_property_item, resapi/PRESUTIL_PROPERTY_ITEM, resapi/RESUTIL_PROPERTY_ITEM'
req.header: resapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
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
req.typenames: RESUTIL_PROPERTY_ITEM, *PRESUTIL_PROPERTY_ITEM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RESUTIL_PROPERTY_ITEM
 - resapi/RESUTIL_PROPERTY_ITEM
 - PRESUTIL_PROPERTY_ITEM
 - resapi/PRESUTIL_PROPERTY_ITEM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ResApi.h
api_name:
 - RESUTIL_PROPERTY_ITEM
---

# RESUTIL_PROPERTY_ITEM structure


## -description

Contains 
    information about a cluster object property. An array of 
    <b>RESUTIL_PROPERTY_ITEM</b> structures forms a 
    <a href="/previous-versions/windows/desktop/mscs/property-tables">property table</a> which can be used in property operations.

## -struct-fields

### -field Name

The name of the property.

### -field KeyName

Optional name of the <a href="/previous-versions/windows/desktop/mscs/cluster-database">cluster database</a> subkey for 
      the property. This parameter can be <b>NULL</b>.

### -field Format

Describes the format of the property such as <b>CLUSPROP_FORMAT_BINARY</b> or 
      <b>CLUSPROP_FORMAT_DWORD</b>. For a list of valid format values, see the 
      <b>wFormat</b> member of 
      <a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_syntax">CLUSPROP_SYNTAX</a>.

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.DefaultPtr

### -field DUMMYUNIONNAME.Default

### -field DUMMYUNIONNAME.lpDefault

### -field DUMMYUNIONNAME.LargeIntData

### -field DUMMYUNIONNAME.ULargeIntData

### -field DUMMYUNIONNAME.FileTimeData

### -field Minimum

Minimum data value for the property. For data values with the 
      <b>CLUSPROP_FORMAT_BINARY</b> and <b>CLUSPROP_FORMAT_MULTI_SZ</b> 
      formats, the <b>Minimum</b> member contains the byte size of the default data value 
      specified by <b>Default</b>.

### -field Maximum

Maximum data value for the property.

### -field Flags

Bitmask that describes the property.



#### RESUTIL_PROPITEM_READ_ONLY (0x00000001)

The property is <a href="/previous-versions/windows/desktop/mscs/read-only-properties">read-only</a>.



#### RESUTIL_PROPITEM_REQUIRED (0x00000002)

The property is required.



#### RESUTIL_PROPITEM_SIGNED (0x00000004)

Flags a numeric property as a signed value.

### -field Offset

Byte offset to the actual property data. The data is stored in a buffer known as a parameter block.


#### - ( unnamed union )

The default value of the property in one of the following forms.



#### DefaultPtr

Pointer to a <b>DWORD</b> default value.



#### Default

A <b>DWORD</b> default value.



#### lpDefault

Void pointer to a buffer containing the default value.



#### LargeIntData

Pointer to a <a href="/previous-versions/windows/desktop/api/resapi/ns-resapi-resutil_largeint_data">RESUTIL_LARGEINT_DATA</a> 
       structure describing the maximum, minimum, and default values for a signed large integer.



#### ULargeIntData

Pointer to a <a href="/previous-versions/windows/desktop/api/resapi/ns-resapi-resutil_ulargeint_data">RESUTIL_ULARGEINT_DATA</a> 
       structure describing the maximum, minimum, and default values for an unsigned large integer. The default value 
       must be consistent with the format specified by the <b>Format</b> member.



#### FileTimeData

Pointer to a <a href="/previous-versions/windows/desktop/api/resapi/ns-resapi-resutil_filetime_data">RESUTIL_FILETIME_DATA</a> 
       structure describing the file data and time data.

## -remarks

For more information about building parameter blocks and property tables, see 
    <a href="/previous-versions/windows/desktop/mscs/using-lists-and-tables">Using Lists and Tables</a>.


#### Examples

See <a href="/previous-versions/windows/desktop/mscs/using-lists-and-tables">Using Lists and Tables</a> and 
     <a href="/previous-versions/windows/desktop/mscs/building-with-clusprop-buffer-helper">Building with CLUSPROP_BUFFER_HELPER</a>, 
     and <a href="/previous-versions/windows/desktop/mscs/defining-structures-and-constants">Defining Structures and Constants</a> in 
     <a href="/previous-versions/windows/desktop/mscs/implementing-resource-dlls">Implementing Resource DLLs</a>.

<div class="code"></div>

## -see-also

<a href="/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_syntax">CLUSPROP_SYNTAX</a>