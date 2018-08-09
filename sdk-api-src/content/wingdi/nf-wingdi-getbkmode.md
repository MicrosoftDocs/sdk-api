---
UID: NF:wingdi.GetBkMode
title: GetBkMode function
author: windows-sdk-content
description: The GetBkMode function returns the current background mix mode for a specified device context. The background mix mode of a device context affects text, hatched brushes, and pen styles that are not solid lines.
old-location: gdi\getbkmode.htm
old-project: gdi
ms.assetid: 3faedb48-3163-48fd-b26e-712de9c4bfaf
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetBkMode, GetBkMode function [Windows GDI], _win32_GetBkMode, gdi.getbkmode, wingdi/GetBkMode
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
tech.root: 
req.typenames: DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Draw-l1-1-1.dll
 - ext-ms-win-gdi-draw-l1-1-2.dll
 - Ext-MS-Win-GDI-Draw-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - GetBkMode
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetBkMode function


## -description


The <b>GetBkMode</b> function returns the current background mix mode for a specified device context. The background mix mode of a device context affects text, hatched brushes, and pen styles that are not solid lines.


## -parameters




### -param hdc [in]

Handle to the device context whose background mode is to be returned.


## -returns



If the function succeeds, the return value specifies the current background mix mode, either OPAQUE or TRANSPARENT.

If the function fails, the return value is zero.




## -see-also




<a href="https://msdn.microsoft.com/1c6e8d05-4b8d-476d-852c-f06f316cb8b7">GetBkColor</a>



<a href="https://msdn.microsoft.com/ec18323e-c13b-4328-83bf-9e4ed4a712b8">Painting and Drawing Functions</a>



<a href="https://msdn.microsoft.com/8e6034af-4dea-4579-b476-52f6dd3d5bc7">Painting and Drawing Overview</a>



<a href="https://msdn.microsoft.com/60e4467a-14ab-421e-b174-4b9c0134ce72">SetBkMode</a>
 

 

