---
UID: NE:sdoias._SERVICE_TYPE
title: "_SERVICE_TYPE"
author: windows-driver-content
description: The values of the SERVICE_TYPE enumeration type specify the type of service administered from the SDO API.
old-location: nps\SDO_service_type.htm
old-project: Nps
ms.assetid: 2ac34e5c-a14c-4657-b570-2be5e13e728d
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: SERVICE_TYPE, SERVICE_TYPE enumeration [Network Policy Server], SERVICE_TYPE_IAS, SERVICE_TYPE_MAX, SERVICE_TYPE_RAMGMTSVC, SERVICE_TYPE_RAS, _SERVICE_TYPE, _sdo_service_type, nps.SDO_service_type, sdo.service_type, sdoias/SERVICE_TYPE, sdoias/SERVICE_TYPE_IAS, sdoias/SERVICE_TYPE_MAX, sdoias/SERVICE_TYPE_RAMGMTSVC, sdoias/SERVICE_TYPE_RAS
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: sdoias.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ConvertStringSidToSidW (Unicode) and ConvertStringSidToSidA (ANSI)
req.idl: SdoIas.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SERVICE_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	SdoIas.h
api_name:
-	SERVICE_TYPE
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _SERVICE_TYPE enumeration


## -description


The values of the 
<b>SERVICE_TYPE</b> enumeration type specify the type of service administered from the SDO API.


## -enum-fields




### -field SERVICE_TYPE_IAS

The service is Internet Authentication Service (IAS) or Network Policy Server (NPS).

<div class="alert"><b>Note</b>  Internet Authentication Service was renamed Network Policy Server starting with Windows Server 2008.</div>
<div> </div>

### -field SERVICE_TYPE_RAS

The service is the Remote Access Service.


### -field SERVICE_TYPE_RAMGMTSVC

The service is the Remote Access Management Service.


### -field SERVICE_TYPE_MAX

Use this constant to test whether the value is in range.


## -see-also




<a href="https://msdn.microsoft.com/265f034a-78be-4792-958e-80ad7a71d1a7">ISdoMachine::GetServiceSDO</a>
 

 

