---
UID: NE:wingdi.DISPLAYCONFIG_TOPOLOGY_ID
title: DISPLAYCONFIG_TOPOLOGY_ID (wingdi.h)
description: The DISPLAYCONFIG_TOPOLOGY_ID enumeration specifies the type of display topology.
helpviewer_keywords: ["CCD_Enumerations_a5eed051-186c-4a2e-8a8b-fd189d867fbd.xml","DISPLAYCONFIG_TOPOLOGY_CLONE","DISPLAYCONFIG_TOPOLOGY_EXTEND","DISPLAYCONFIG_TOPOLOGY_EXTERNAL","DISPLAYCONFIG_TOPOLOGY_FORCE_UINT32","DISPLAYCONFIG_TOPOLOGY_ID","DISPLAYCONFIG_TOPOLOGY_ID enumeration [Display Devices]","DISPLAYCONFIG_TOPOLOGY_INTERNAL","display.displayconfig_topology_id","wingdi/DISPLAYCONFIG_TOPOLOGY_CLONE","wingdi/DISPLAYCONFIG_TOPOLOGY_EXTEND","wingdi/DISPLAYCONFIG_TOPOLOGY_EXTERNAL","wingdi/DISPLAYCONFIG_TOPOLOGY_FORCE_UINT32","wingdi/DISPLAYCONFIG_TOPOLOGY_ID","wingdi/DISPLAYCONFIG_TOPOLOGY_INTERNAL"]
old-location: display\displayconfig_topology_id.htm
tech.root: display
ms.assetid: 0018f137-7cdf-47b7-9ede-8685f9b073fb
ms.date: 12/05/2018
ms.keywords: CCD_Enumerations_a5eed051-186c-4a2e-8a8b-fd189d867fbd.xml, DISPLAYCONFIG_TOPOLOGY_CLONE, DISPLAYCONFIG_TOPOLOGY_EXTEND, DISPLAYCONFIG_TOPOLOGY_EXTERNAL, DISPLAYCONFIG_TOPOLOGY_FORCE_UINT32, DISPLAYCONFIG_TOPOLOGY_ID, DISPLAYCONFIG_TOPOLOGY_ID enumeration [Display Devices], DISPLAYCONFIG_TOPOLOGY_INTERNAL, display.displayconfig_topology_id, wingdi/DISPLAYCONFIG_TOPOLOGY_CLONE, wingdi/DISPLAYCONFIG_TOPOLOGY_EXTEND, wingdi/DISPLAYCONFIG_TOPOLOGY_EXTERNAL, wingdi/DISPLAYCONFIG_TOPOLOGY_FORCE_UINT32, wingdi/DISPLAYCONFIG_TOPOLOGY_ID, wingdi/DISPLAYCONFIG_TOPOLOGY_INTERNAL
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Available in Windows 7 Client.
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
req.typenames: DISPLAYCONFIG_TOPOLOGY_ID
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DISPLAYCONFIG_TOPOLOGY_ID
 - wingdi/DISPLAYCONFIG_TOPOLOGY_ID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wingdi.h
api_name:
 - DISPLAYCONFIG_TOPOLOGY_ID
---

# DISPLAYCONFIG_TOPOLOGY_ID enumeration


## -description

The DISPLAYCONFIG_TOPOLOGY_ID enumeration specifies the type of display topology.

## -enum-fields

### -field DISPLAYCONFIG_TOPOLOGY_INTERNAL:0x00000001

Indicates that the display topology is an internal configuration.

### -field DISPLAYCONFIG_TOPOLOGY_CLONE:0x00000002

Indicates that the display topology is clone-view configuration.

### -field DISPLAYCONFIG_TOPOLOGY_EXTEND:0x00000004

Indicates that the display topology is an extended configuration.

### -field DISPLAYCONFIG_TOPOLOGY_EXTERNAL:0x00000008

Indicates that the display topology is an external configuration.

### -field DISPLAYCONFIG_TOPOLOGY_FORCE_UINT32:0xFFFFFFFF

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. You should not use this value.

