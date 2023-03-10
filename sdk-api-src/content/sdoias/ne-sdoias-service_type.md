---
UID: NE:sdoias._SERVICE_TYPE
title: SERVICE_TYPE (sdoias.h)
description: The values of the SERVICE_TYPE enumeration type specify the type of service administered from the SDO API.
helpviewer_keywords: ["SERVICE_TYPE","SERVICE_TYPE enumeration [Network Policy Server]","SERVICE_TYPE_IAS","SERVICE_TYPE_MAX","SERVICE_TYPE_RAMGMTSVC","SERVICE_TYPE_RAS","_sdo_service_type","nps.SDO_service_type","sdo.service_type","sdoias/SERVICE_TYPE","sdoias/SERVICE_TYPE_IAS","sdoias/SERVICE_TYPE_MAX","sdoias/SERVICE_TYPE_RAMGMTSVC","sdoias/SERVICE_TYPE_RAS"]
old-location: nps\SDO_service_type.htm
tech.root: Nps
ms.assetid: 2ac34e5c-a14c-4657-b570-2be5e13e728d
ms.date: 12/05/2018
ms.keywords: SERVICE_TYPE, SERVICE_TYPE enumeration [Network Policy Server], SERVICE_TYPE_IAS, SERVICE_TYPE_MAX, SERVICE_TYPE_RAMGMTSVC, SERVICE_TYPE_RAS, _sdo_service_type, nps.SDO_service_type, sdo.service_type, sdoias/SERVICE_TYPE, sdoias/SERVICE_TYPE_IAS, sdoias/SERVICE_TYPE_MAX, sdoias/SERVICE_TYPE_RAMGMTSVC, sdoias/SERVICE_TYPE_RAS
req.header: sdoias.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: SdoIas.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SERVICE_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SERVICE_TYPE
 - sdoias/_SERVICE_TYPE
 - SERVICE_TYPE
 - sdoias/SERVICE_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - SdoIas.h
api_name:
 - SERVICE_TYPE
---

# SERVICE_TYPE enumeration


## -description

The values of the 
<b>SERVICE_TYPE</b> enumeration type specify the type of service administered from the SDO API.

## -enum-fields

### -field SERVICE_TYPE_IAS:0

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

<a href="/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo">ISdoMachine::GetServiceSDO</a>
