---
UID: NF:wingdi.OffsetWindowOrgEx
title: OffsetWindowOrgEx function
author: windows-sdk-content
description: The OffsetWindowOrgEx function modifies the window origin for a device context using the specified horizontal and vertical offsets.
old-location: gdi\offsetwindoworgex.htm
tech.root: gdi
ms.assetid: 085f40ac-d91f-4853-8ad1-1fc5da08b981
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: OffsetWindowOrgEx, OffsetWindowOrgEx function [Windows GDI], _win32_OffsetWindowOrgEx, gdi.offsetwindoworgex, wingdi/OffsetWindowOrgEx
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - ext-ms-win-gdi-draw-l1-1-2.dll
 - Ext-MS-Win-GDI-Draw-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - OffsetWindowOrgEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# OffsetWindowOrgEx function


## -description


The <b>OffsetWindowOrgEx</b> function modifies the window origin for a device context using the specified horizontal and vertical offsets.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param x [in]

The horizontal offset, in logical units.


### -param y [in]

The vertical offset, in logical units.


### -param lppt [out]

A pointer to a <a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a> structure. The logical coordinates of the previous window origin are placed in this structure. If <i>lpPoint</i> is <b>NULL</b>, the previous origin is not returned.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -see-also




<a href="https://msdn.microsoft.com/3ebcabf2-9718-47b2-aba0-7cc28fa42e5a">Coordinate Space and Transformation Functions</a>



<a href="https://msdn.microsoft.com/cfb02788-9b73-4451-9e68-2ad310e0e527">Coordinate Spaces and Transformations Overview</a>



<a href="https://msdn.microsoft.com/6e6c7090-edf4-46a3-8bcd-10a00c0cf847">GetViewportOrgEx</a>



<a href="https://msdn.microsoft.com/54311cbe-1c54-4193-8991-891dbd0856bf">OffsetViewportOrgEx</a>



<a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a>
 

 

