---
UID: NS:wingdi._RGNDATAHEADER
title: "_RGNDATAHEADER"
author: windows-sdk-content
description: The RGNDATAHEADER structure describes the data returned by the GetRegionData function.
old-location: gdi\rgndataheader.htm
old-project: gdi
ms.assetid: 15990903-8a48-4c47-b527-269d775255a5
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: "*PRGNDATAHEADER, PRGNDATAHEADER, PRGNDATAHEADER structure pointer [Windows GDI], RGNDATAHEADER, RGNDATAHEADER structure [Windows GDI], _RGNDATAHEADER, _win32_RGNDATAHEADER_str, gdi.rgndataheader, wingdi/PRGNDATAHEADER, wingdi/RGNDATAHEADER"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.typenames: RGNDATAHEADER, *PRGNDATAHEADER
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wingdi.h
api_name:
 - RGNDATAHEADER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _RGNDATAHEADER structure


## -description



The <b>RGNDATAHEADER</b> structure describes the data returned by the <a href="https://msdn.microsoft.com/e0d4862d-a405-4c00-b7b0-af4dd60407c0">GetRegionData</a> function.




## -struct-fields




### -field dwSize

The size, in bytes, of the header.


### -field iType

The type of region. This value must be RDH_RECTANGLES.


### -field nCount

The number of rectangles that make up the region.


### -field nRgnSize

The size of the <a href="https://msdn.microsoft.com/3eac0b23-3138-4b34-9c16-6cc185e4de22">RGNDATA</a> buffer required to receive the <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structures that make up the region. If the size is not known, this member can be zero.


### -field rcBound

A bounding rectangle for the region in logical units.


## -see-also




<a href="https://msdn.microsoft.com/e0d4862d-a405-4c00-b7b0-af4dd60407c0">GetRegionData</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>



<a href="https://msdn.microsoft.com/3eac0b23-3138-4b34-9c16-6cc185e4de22">RGNDATA</a>



<a href="https://msdn.microsoft.com/e66d46fd-af6f-43ce-a9f7-21389d14cb89">Region Structures</a>



<a href="https://msdn.microsoft.com/5d2e8624-4d1a-44f7-821e-a54f6f538214">Regions Overview</a>
 

 

