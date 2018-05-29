---
UID: NE:msinkaut.TabletHardwareCapabilities
title: TabletHardwareCapabilities
author: windows-sdk-content
description: Specifies the hardware capabilities of the Tablet PC.
old-location: tablet\tablethardwarecapabilities.htm
old-project: tablet
ms.assetid: ab8dfca3-df5e-40a7-9da2-d19447bc746b
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: THWC_CursorMustTouch, THWC_CursorsHavePhysicalIds, THWC_HardProximity, THWC_Integrated, TabletHardwareCapabilities, TabletHardwareCapabilities enumeration [Tablet PC], ab8dfca3-df5e-40a7-9da2-d19447bc746b, msinkaut/THWC_CursorMustTouch, msinkaut/THWC_CursorsHavePhysicalIds, msinkaut/THWC_HardProximity, msinkaut/THWC_Integrated, msinkaut/TabletHardwareCapabilities, tablet.tablethardwarecapabilities
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: msinkaut.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TabletHardwareCapabilities
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	msinkaut.h
api_name:
-	TabletHardwareCapabilities
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# TabletHardwareCapabilities enumeration


## -description



Specifies the hardware capabilities of the Tablet PC.




## -enum-fields




### -field THWC_Integrated

The digitizer is integrated with the display.


### -field THWC_CursorMustTouch

The cursor must be in physical contact with the device to report position.


### -field THWC_HardProximity

The device can generate in-air packets when the cursor is in the physical detection range (proximity) of the device.


### -field THWC_CursorsHavePhysicalIds

The device can uniquely identify the active cursor.


## -remarks



In C++, explicit casting is required when trying to set more than one flag at a time. A compilation error occurs if explicit casting is not used.

The value is 0 if the tablet device cannot provide this information.

This enumeration is a flag.




## -see-also




<a href="https://msdn.microsoft.com/886c1e7c-fec0-4294-aba1-8e0806c2d0ca">HardwareCapabilities Property</a>



<a href="https://msdn.microsoft.com/9a945740-b191-41f5-8b3d-49b7e2d1e463">IInkTablet Interface</a>
 

 

