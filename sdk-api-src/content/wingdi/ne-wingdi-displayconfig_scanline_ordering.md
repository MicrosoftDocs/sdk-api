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

