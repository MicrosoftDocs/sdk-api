---
UID: NE:authif._RADIUS_DATA_TYPE
title: RADIUS_DATA_TYPE
author: windows-sdk-content
description: The RADIUS_DATA_TYPE type enumerates the possible data type for a RADIUS attribute or extended attribute.
old-location: nps\IAS_radius_data_type.htm
tech.root: Nps
ms.assetid: 620d5c1f-61dc-48af-a1b2-4eaa81e358a7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RADIUS_DATA_TYPE, RADIUS_DATA_TYPE enumeration [Network Policy Server], _ias_radius_data_type, authif/RADIUS_DATA_TYPE, authif/rdtAddress, authif/rdtInteger, authif/rdtIpv6Address, authif/rdtString, authif/rdtTime, authif/rdtUnknown, ias.radius_data_type, nps.IAS_radius_data_type, rdtAddress, rdtInteger, rdtIpv6Address, rdtString, rdtTime, rdtUnknown
ms.topic: enum
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
 - RADIUS_DATA_TYPE
product: Windows
targetos: Windows
req.typenames: RADIUS_DATA_TYPE
req.redist: 
---

# RADIUS_DATA_TYPE enumeration


## -description


<div class="alert"><b>Note</b>  Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.  The content of this topic applies to both IAS and NPS.</div><div> </div>The 
<b>RADIUS_DATA_TYPE</b> type enumerates the possible data type for a RADIUS attribute or extended attribute.


## -enum-fields




### -field rdtUnknown

The value is a pointer to an unknown data type.


### -field rdtString

The value of the attribute is a pointer to a character string.


### -field rdtAddress

The value of the attribute is a 32-bit <b>DWORD</b> value that represents an address.


### -field rdtInteger

The value of the attribute is a 32-bit <b>DWORD</b> value that represents an integer.


### -field rdtTime

The value of the attribute is a 32-bit <b>DWORD</b> value that represents a time.


### -field rdtIpv6Address

The value of the attribute is a <b>BYTE*</b> value that represents an IPv6 address.


## -see-also




<a href="https://msdn.microsoft.com/3d4d8d22-4cd3-48e0-b4a4-dfa0a0b7b87f">About NPS Extensions</a>



<a href="https://msdn.microsoft.com/6bf9c421-f0f6-4c75-bb4d-dbe91dcb8d01">NPS Extensions Enumerations</a>



<a href="https://msdn.microsoft.com/2b7a16cb-bc64-4e81-8149-82f51c451312">NPS Extensions Reference</a>



<a href="https://msdn.microsoft.com/7c6e1a41-9736-4bd3-b709-779d871ead57">RADIUS_ATTRIBUTE</a>



<a href="https://msdn.microsoft.com/b0b39062-0622-48f8-a06a-232713ec8c3c">RADIUS_ATTRIBUTE_TYPE</a>
 

 

