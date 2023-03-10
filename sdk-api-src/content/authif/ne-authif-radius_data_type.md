---
UID: NE:authif._RADIUS_DATA_TYPE
title: RADIUS_DATA_TYPE (authif.h)
description: The RADIUS_DATA_TYPE type enumerates the possible data type for a RADIUS attribute or extended attribute.
helpviewer_keywords: ["RADIUS_DATA_TYPE","RADIUS_DATA_TYPE enumeration [Network Policy Server]","_ias_radius_data_type","authif/RADIUS_DATA_TYPE","authif/rdtAddress","authif/rdtInteger","authif/rdtIpv6Address","authif/rdtString","authif/rdtTime","authif/rdtUnknown","ias.radius_data_type","nps.IAS_radius_data_type","rdtAddress","rdtInteger","rdtIpv6Address","rdtString","rdtTime","rdtUnknown"]
old-location: nps\IAS_radius_data_type.htm
tech.root: Nps
ms.assetid: 620d5c1f-61dc-48af-a1b2-4eaa81e358a7
ms.date: 12/05/2018
ms.keywords: RADIUS_DATA_TYPE, RADIUS_DATA_TYPE enumeration [Network Policy Server], _ias_radius_data_type, authif/RADIUS_DATA_TYPE, authif/rdtAddress, authif/rdtInteger, authif/rdtIpv6Address, authif/rdtString, authif/rdtTime, authif/rdtUnknown, ias.radius_data_type, nps.IAS_radius_data_type, rdtAddress, rdtInteger, rdtIpv6Address, rdtString, rdtTime, rdtUnknown
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
targetos: Windows
req.typenames: RADIUS_DATA_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RADIUS_DATA_TYPE
 - authif/_RADIUS_DATA_TYPE
 - RADIUS_DATA_TYPE
 - authif/RADIUS_DATA_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - AuthIf.h
api_name:
 - RADIUS_DATA_TYPE
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

<a href="/windows/desktop/Nps/ias-about-internet-authentication-service">About NPS Extensions</a>



<a href="/windows/desktop/Nps/ias-internet-authentication-service-enumerations">NPS Extensions Enumerations</a>



<a href="/windows/desktop/Nps/ias-internet-authentication-service-reference">NPS Extensions Reference</a>



<a href="/windows/desktop/api/authif/ns-authif-radius_attribute">RADIUS_ATTRIBUTE</a>



<a href="/windows/desktop/api/authif/ne-authif-radius_attribute_type">RADIUS_ATTRIBUTE_TYPE</a>