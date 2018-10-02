---
UID: NF:wingdi.GetGraphicsMode
title: GetGraphicsMode function
author: windows-sdk-content
description: The GetGraphicsMode function retrieves the current graphics mode for the specified device context.
old-location: gdi\getgraphicsmode.htm
tech.root: gdi
ms.assetid: 62e2960b-d414-4e84-a94f-60b192071402
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetGraphicsMode, GetGraphicsMode function [Windows GDI], _win32_GetGraphicsMode, gdi.getgraphicsmode, wingdi/GetGraphicsMode
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
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - GetGraphicsMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetGraphicsMode function


## -description


The <b>GetGraphicsMode</b> function retrieves the current graphics mode for the specified device context.


## -parameters




### -param hdc [in]

A handle to the device context.


## -returns



If the function succeeds, the return value is the current graphics mode. It can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>GM_COMPATIBLE</td>
<td>The current graphics mode is the compatible graphics mode, a mode that is compatible with 16-bit Windows. In this graphics mode, an application cannot set or modify the world transformation for the specified device context. The compatible graphics mode is the default graphics mode.</td>
</tr>
<tr>
<td>GM_ADVANCED</td>
<td>The current graphics mode is the advanced graphics mode, a mode that allows world transformations. In this graphics mode, an application can set or modify the world transformation for the specified device context.</td>
</tr>
</table>
 

Otherwise, the return value is zero.




## -remarks



An application can set the graphics mode for a device context by calling the <a href="https://msdn.microsoft.com/73824a14-2951-45a2-98cd-156418c59a2d">SetGraphicsMode</a> function.




## -see-also




<a href="https://msdn.microsoft.com/3ebcabf2-9718-47b2-aba0-7cc28fa42e5a">Coordinate Space and Transformation Functions</a>



<a href="https://msdn.microsoft.com/cfb02788-9b73-4451-9e68-2ad310e0e527">Coordinate Spaces and Transformations Overview</a>



<a href="https://msdn.microsoft.com/73824a14-2951-45a2-98cd-156418c59a2d">SetGraphicsMode</a>
 

 

