---
UID: NF:wingdi.OffsetViewportOrgEx
title: OffsetViewportOrgEx function
author: windows-sdk-content
description: The OffsetViewportOrgEx function modifies the viewport origin for a device context using the specified horizontal and vertical offsets.
old-location: gdi\offsetviewportorgex.htm
old-project: gdi
ms.assetid: 54311cbe-1c54-4193-8991-891dbd0856bf
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: OffsetViewportOrgEx, OffsetViewportOrgEx function [Windows GDI], _win32_OffsetViewportOrgEx, gdi.offsetviewportorgex, wingdi/OffsetViewportOrgEx
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	gdi32.dll
-	Ext-MS-Win-GDI-Draw-l1-1-1.dll
-	ext-ms-win-gdi-draw-l1-1-2.dll
-	Ext-MS-Win-GDI-Draw-L1-1-3.dll
-	GDI32Full.dll
api_name:
-	OffsetViewportOrgEx
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# OffsetViewportOrgEx function


## -description


The <b>OffsetViewportOrgEx</b> function modifies the viewport origin for a device context using the specified horizontal and vertical offsets.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param x

TBD


### -param y

TBD


### -param lppt

TBD




#### - lpPoint [out]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a> structure. The previous viewport origin, in device units, is placed in this structure. If <i>lpPoint</i> is <b>NULL</b>, the previous viewport origin is not returned.


#### - nXOffset [in]

The horizontal offset, in device units.


#### - nYOffset [in]

The vertical offset, in device units.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The new origin is the sum of the current origin and the horizontal and vertical offsets.




## -see-also




<a href="https://msdn.microsoft.com/3ebcabf2-9718-47b2-aba0-7cc28fa42e5a">Coordinate Space and Transformation Functions</a>



<a href="https://msdn.microsoft.com/cfb02788-9b73-4451-9e68-2ad310e0e527">Coordinate Spaces and Transformations Overview</a>



<a href="https://msdn.microsoft.com/6e6c7090-edf4-46a3-8bcd-10a00c0cf847">GetViewportOrgEx</a>



<a href="https://msdn.microsoft.com/085f40ac-d91f-4853-8ad1-1fc5da08b981">OffsetWindowOrgEx</a>



<a href="https://msdn.microsoft.com/d3b6326e-9fec-42a1-8d2e-d1ad4fcc79a4">SetViewportOrgEx</a>
 

 

