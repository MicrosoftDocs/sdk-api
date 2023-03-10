---
UID: NS:nspapi._SERVICE_ADDRESSES
title: SERVICE_ADDRESSES (nspapi.h)
description: The SERVICE_ADDRESSES structure contains an array of SERVICE_ADDRESS data structures.
helpviewer_keywords: ["*LPSERVICE_ADDRESSES","*PSERVICE_ADDRESSES","SERVICE_ADDRESSES","SERVICE_ADDRESSES structure [Winsock]","_win32_service_addresses_2","nspapi/SERVICE_ADDRESSES","winsock.service_addresses_2"]
old-location: winsock\service_addresses_2.htm
tech.root: WinSock
ms.assetid: 1ed0c634-4f09-49c1-8fbf-9182d6a4bd51
ms.date: 12/05/2018
ms.keywords: '*LPSERVICE_ADDRESSES, *PSERVICE_ADDRESSES, SERVICE_ADDRESSES, SERVICE_ADDRESSES structure [Winsock], _win32_service_addresses_2, nspapi/SERVICE_ADDRESSES, winsock.service_addresses_2'
req.header: nspapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: SERVICE_ADDRESSES, *PSERVICE_ADDRESSES, *LPSERVICE_ADDRESSES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SERVICE_ADDRESSES
 - nspapi/_SERVICE_ADDRESSES
 - PSERVICE_ADDRESSES
 - nspapi/PSERVICE_ADDRESSES
 - SERVICE_ADDRESSES
 - nspapi/SERVICE_ADDRESSES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Nspapi.h
api_name:
 - SERVICE_ADDRESSES
---

# SERVICE_ADDRESSES structure


## -description

The 
<b>SERVICE_ADDRESSES</b> structure contains an array of 
<a href="/windows/desktop/api/nspapi/ns-nspapi-service_address">SERVICE_ADDRESS</a> data structures.

## -struct-fields

### -field dwAddressCount

Number of 
<a href="/windows/desktop/api/nspapi/ns-nspapi-service_address">SERVICE_ADDRESS</a> structures in the <b>Addresses</b> array.

### -field Addresses

### -field Addresses.size_is

### -field Addresses.size_is.dwAddressCount

### -field Addresses

Array of 
<a href="/windows/desktop/api/nspapi/ns-nspapi-service_address">SERVICE_ADDRESS</a> data structures. Each 
<b>SERVICE_ADDRESS</b> structure contains information about a network service address.

## -see-also

<a href="/windows/desktop/api/nspapi/ns-nspapi-service_address">SERVICE_ADDRESS</a>



<a href="/windows/desktop/api/nspapi/ns-nspapi-service_infoa">SERVICE_INFO</a>