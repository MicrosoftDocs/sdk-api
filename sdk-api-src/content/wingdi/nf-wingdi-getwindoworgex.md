---
UID: NF:wingdi.GetWindowOrgEx
title: GetWindowOrgEx function
author: windows-sdk-content
description: The GetWindowOrgEx function retrieves the x-coordinates and y-coordinates of the window origin for the specified device context.
old-location: gdi\getwindoworgex.htm
tech.root: gdi
ms.assetid: 9579ed10-6d4c-4724-af8b-22cab5b6ff5e
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetWindowOrgEx, GetWindowOrgEx function [Windows GDI], _win32_GetWindowOrgEx, gdi.getwindoworgex, wingdi/GetWindowOrgEx
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
 - Ext-MS-Win-GDI-Draw-L1-1-2.dll
 - Ext-MS-Win-GDI-Draw-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - GetWindowOrgEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- GetWindowOrgEx
: 
---

# GetWindowOrgEx function


## -description


The <b>GetWindowOrgEx</b> function retrieves the x-coordinates and y-coordinates of the window origin for the specified device context.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param lppoint [out]

A pointer to a <a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a> structure that receives the coordinates, in logical units, of the window origin.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -see-also




<a href="https://msdn.microsoft.com/3ebcabf2-9718-47b2-aba0-7cc28fa42e5a">Coordinate Space and Transformation Functions</a>



<a href="https://msdn.microsoft.com/cfb02788-9b73-4451-9e68-2ad310e0e527">Coordinate Spaces and Transformations Overview</a>



<a href="https://msdn.microsoft.com/6e6c7090-edf4-46a3-8bcd-10a00c0cf847">GetViewportOrgEx</a>



<a href="https://msdn.microsoft.com/d3b6326e-9fec-42a1-8d2e-d1ad4fcc79a4">SetViewportOrgEx</a>



<a href="https://msdn.microsoft.com/75409b5a-c003-49f2-aceb-a28330b92b0a">SetWindowOrgEx</a>
 

 

