---
UID: NS:ifdef._NET_PHYSICAL_LOCATION_LH
title: NET_PHYSICAL_LOCATION_LH (ifdef.h)
description: The NET_PHYSICAL_LOCATION structure provides NDIS with information about the physical location of a registered network interface.
helpviewer_keywords: ["*PNET_PHYSICAL_LOCATION","*PNET_PHYSICAL_LOCATION_LH","NET_PHYSICAL_LOCATION","NET_PHYSICAL_LOCATION structure [Network Drivers Starting with Windows Vista]","NET_PHYSICAL_LOCATION_LH","ifdef/NET_PHYSICAL_LOCATION","net_if_struct_ref_838a8166-a43e-4b5a-ab96-15286d981684.xml","netvista.net_physical_location"]
old-location: netvista\net_physical_location.htm
tech.root: NetVista
ms.assetid: e5661e05-a83f-4632-af98-2a021eeb7d80
ms.date: 12/05/2018
ms.keywords: '*PNET_PHYSICAL_LOCATION, *PNET_PHYSICAL_LOCATION_LH, NET_PHYSICAL_LOCATION, NET_PHYSICAL_LOCATION structure [Network Drivers Starting with Windows Vista], NET_PHYSICAL_LOCATION_LH, ifdef/NET_PHYSICAL_LOCATION, net_if_struct_ref_838a8166-a43e-4b5a-ab96-15286d981684.xml, netvista.net_physical_location'
req.header: ifdef.h
req.include-header: Ntddndis.h
req.target-type: Windows
req.target-min-winverclnt: Supported in NDIS 6.0 and later.
req.target-min-winversvr: 
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
req.typenames: NET_PHYSICAL_LOCATION_LH, *PNET_PHYSICAL_LOCATION_LH
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _NET_PHYSICAL_LOCATION_LH
 - ifdef/_NET_PHYSICAL_LOCATION_LH
 - PNET_PHYSICAL_LOCATION_LH
 - ifdef/PNET_PHYSICAL_LOCATION_LH
 - NET_PHYSICAL_LOCATION_LH
 - ifdef/NET_PHYSICAL_LOCATION_LH
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ifdef.h
api_name:
 - NET_PHYSICAL_LOCATION
---

# NET_PHYSICAL_LOCATION_LH structure


## -description

The NET_PHYSICAL_LOCATION structure provides NDIS with information about the physical location of a
  registered network interface.

## -struct-fields

### -field BusNumber

The bus number of the physical location for hardware. If the physical location is unknown, set
     this member to NIIF_BUS_NUMBER_UNKNOWN. Other values are reserved for NDIS.

### -field SlotNumber

The slot number of the physical location for hardware. If the physical location is unknown, set
     this member to NIIF_SLOT_NUMBER_UNKNOWN. Other values are reserved for NDIS.

### -field FunctionNumber

The function number of the physical location for hardware. If the physical location is unknown,
     set this member to NIIF_FUNCTION_NUMBER_UNKNOWN. Other values are reserved for NDIS.

## -remarks

A network interface provider initializes a 
    <a href="/windows-hardware/drivers/ddi/content/ndis/ns-ndis-_net_if_information">NET_IF_INFORMATION</a> structure to provide
    NDIS with information about each registered interface. The NET_PHYSICAL_LOCATION structure is included in
    the 
    <b>PhysicalLocation</b> member of the NET_IF_INFORMATION structure.

NET_PHYSICAL_LOCATION contains information that remains constant during the lifetime of the interface.
    To register an interface, a provider passes a pointer to a provider-initialized NET_IF_INFORMATION
    structure to the 
    <a href="/windows-hardware/drivers/ddi/content/ndis/nf-ndis-ndisifregisterinterface">NdisIfRegisterInterface</a> function.

## -see-also

<a href="/windows-hardware/drivers/ddi/content/ndis/ns-ndis-_net_if_information">NET_IF_INFORMATION</a>



<a href="/windows-hardware/drivers/ddi/content/ndis/nf-ndis-ndisifregisterinterface">NdisIfRegisterInterface</a>