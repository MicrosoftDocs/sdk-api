---
UID: NE:d3d11.D3D11_BUS_TYPE
title: D3D11_BUS_TYPE (d3d11.h)
description: Specifies the type of I/O bus that is used by the graphics adapter.
helpviewer_keywords: ["D3D11_BUS_IMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR","D3D11_BUS_IMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR_INSIDE_OF_NUAE","D3D11_BUS_IMPL_MODIFIER_INSIDE_OF_CHIPSET","D3D11_BUS_IMPL_MODIFIER_NON_STANDARD","D3D11_BUS_IMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_CHIP","D3D11_BUS_IMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_SOCKET","D3D11_BUS_TYPE","D3D11_BUS_TYPE enumeration [Media Foundation]","D3D11_BUS_TYPE_AGP","D3D11_BUS_TYPE_OTHER","D3D11_BUS_TYPE_PCI","D3D11_BUS_TYPE_PCIEXPRESS","D3D11_BUS_TYPE_PCIX","d3d11/D3D11_BUS_IMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR","d3d11/D3D11_BUS_IMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR_INSIDE_OF_NUAE","d3d11/D3D11_BUS_IMPL_MODIFIER_INSIDE_OF_CHIPSET","d3d11/D3D11_BUS_IMPL_MODIFIER_NON_STANDARD","d3d11/D3D11_BUS_IMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_CHIP","d3d11/D3D11_BUS_IMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_SOCKET","d3d11/D3D11_BUS_TYPE","d3d11/D3D11_BUS_TYPE_AGP","d3d11/D3D11_BUS_TYPE_OTHER","d3d11/D3D11_BUS_TYPE_PCI","d3d11/D3D11_BUS_TYPE_PCIEXPRESS","d3d11/D3D11_BUS_TYPE_PCIX","mf.d3d11_bus_type"]
old-location: mf\d3d11_bus_type.htm
tech.root: mf
ms.assetid: 3B93166B-7829-4A3D-9D13-631F0242E13F
ms.date: 12/05/2018
ms.keywords: D3D11_BUS_IMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR, D3D11_BUS_IMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR_INSIDE_OF_NUAE, D3D11_BUS_IMPL_MODIFIER_INSIDE_OF_CHIPSET, D3D11_BUS_IMPL_MODIFIER_NON_STANDARD, D3D11_BUS_IMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_CHIP, D3D11_BUS_IMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_SOCKET, D3D11_BUS_TYPE, D3D11_BUS_TYPE enumeration [Media Foundation], D3D11_BUS_TYPE_AGP, D3D11_BUS_TYPE_OTHER, D3D11_BUS_TYPE_PCI, D3D11_BUS_TYPE_PCIEXPRESS, D3D11_BUS_TYPE_PCIX, d3d11/D3D11_BUS_IMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR, d3d11/D3D11_BUS_IMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR_INSIDE_OF_NUAE, d3d11/D3D11_BUS_IMPL_MODIFIER_INSIDE_OF_CHIPSET, d3d11/D3D11_BUS_IMPL_MODIFIER_NON_STANDARD, d3d11/D3D11_BUS_IMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_CHIP, d3d11/D3D11_BUS_IMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_SOCKET, d3d11/D3D11_BUS_TYPE, d3d11/D3D11_BUS_TYPE_AGP, d3d11/D3D11_BUS_TYPE_OTHER, d3d11/D3D11_BUS_TYPE_PCI, d3d11/D3D11_BUS_TYPE_PCIEXPRESS, d3d11/D3D11_BUS_TYPE_PCIX, mf.d3d11_bus_type
req.header: d3d11.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D3D11_BUS_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_BUS_TYPE
 - d3d11/D3D11_BUS_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d11.h
api_name:
 - D3D11_BUS_TYPE
---

# D3D11_BUS_TYPE enumeration


## -description

Specifies the type of I/O bus that is used by the graphics adapter.

## -enum-fields

### -field D3D11_BUS_TYPE_OTHER:0

Indicates a type of bus other than the types listed here.

### -field D3D11_BUS_TYPE_PCI:0x1

PCI bus.

### -field D3D11_BUS_TYPE_PCIX:0x2

PCI-X bus.

### -field D3D11_BUS_TYPE_PCIEXPRESS:0x3

PCI Express bus.

### -field D3D11_BUS_TYPE_AGP:0x4

Accelerated Graphics Port (AGP) bus.

### -field D3D11_BUS_IMPL_MODIFIER_INSIDE_OF_CHIPSET:0x10000

The implementation for the graphics adapter is in a motherboard chipset's north bridge. This flag implies that data never goes over an expansion bus (such as PCI or AGP) when it is transferred from main memory to the graphics adapter.

### -field D3D11_BUS_IMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_CHIP:0x20000

Indicates that the graphics adapter is connected to a motherboard chipset's north bridge by tracks on the motherboard, and all of the graphics adapter's chips are soldered to the motherboard. This flag implies that data never goes over an expansion bus (such as PCI or AGP) when it is transferred from main memory to the graphics adapter.

### -field D3D11_BUS_IMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_SOCKET:0x30000

The graphics adapter is connected to a motherboard chipset's north bridge by tracks on the motherboard, and all of the graphics adapter's chips are connected through sockets to the motherboard.

### -field D3D11_BUS_IMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR:0x40000

The graphics adapter is connected to the motherboard through a daughterboard connector.

### -field D3D11_BUS_IMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR_INSIDE_OF_NUAE:0x50000

The graphics adapter is connected to the motherboard through a daughterboard connector, and the graphics adapter is inside an enclosure that is not user accessible.

### -field D3D11_BUS_IMPL_MODIFIER_NON_STANDARD:0x80000000

One of the <b>D3D11_BUS_IMPL_MODIFIER_Xxx</b> flags is set.

## -see-also

<a href="/windows/desktop/medfound/direct3d-11-video-enumerations">Direct3D 11 Video Enumerations</a>
