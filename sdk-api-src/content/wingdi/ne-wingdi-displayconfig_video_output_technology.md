---
UID: NE:wingdi.DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY
title: DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY
author: windows-sdk-content
description: The DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY enumeration specifies the target's connector type.
old-location: display\displayconfig_video_output_technology.htm
old-project: display
ms.assetid: f8c2095a-d67e-42ed-b615-b5e0e0e0d507
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: CCD_Enumerations_311f4c31-4f6c-42d2-945f-5d9983488a4e.xml, DISPLAYCONFIG_OUTPUT_TECHNOLOGY_COMPONENT_VIDEO, DISPLAYCONFIG_OUTPUT_TECHNOLOGY_COMPOSITE_VIDEO, DISPLAYCONFIG_OUTPUT_TECHNOLOGY_DISPLAYPORT_EMBEDDED, DISPLAYCONFIG_OUTPUT_TECHNOLOGY_DISPLAYPORT_EXTERNAL, DISPLAYCONFIG_OUTPUT_TECHNOLOGY_DVI, DISPLAYCONFIG_OUTPUT_TECHNOLOGY_D_JPN, DISPLAYCONFIG_OUTPUT_TECHNOLOGY_FORCE_UINT32, DISPLAYCONFIG_OUTPUT_TECHNOLOGY_HD15, DISPLAYCONFIG_OUTPUT_TECHNOLOGY_HDMI, DISPLAYCONFIG_OUTPUT_TECHNOLOGY_INTERNAL, DISPLAYCONFIG_OUTPUT_TECHNOLOGY_LVDS, DISPLAYCONFIG_OUTPUT_TECHNOLOGY_MIRACAST, DISPLAYCONFIG_OUTPUT_TECHNOLOGY_OTHER, DISPLAYCONFIG_OUTPUT_TECHNOLOGY_SDI, DISPLAYCONFIG_OUTPUT_TECHNOLOGY_SDTVDONGLE, DISPLAYCONFIG_OUTPUT_TECHNOLOGY_SVIDEO, DISPLAYCONFIG_OUTPUT_TECHNOLOGY_UDI_EMBEDDED, DISPLAYCONFIG_OUTPUT_TECHNOLOGY_UDI_EXTERNAL, DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY, DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY enumeration [Display Devices], display.displayconfig_video_output_technology, wingdi/DISPLAYCONFIG_OUTPUT_TECHNOLOGY_COMPONENT_VIDEO, wingdi/DISPLAYCONFIG_OUTPUT_TECHNOLOGY_COMPOSITE_VIDEO, wingdi/DISPLAYCONFIG_OUTPUT_TECHNOLOGY_DISPLAYPORT_EMBEDDED, wingdi/DISPLAYCONFIG_OUTPUT_TECHNOLOGY_DISPLAYPORT_EXTERNAL, wingdi/DISPLAYCONFIG_OUTPUT_TECHNOLOGY_DVI, wingdi/DISPLAYCONFIG_OUTPUT_TECHNOLOGY_D_JPN, wingdi/DISPLAYCONFIG_OUTPUT_TECHNOLOGY_FORCE_UINT32, wingdi/DISPLAYCONFIG_OUTPUT_TECHNOLOGY_HD15, wingdi/DISPLAYCONFIG_OUTPUT_TECHNOLOGY_HDMI, wingdi/DISPLAYCONFIG_OUTPUT_TECHNOLOGY_INTERNAL, wingdi/DISPLAYCONFIG_OUTPUT_TECHNOLOGY_LVDS, wingdi/DISPLAYCONFIG_OUTPUT_TECHNOLOGY_MIRACAST, wingdi/DISPLAYCONFIG_OUTPUT_TECHNOLOGY_OTHER, wingdi/DISPLAYCONFIG_OUTPUT_TECHNOLOGY_SDI, wingdi/DISPLAYCONFIG_OUTPUT_TECHNOLOGY_SDTVDONGLE, wingdi/DISPLAYCONFIG_OUTPUT_TECHNOLOGY_SVIDEO, wingdi/DISPLAYCONFIG_OUTPUT_TECHNOLOGY_UDI_EMBEDDED, wingdi/DISPLAYCONFIG_OUTPUT_TECHNOLOGY_UDI_EXTERNAL, wingdi/DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wingdi.h
api_name:
 - DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
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


### -field DISPLAYCONFIG_OUTPUT_TECHNOLOGY_INDIRECT_VIRTUAL


### -field DISPLAYCONFIG_OUTPUT_TECHNOLOGY_INTERNAL

Indicates that the video output device connects internally to a display device (for example, the internal connection in a laptop computer).


### -field DISPLAYCONFIG_OUTPUT_TECHNOLOGY_FORCE_UINT32

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. You should not use this value.


## -remarks



Values with "embedded" in their names indicate that the graphics adapter's video output device connects internally to the display device. In those cases, the DISPLAYCONFIG_OUTPUT_TECHNOLOGY_INTERNAL value is redundant. The caller should ignore DISPLAYCONFIG_OUTPUT_TECHNOLOGY_INTERNAL and just process the embedded values, DISPLAYCONFIG_OUTPUT_TECHNOLOGY_DISPLAYPORT_EMBEDDED and DISPLAYCONFIG_OUTPUT_TECHNOLOGY_UDI_EMBEDDED.

An embedded display port or UDI is also known as an integrated display port or UDI.



