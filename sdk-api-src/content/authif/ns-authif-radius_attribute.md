---
UID: NS:authif._RADIUS_ATTRIBUTE
title: RADIUS_ATTRIBUTE (authif.h)
author: windows-sdk-content
description: The RADIUS_ATTRIBUTE structure represents a RADIUS attribute or an extended attribute.
old-location: nps\IAS_radius_attribute.htm
tech.root: Nps
ms.assetid: 7c6e1a41-9736-4bd3-b709-779d871ead57
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PRADIUS_ATTRIBUTE, PRADIUS_ATTRIBUTE, PRADIUS_ATTRIBUTE structure pointer [Network Policy Server], RADIUS_ATTRIBUTE, RADIUS_ATTRIBUTE structure [Network Policy Server], _ias_radius_attribute, authif/PRADIUS_ATTRIBUTE, authif/RADIUS_ATTRIBUTE, ias.radius_attribute, nps.IAS_radius_attribute"
ms.topic: struct
req.header: authif.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
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
 - AuthIf.h
api_name:
 - RADIUS_ATTRIBUTE
product: Windows
targetos: Windows
req.typenames: RADIUS_ATTRIBUTE, *PRADIUS_ATTRIBUTE
req.redist: 
---

# RADIUS_ATTRIBUTE structure


## -description


<div class="alert"><b>Note</b>  Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.  The content of this topic applies to both IAS and NPS.</div><div> </div>The 
<b>RADIUS_ATTRIBUTE</b> structure represents a RADIUS attribute or an extended attribute.


## -struct-fields




### -field dwAttrType

Stores a value from the 
<a href="https://msdn.microsoft.com/b0b39062-0622-48f8-a06a-232713ec8c3c">RADIUS_ATTRIBUTE_TYPE</a> enumeration. This value specifies the type of the attribute represented by the 
<b>RADIUS_ATTRIBUTE</b> structure.


### -field fDataType

Stores a value from the 
<a href="https://msdn.microsoft.com/620d5c1f-61dc-48af-a1b2-4eaa81e358a7">RADIUS_DATA_TYPE</a> enumeration. This value specifies the type of the value stored in the union that contains the <b>dwValue</b> and <b>lpValue</b> members.


### -field cbDataLength

Stores the length, in bytes, of the data. The <b>cbDataLength</b> member is used only if <b>lpValue</b> member is used.


### -field dwValue

Stores a value of type <b>DWORD</b>. The <b>dwValue</b> member is used if the <b>fDataType</b> member specifies <b>rdtAddress</b>, <b>rdtInteger</b>, or <b>rdtTime</b>.

<div class="alert"><b>Note</b>  In Windows Server 2008 the byte order format of dwValue is represented in network byte order (big-endian) when <b>fDataType</b> is specified as <b>rdtAddress</b>.  Previous Windows versions represented network addressing using the little-endian format.</div>
<div> </div>

### -field lpValue

Stores a multi-byte data value. The <b>lpValue</b> member is used if the <b>fDataType</b> member specifies <b>rdtUnknown</b>,  <b>rdtIpv6Address</b>, or <b>rdtString</b>.


## -see-also




<a href="https://msdn.microsoft.com/3d4d8d22-4cd3-48e0-b4a4-dfa0a0b7b87f">About NPS Extensions</a>



<a href="https://msdn.microsoft.com/2b7a16cb-bc64-4e81-8149-82f51c451312">NPS Extensions Reference</a>



<a href="https://msdn.microsoft.com/8b13a21c-edbe-4982-8718-a34d62ecc38d">NPS Extensions Structures</a>



<a href="https://msdn.microsoft.com/b0b39062-0622-48f8-a06a-232713ec8c3c">RADIUS_ATTRIBUTE_TYPE</a>



<a href="https://msdn.microsoft.com/620d5c1f-61dc-48af-a1b2-4eaa81e358a7">RADIUS_DATA_TYPE</a>
 

 

