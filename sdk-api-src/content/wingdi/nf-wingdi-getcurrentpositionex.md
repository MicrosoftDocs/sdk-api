---
UID: NF:wingdi.GetCurrentPositionEx
title: GetCurrentPositionEx function
author: windows-sdk-content
description: The GetCurrentPositionEx function retrieves the current position in logical coordinates.
old-location: gdi\getcurrentpositionex.htm
tech.root: gdi
ms.assetid: 23a5ac58-2b88-42d3-ab02-8edb8ef187cc
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetCurrentPositionEx, GetCurrentPositionEx function [Windows GDI], _win32_GetCurrentPositionEx, gdi.getcurrentpositionex, wingdi/GetCurrentPositionEx
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
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - GetCurrentPositionEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetCurrentPositionEx function


## -description


The <b>GetCurrentPositionEx</b> function retrieves the current position in logical coordinates.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param lppt [out]

A pointer to a <a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a> structure that receives the logical coordinates of the current position.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -see-also




<a href="https://msdn.microsoft.com/3ebcabf2-9718-47b2-aba0-7cc28fa42e5a">Coordinate Space and Transformation Functions</a>



<a href="https://msdn.microsoft.com/cfb02788-9b73-4451-9e68-2ad310e0e527">Coordinate Spaces and Transformations Overview</a>



<a href="https://msdn.microsoft.com/af11eeb7-4036-4a90-8685-9b5719f79e01">MoveToEx</a>



<a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a>
 

 

