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

# DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY enumeration


## -description


The DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY enumeration specifies the target's connector type.


## -enum-fields




### -field DISPLAYCONFIG_OUTPUT_TECHNOLOGY_OTHER

Indicates a connector that is not one of the types that is indicated by the following enumerators in this enumeration.


### -field DISPLAYCONFIG_OUTPUT_TECHNOLOGY_HD15

Indicates an HD15 (VGA) connector.


### -field DISPLAYCONFIG_OUTPUT_TECHNOLOGY_SVIDEO

Indicates an S-video connector.


### -field DISPLAYCONFIG_OUTPUT_TECHNOLOGY_COMPOSITE_VIDEO

Indicates a composite video connector group.


### -field DISPLAYCONFIG_OUTPUT_TECHNOLOGY_COMPONENT_VIDEO

Indicates a component video connector group.


### -field DISPLAYCONFIG_OUTPUT_TECHNOLOGY_DVI

Indicates a Digital Video Interface (DVI) connector.


### -field DISPLAYCONFIG_OUTPUT_TECHNOLOGY_HDMI

Indicates a High-Definition Multimedia Interface (HDMI) connector.


### -field DISPLAYCONFIG_OUTPUT_TECHNOLOGY_LVDS

Indicates a Low Voltage Differential Swing (LVDS) connector.


### -field DISPLAYCONFIG_OUTPUT_TECHNOLOGY_D_JPN

Indicates a Japanese D connector. 


### -field DISPLAYCONFIG_OUTPUT_TECHNOLOGY_SDI

Indicates an SDI connector.


### -field DISPLAYCONFIG_OUTPUT_TECHNOLOGY_DISPLAYPORT_EXTERNAL

Indicates an external display port, which is a display port that connects externally to a display device.


### -field DISPLAYCONFIG_OUTPUT_TECHNOLOGY_DISPLAYPORT_EMBEDDED

Indicates an embedded display port that connects internally to a display device.


### -field DISPLAYCONFIG_OUTPUT_TECHNOLOGY_UDI_EXTERNAL

Indicates an external Unified Display Interface (UDI), which is a UDI that connects externally to a display device.


### -field DISPLAYCONFIG_OUTPUT_TECHNOLOGY_UDI_EMBEDDED

Indicates an embedded UDI that connects internally to a display device.


### -field DISPLAYCONFIG_OUTPUT_TECHNOLOGY_SDTVDONGLE

Indicates a dongle cable that supports standard definition television (SDTV).


### -field DISPLAYCONFIG_OUTPUT_TECHNOLOGY_MIRACAST

Indicates that the VidPN target is  a Miracast wireless display device.

Supported starting in Windows 8.1.


### -field DISPLAYCONFIG_OUTPUT_TECHNOLOGY_INDIRECT_WIRED


### -field DISPLAYCONFIG_OUTPUT_TECHNOLOGY_INTERNAL

Indicates that the video output device connects internally to a display device (for example, the internal connection in a laptop computer).


### -field DISPLAYCONFIG_OUTPUT_TECHNOLOGY_FORCE_UINT32

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. You should not use this value.


## -remarks



Values with "embedded" in their names indicate that the graphics adapter's video output device connects internally to the display device. In those cases, the DISPLAYCONFIG_OUTPUT_TECHNOLOGY_INTERNAL value is redundant. The caller should ignore DISPLAYCONFIG_OUTPUT_TECHNOLOGY_INTERNAL and just process the embedded values, DISPLAYCONFIG_OUTPUT_TECHNOLOGY_DISPLAYPORT_EMBEDDED and DISPLAYCONFIG_OUTPUT_TECHNOLOGY_UDI_EMBEDDED.

An embedded display port or UDI is also known as an integrated display port or UDI.



