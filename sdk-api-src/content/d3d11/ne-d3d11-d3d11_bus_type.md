---
UID: NE:d3d11.D3D11_BUS_TYPE
title: D3D11_BUS_TYPE
author: windows-sdk-content
description: Specifies the type of I/O bus that is used by the graphics adapter.
old-location: mf\d3d11_bus_type.htm
old-project: medfound
ms.assetid: 3B93166B-7829-4A3D-9D13-631F0242E13F
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: D3D11_BUS_IMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR, D3D11_BUS_IMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR_INSIDE_OF_NUAE, D3D11_BUS_IMPL_MODIFIER_INSIDE_OF_CHIPSET, D3D11_BUS_IMPL_MODIFIER_NON_STANDARD, D3D11_BUS_IMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_CHIP, D3D11_BUS_IMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_SOCKET, D3D11_BUS_TYPE, D3D11_BUS_TYPE enumeration [Media Foundation], D3D11_BUS_TYPE_AGP, D3D11_BUS_TYPE_OTHER, D3D11_BUS_TYPE_PCI, D3D11_BUS_TYPE_PCIEXPRESS, D3D11_BUS_TYPE_PCIX, d3d11/D3D11_BUS_IMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR, d3d11/D3D11_BUS_IMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR_INSIDE_OF_NUAE, d3d11/D3D11_BUS_IMPL_MODIFIER_INSIDE_OF_CHIPSET, d3d11/D3D11_BUS_IMPL_MODIFIER_NON_STANDARD, d3d11/D3D11_BUS_IMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_CHIP, d3d11/D3D11_BUS_IMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_SOCKET, d3d11/D3D11_BUS_TYPE, d3d11/D3D11_BUS_TYPE_AGP, d3d11/D3D11_BUS_TYPE_OTHER, d3d11/D3D11_BUS_TYPE_PCI, d3d11/D3D11_BUS_TYPE_PCIEXPRESS, d3d11/D3D11_BUS_TYPE_PCIX, mf.d3d11_bus_type
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d3d11.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: D3D11_BUS_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d11.h
api_name:
 - D3D11_BUS_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D11_BUS_TYPE enumeration


## -description


Specifies the type of I/O bus that is used by the graphics adapter.


## -enum-fields




### -field D3D11_BUS_TYPE_OTHER

Indicates a type of bus other than the types listed here.



### -field D3D11_BUS_TYPE_PCI

PCI bus.



### -field D3D11_BUS_TYPE_PCIX

PCI-X bus.



### -field D3D11_BUS_TYPE_PCIEXPRESS

PCI Express bus.



### -field D3D11_BUS_TYPE_AGP

Accelerated Graphics Port (AGP) bus.



### -field D3D11_BUS_IMPL_MODIFIER_INSIDE_OF_CHIPSET

The implementation for the graphics adapter is in a motherboard chipset's north bridge. This flag implies that data never goes over an expansion bus (such as PCI or AGP) when it is transferred from main memory to the graphics adapter.


### -field D3D11_BUS_IMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_CHIP

Indicates that the graphics adapter is connected to a motherboard chipset's north bridge by tracks on the motherboard, and all of the graphics adapter's chips are soldered to the motherboard. This flag implies that data never goes over an expansion bus (such as PCI or AGP) when it is transferred from main memory to the graphics adapter.


### -field D3D11_BUS_IMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_SOCKET

The graphics adapter is connected to a motherboard chipset's north bridge by tracks on the motherboard, and all of the graphics adapter's chips are connected through sockets to the motherboard.



### -field D3D11_BUS_IMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR

The graphics adapter is connected to the motherboard through a daughterboard connector.



### -field D3D11_BUS_IMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR_INSIDE_OF_NUAE

The graphics adapter is connected to the motherboard through a daughterboard connector, and the graphics adapter is inside an enclosure that is not user accessible.



### -field D3D11_BUS_IMPL_MODIFIER_NON_STANDARD

One of the <b>D3D11_BUS_IMPL_MODIFIER_Xxx</b> flags is set.



## -see-also




<a href="https://msdn.microsoft.com/40061AD1-BCD9-4170-A442-34B4C792BB55">Direct3D 11 Video Enumerations</a>
 

 

