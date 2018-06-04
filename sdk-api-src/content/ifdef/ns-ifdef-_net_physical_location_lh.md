---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
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
---

# _NET_PHYSICAL_LOCATION_LH structure


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
    <a href="https://msdn.microsoft.com/library/windows/hardware/ff568743">NET_IF_INFORMATION</a> structure to provide
    NDIS with information about each registered interface. The NET_PHYSICAL_LOCATION structure is included in
    the 
    <b>PhysicalLocation</b> member of the NET_IF_INFORMATION structure.

NET_PHYSICAL_LOCATION contains information that remains constant during the lifetime of the interface.
    To register an interface, a provider passes a pointer to a provider-initialized NET_IF_INFORMATION
    structure to the 
    <a href="https://msdn.microsoft.com/d0b0ada7-afb1-4cb7-ada6-7c5c7abe7d19">
    NdisIfRegisterInterface</a> function.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff568743">NET_IF_INFORMATION</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff562715">NdisIfRegisterInterface</a>
 

 

