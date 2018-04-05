---
UID: NE:d3d9types._D3DBUSTYPE
title: "_D3DBUSTYPE"
author: windows-driver-content
description: Specifies the type of I/O bus used by the graphics adapter.
old-location: mf\d3dbustype.htm
old-project: medfound
ms.assetid: 11bb7e0e-8d49-45f2-89aa-7583dd925edf
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR, D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR_INSIDE_OF_NUAE, D3DBUSIMPL_MODIFIER_INSIDE_OF_CHIPSET, D3DBUSIMPL_MODIFIER_NON_STANDARD, D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_CHIP, D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_SOCKET, D3DBUSTYPE, D3DBUSTYPE enumeration [Media Foundation], D3DBUSTYPE_AGP, D3DBUSTYPE_OTHER, D3DBUSTYPE_PCI, D3DBUSTYPE_PCIEXPRESS, D3DBUSTYPE_PCIX, _D3DBUSTYPE, d3d9types/D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR, d3d9types/D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR_INSIDE_OF_NUAE, d3d9types/D3DBUSIMPL_MODIFIER_INSIDE_OF_CHIPSET, d3d9types/D3DBUSIMPL_MODIFIER_NON_STANDARD, d3d9types/D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_CHIP, d3d9types/D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_SOCKET, d3d9types/D3DBUSTYPE, d3d9types/D3DBUSTYPE_AGP, d3d9types/D3DBUSTYPE_OTHER, d3d9types/D3DBUSTYPE_PCI, d3d9types/D3DBUSTYPE_PCIEXPRESS, d3d9types/D3DBUSTYPE_PCIX, mf.d3dbustype
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: d3d9types.h
req.include-header: D3d9.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: D3DBUSTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	d3d9types.h
api_name:
-	D3DBUSTYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DBUSTYPE enumeration


## -description


Specifies the type of I/O bus used by the graphics adapter.


## -enum-fields




### -field D3DBUSTYPE_OTHER

Indicates a type of bus other than the types listed here.



### -field D3DBUSTYPE_PCI

PCI bus.



### -field D3DBUSTYPE_PCIX

PCI-X bus.



### -field D3DBUSTYPE_PCIEXPRESS

PCI Express bus.



### -field D3DBUSTYPE_AGP

Accelerated Graphics Port (AGP) bus.



### -field D3DBUSIMPL_MODIFIER_INSIDE_OF_CHIPSET

The implementation for the graphics adapter is in a motherboard chipset's north bridge. This flag implies that data never goes over an expansion bus (such as PCI or AGP) when it is transferred from main memory to the graphics adapter.


### -field D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_CHIP

Indicates that the graphics adapter is connected to a motherboard chipset's north bridge by tracks on the motherboard and all of the graphics adapter's chips are soldered to the motherboard. This flag implies that data never goes over an expansion bus (such as PCI or AGP) when it is transferred from main memory to the graphics adapter.


### -field D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_SOCKET

The graphics adapter is connected to a motherboard chipset's north bridge by tracks on the motherboard, and all of the graphics adapter's chips are connected through sockets to the motherboard.



### -field D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR

The graphics adapter is connected to the motherboard through a daughterboard connector.



### -field D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR_INSIDE_OF_NUAE

The graphics adapter is connected to the motherboard through a daughterboard connector, and the graphics adapter is inside an enclosure that is not user accessible.



### -field D3DBUSIMPL_MODIFIER_NON_STANDARD

One of the D3DBUSIMPL_MODIFIER_MODIFIER_Xxx flags is set.



## -remarks



As many as three flags can be set. Flags in the range 0x00 through 0x04 (<b>D3DBUSTYPE_Xxx</b>) provide the basic bus type. Flags in the range 0x10000 through 0x50000 (<b>D3DBUSIMPL_MODIFIER_Xxx</b>) modify the basic description. The driver sets one bus-type flag, and can set zero or one modifier flag. If the driver sets a modifier flag, it also sets the <b>D3DBUSIMPL_MODIFIER_NON_STANDARD</b> flag. Flags are combined with a bitwise <b>OR</b>.






## -see-also




<a href="https://msdn.microsoft.com/41959498-501d-4f0d-ba1f-1c0690b62f4d">Direct3D Video Enumerations</a>
 

 

