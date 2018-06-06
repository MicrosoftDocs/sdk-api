---
UID: NE:wingdi.DISPLAYCONFIG_SCANLINE_ORDERING
title: DISPLAYCONFIG_SCANLINE_ORDERING
author: windows-sdk-content
description: The DISPLAYCONFIG_SCANLINE_ORDERING enumeration specifies the method that the display uses to create an image on a screen.
old-location: display\displayconfig_scanline_ordering.htm
old-project: display
ms.assetid: 5b8d6c83-e8fb-4529-8d61-557ed0e4da37
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: CCD_Enumerations_e6c7a4af-750c-4a3c-a89d-562448487abc.xml, DISPLAYCONFIG_SCANLINE_ORDERING, DISPLAYCONFIG_SCANLINE_ORDERING enumeration [Display Devices], DISPLAYCONFIG_SCANLINE_ORDERING_FORCE_UINT32, DISPLAYCONFIG_SCANLINE_ORDERING_INTERLACED, DISPLAYCONFIG_SCANLINE_ORDERING_INTERLACED_LOWERFIELDFIRST, DISPLAYCONFIG_SCANLINE_ORDERING_INTERLACED_UPPERFIELDFIRST, DISPLAYCONFIG_SCANLINE_ORDERING_PROGRESSIVE, DISPLAYCONFIG_SCANLINE_ORDERING_UNSPECIFIED, display.displayconfig_scanline_ordering, wingdi/DISPLAYCONFIG_SCANLINE_ORDERING, wingdi/DISPLAYCONFIG_SCANLINE_ORDERING_FORCE_UINT32, wingdi/DISPLAYCONFIG_SCANLINE_ORDERING_INTERLACED, wingdi/DISPLAYCONFIG_SCANLINE_ORDERING_INTERLACED_LOWERFIELDFIRST, wingdi/DISPLAYCONFIG_SCANLINE_ORDERING_INTERLACED_UPPERFIELDFIRST, wingdi/DISPLAYCONFIG_SCANLINE_ORDERING_PROGRESSIVE, wingdi/DISPLAYCONFIG_SCANLINE_ORDERING_UNSPECIFIED
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
req.typenames: DISPLAYCONFIG_SCANLINE_ORDERING
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wingdi.h
api_name:
 - DISPLAYCONFIG_SCANLINE_ORDERING
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# DISPLAYCONFIG_SCANLINE_ORDERING enumeration


## -description


The DISPLAYCONFIG_SCANLINE_ORDERING enumeration specifies the method that the display uses to create an image on a screen.


## -enum-fields




### -field DISPLAYCONFIG_SCANLINE_ORDERING_UNSPECIFIED

Indicates that scan-line ordering of the output is unspecified. The caller can only set the <b>scanLineOrdering</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff553954">DISPLAYCONFIG_PATH_TARGET_INFO</a> structure in a call to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff569533">SetDisplayConfig</a> function to DISPLAYCONFIG_SCANLINE_ORDERING_UNSPECIFIED if the caller also set the refresh rate denominator and numerator of the <b>refreshRate</b> member both to zero. In this case, <b>SetDisplayConfig</b> uses the best refresh rate it can find. 


### -field DISPLAYCONFIG_SCANLINE_ORDERING_PROGRESSIVE

Indicates that the output is a progressive image.


### -field DISPLAYCONFIG_SCANLINE_ORDERING_INTERLACED

Indicates that the output is an interlaced image that is created beginning with the upper field.


### -field DISPLAYCONFIG_SCANLINE_ORDERING_INTERLACED_UPPERFIELDFIRST

Indicates that the output is an interlaced image that is created beginning with the upper field.


### -field DISPLAYCONFIG_SCANLINE_ORDERING_INTERLACED_LOWERFIELDFIRST

Indicates that the output is an interlaced image that is created beginning with the lower field.


### -field DISPLAYCONFIG_SCANLINE_ORDERING_FORCE_UINT32

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. You should not use this value. 

