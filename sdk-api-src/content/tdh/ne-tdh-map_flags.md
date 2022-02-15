---
UID: NE:tdh._MAP_FLAGS
title: MAP_FLAGS (tdh.h)
description: Defines constant values that indicate if the map is a value map, bitmap, or pattern map.
helpviewer_keywords: ["EVENTMAP_INFO_FLAG_MANIFEST_BITMAP","EVENTMAP_INFO_FLAG_MANIFEST_PATTERNMAP","EVENTMAP_INFO_FLAG_MANIFEST_VALUEMAP","EVENTMAP_INFO_FLAG_WBEM_BITMAP","EVENTMAP_INFO_FLAG_WBEM_FLAG","EVENTMAP_INFO_FLAG_WBEM_NO_MAP","EVENTMAP_INFO_FLAG_WBEM_VALUEMAP","MAP_FLAGS","MAP_FLAGS enumeration [ETW]","etw.map_flags_enum","tdh.map_flags_enum","tdh/EVENTMAP_INFO_FLAG_MANIFEST_BITMAP","tdh/EVENTMAP_INFO_FLAG_MANIFEST_PATTERNMAP","tdh/EVENTMAP_INFO_FLAG_MANIFEST_VALUEMAP","tdh/EVENTMAP_INFO_FLAG_WBEM_BITMAP","tdh/EVENTMAP_INFO_FLAG_WBEM_FLAG","tdh/EVENTMAP_INFO_FLAG_WBEM_NO_MAP","tdh/EVENTMAP_INFO_FLAG_WBEM_VALUEMAP","tdh/MAP_FLAGS"]
old-location: etw\map_flags_enum.htm
tech.root: ETW
ms.assetid: 3fc6935a-328a-4df3-8c2f-cd634d94ca16
ms.date: 12/05/2018
ms.keywords: EVENTMAP_INFO_FLAG_MANIFEST_BITMAP, EVENTMAP_INFO_FLAG_MANIFEST_PATTERNMAP, EVENTMAP_INFO_FLAG_MANIFEST_VALUEMAP, EVENTMAP_INFO_FLAG_WBEM_BITMAP, EVENTMAP_INFO_FLAG_WBEM_FLAG, EVENTMAP_INFO_FLAG_WBEM_NO_MAP, EVENTMAP_INFO_FLAG_WBEM_VALUEMAP, MAP_FLAGS, MAP_FLAGS enumeration [ETW], etw.map_flags_enum, tdh.map_flags_enum, tdh/EVENTMAP_INFO_FLAG_MANIFEST_BITMAP, tdh/EVENTMAP_INFO_FLAG_MANIFEST_PATTERNMAP, tdh/EVENTMAP_INFO_FLAG_MANIFEST_VALUEMAP, tdh/EVENTMAP_INFO_FLAG_WBEM_BITMAP, tdh/EVENTMAP_INFO_FLAG_WBEM_FLAG, tdh/EVENTMAP_INFO_FLAG_WBEM_NO_MAP, tdh/EVENTMAP_INFO_FLAG_WBEM_VALUEMAP, tdh/MAP_FLAGS
req.header: tdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: MAP_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MAP_FLAGS
 - tdh/_MAP_FLAGS
 - MAP_FLAGS
 - tdh/MAP_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tdh.h
api_name:
 - MAP_FLAGS
---

# MAP_FLAGS enumeration


## -description

Defines constant values that indicate if the map is a value map, bitmap, or pattern map.

## -enum-fields

### -field EVENTMAP_INFO_FLAG_MANIFEST_VALUEMAP:0x1

The manifest value map maps integer values to strings. For details, see the <a href="/windows/desktop/WES/eventmanifestschema-maptype-complextype">MapType</a> complex type.

### -field EVENTMAP_INFO_FLAG_MANIFEST_BITMAP:0x2

The manifest value map maps bit values to strings. For details, see the <a href="/windows/desktop/WES/eventmanifestschema-maptype-complextype">MapType</a> complex type.

### -field EVENTMAP_INFO_FLAG_MANIFEST_PATTERNMAP:0x4

The manifest value map uses regular expressions to map one name to another name. For details, see the <a href="/windows/desktop/WES/eventmanifestschema-patternmaptype-complextype">PatternMapType</a> complex type.

### -field EVENTMAP_INFO_FLAG_WBEM_VALUEMAP:0x8

The WMI value map maps integer values to strings. For details, see <a href="/windows/desktop/WmiSdk/value-map">ValueMap and Value Qualifiers</a>.

### -field EVENTMAP_INFO_FLAG_WBEM_BITMAP:0x10

The WMI value map maps bit values to strings. For details, see <a href="/windows/desktop/WmiSdk/bitmap-and-bitvalues">BitMap and BitValue Qualifiers</a>.

### -field EVENTMAP_INFO_FLAG_WBEM_FLAG:0x20

This flag can be combined with the EVENTMAP_INFO_FLAG_WBEM_VALUEMAP flag to indicate that the ValueMap qualifier contains bit (flag) values instead of index values.

### -field EVENTMAP_INFO_FLAG_WBEM_NO_MAP:0x40

This flag can be combined with the EVENTMAP_INFO_FLAG_WBEM_VALUEMAP or EVENTMAP_INFO_FLAG_WBEM_BITMAP flag to indicate that the MOF class property contains a BitValues or Values qualifier but does not contain the BitMap or ValueMap qualifier.

## -remarks

The following MOF example shows the flags that are set based on the WMI property attributes used. 


``` syntax
Sets the EVENTMAP_INFO_FLAG_WBEM_VALUEMAP and EVENTMAP_INFO_FLAG_WBEM_NO_MAP flags.
[WmiDataId(1),
Values {"ValueIndex1", "ValueIndex2", "ValueIndex3"}] 
uint32  Data1;

Sets the EVENTMAP_INFO_FLAG_WBEM_VALUEMAP flag.
[WmiDataId(2),
ValueMap {"1", "3", "5", "0", "-1"},
Values {"ValueMap1", "ValueMap3", "ValueMap5", "ValueMap0", "ValueMap-1", "Other"}] 
sint32  Data2;

Sets the EVENTMAP_INFO_FLAG_WBEM_VALUEMAP and EVENTMAP_INFO_FLAG_WBEM_FLAG flags.
[WmiDataId(3),
ValueType("flag"),
ValueMap {"0x01", "0x02", "0x04", "0x08"},
Values {"ValueMapFlag1", "ValueMapFlag2", "ValueMapFlag4", "ValueMapFlag8"}]
uint32  Data3;

Sets the EVENTMAP_INFO_FLAG_WBEM_VALUEMAP flag.
[WmiDataId(4),
ValueType("index"),
ValueMap {"1", "3", "5", "0", "-1"},
Values {"ValueMapIndex1", "ValueMapIndex3", "ValueMapIndex5", "ValueMapIndex0", "ValueMapIndex-1"}]
sint32  Data4;

Sets the EVENTMAP_INFO_FLAG_WBEM_BITMAP and EVENTMAP_INFO_FLAG_WBEM_NO_MAP flags.
[WmiDataId(5),
BitValues {"BitValueIndex1", "BitValueIndex2", "BitValueIndex3"}]
uint32  Data5;

Sets the EVENTMAP_INFO_FLAG_WBEM_BITMAP flag
[WmiDataId(6),
BitMap {"1", "3", "5", "0"},
BitValues {"BitMap1", "BitMap3", "BitMap5", "BitMap0", "Other"}]
uint32  Data6;
```


## -see-also

<a href="/windows/desktop/api/tdh/ns-tdh-event_map_info">EVENT_MAP_INFO</a>
