---
UID: NF:wingdi.UnrealizeObject
title: UnrealizeObject function
author: windows-sdk-content
description: The UnrealizeObject function resets the origin of a brush or resets a logical palette.
old-location: gdi\unrealizeobject.htm
tech.root: gdi
ms.assetid: b84cd0b3-fdf1-4f12-bc45-308032d6d698
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: UnrealizeObject, UnrealizeObject function [Windows GDI], _win32_UnrealizeObject, gdi.unrealizeobject, wingdi/UnrealizeObject
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
 - UnrealizeObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# UnrealizeObject function


## -description


The <b>UnrealizeObject</b> function resets the origin of a brush or resets a logical palette. If the <i>hgdiobj</i> parameter is a handle to a brush, <b>UnrealizeObject</b> directs the system to reset the origin of the brush the next time it is selected. If the <i>hgdiobj</i> parameter is a handle to a logical palette, <b>UnrealizeObject</b> directs the system to realize the palette as though it had not previously been realized. The next time the application calls the <a href="https://msdn.microsoft.com/1c744ad2-09bc-455f-bc3c-9a2583b57a30">RealizePalette</a> function for the specified palette, the system completely remaps the logical palette to the system palette.


## -parameters




### -param h [in]

A handle to the logical palette to be reset.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The <b>UnrealizeObject</b> function should not be used with stock objects. For example, the default palette, obtained by calling <a href="https://msdn.microsoft.com/b14ddc05-7e7b-4fc6-b7e3-efe892df7e21">GetStockObject</a> (DEFAULT_PALETTE), is a stock object.

A palette identified by <i>hgdiobj</i> can be the currently selected palette of a device context.

If <i>hgdiobj</i> is a brush, <b>UnrealizeObject</b> does nothing, and the function returns <b>TRUE</b>. Use <a href="https://msdn.microsoft.com/dcc7575a-49fd-4306-8baa-57e9e0d5ed1f">SetBrushOrgEx</a> to set the origin of a brush.




## -see-also




<a href="https://msdn.microsoft.com/9dd32d4a-30bd-406f-a934-bb71ad4ca2cb">Color Functions</a>



<a href="https://msdn.microsoft.com/d1a25f13-6b47-4be7-927b-814dd6ae81f8">Colors Overview</a>



<a href="https://msdn.microsoft.com/b14ddc05-7e7b-4fc6-b7e3-efe892df7e21">GetStockObject</a>



<a href="https://msdn.microsoft.com/1c744ad2-09bc-455f-bc3c-9a2583b57a30">RealizePalette</a>



<a href="https://msdn.microsoft.com/dcc7575a-49fd-4306-8baa-57e9e0d5ed1f">SetBrushOrgEx</a>
 

 

