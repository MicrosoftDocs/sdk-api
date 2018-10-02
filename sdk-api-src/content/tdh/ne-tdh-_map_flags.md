---
UID: NE:tdh._MAP_FLAGS
title: "_MAP_FLAGS"
author: windows-sdk-content
description: Defines constant values that indicate if the map is a value map, bitmap, or pattern map.
old-location: etw\map_flags_enum.htm
tech.root: ETW
ms.assetid: 3fc6935a-328a-4df3-8c2f-cd634d94ca16
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: EVENTMAP_INFO_FLAG_MANIFEST_BITMAP, EVENTMAP_INFO_FLAG_MANIFEST_PATTERNMAP, EVENTMAP_INFO_FLAG_MANIFEST_VALUEMAP, EVENTMAP_INFO_FLAG_WBEM_BITMAP, EVENTMAP_INFO_FLAG_WBEM_FLAG, EVENTMAP_INFO_FLAG_WBEM_NO_MAP, EVENTMAP_INFO_FLAG_WBEM_VALUEMAP, MAP_FLAGS, MAP_FLAGS enumeration [ETW], _MAP_FLAGS, etw.map_flags_enum, tdh.map_flags_enum, tdh/EVENTMAP_INFO_FLAG_MANIFEST_BITMAP, tdh/EVENTMAP_INFO_FLAG_MANIFEST_PATTERNMAP, tdh/EVENTMAP_INFO_FLAG_MANIFEST_VALUEMAP, tdh/EVENTMAP_INFO_FLAG_WBEM_BITMAP, tdh/EVENTMAP_INFO_FLAG_WBEM_FLAG, tdh/EVENTMAP_INFO_FLAG_WBEM_NO_MAP, tdh/EVENTMAP_INFO_FLAG_WBEM_VALUEMAP, tdh/MAP_FLAGS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tdh.h
api_name:
 - MAP_FLAGS
product: Windows
targetos: Windows
req.typenames: MAP_FLAGS
req.redist: 
---

# _MAP_FLAGS enumeration


## -description


Defines constant values that indicate if the map is a value map, bitmap, or pattern map.


## -enum-fields




### -field EVENTMAP_INFO_FLAG_MANIFEST_VALUEMAP

The manifest value map maps integer values to strings. For details, see the <a href="https://msdn.microsoft.com/208ae219-8f79-4049-b946-a57b33c97b1b">MapType</a> complex type.


### -field EVENTMAP_INFO_FLAG_MANIFEST_BITMAP

The manifest value map maps bit values to strings. For details, see the <a href="https://msdn.microsoft.com/208ae219-8f79-4049-b946-a57b33c97b1b">MapType</a> complex type.


### -field EVENTMAP_INFO_FLAG_MANIFEST_PATTERNMAP

The manifest value map uses regular expressions to map one name to another name. For details, see the <a href="https://msdn.microsoft.com/184b6aeb-a554-4a92-b19e-1849c711d33b">PatternMapType</a> complex type.


### -field EVENTMAP_INFO_FLAG_WBEM_VALUEMAP

The WMI value map maps integer values to strings. For details, see <a href="https://msdn.microsoft.com/7667e87f-b997-4fd9-81ea-b27c9d2a9335">ValueMap and Value Qualifiers</a>. 


### -field EVENTMAP_INFO_FLAG_WBEM_BITMAP

The WMI value map maps bit values to strings. For details, see <a href="https://msdn.microsoft.com/14c34909-2419-41a1-a1ed-3b647a3c5e75">BitMap and BitValue Qualifiers</a>.


### -field EVENTMAP_INFO_FLAG_WBEM_FLAG

This flag can be combined with the EVENTMAP_INFO_FLAG_WBEM_VALUEMAP flag to indicate that the ValueMap qualifier contains bit (flag) values instead of index values.


### -field EVENTMAP_INFO_FLAG_WBEM_NO_MAP

This flag can be combined with the EVENTMAP_INFO_FLAG_WBEM_VALUEMAP or EVENTMAP_INFO_FLAG_WBEM_BITMAP flag to indicate that the MOF class property contains a BitValues or Values qualifier but does not contain the BitMap or ValueMap qualifier.


## -remarks



The following MOF example shows the flags that are set based on the WMI property attributes used. 

<pre class="syntax" xml:space="preserve"><code>Sets the EVENTMAP_INFO_FLAG_WBEM_VALUEMAP and EVENTMAP_INFO_FLAG_WBEM_NO_MAP flags.
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
uint32  Data6;</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/dc7f14e7-16d7-4dfc-8c1a-5db6fa999d98">EVENT_MAP_INFO</a>
 

 

