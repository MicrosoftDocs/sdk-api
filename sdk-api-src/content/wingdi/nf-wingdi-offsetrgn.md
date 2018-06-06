---
UID: NF:wingdi.OffsetRgn
title: OffsetRgn function
author: windows-sdk-content
description: The OffsetRgn function moves a region by the specified offsets.
old-location: gdi\offsetrgn.htm
old-project: gdi
ms.assetid: 5228c614-3278-4852-a867-7eed57359aef
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: OffsetRgn, OffsetRgn function [Windows GDI], _win32_OffsetRgn, gdi.offsetrgn, wingdi/OffsetRgn
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
 - Ext-MS-Win-RTCore-GDI-rgn-l1-1-0.dll
 - ext-ms-win-rtcore-gdi-rgn-l1-1-1.dll
api_name:
 - OffsetRgn
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# OffsetRgn function


## -description


The <b>OffsetRgn</b> function moves a region by the specified offsets.


## -parameters




### -param hrgn [in]

Handle to the region to be moved.


### -param x

TBD


### -param y

TBD




#### - nXOffset [in]

Specifies the number of logical units to move left or right.


#### - nYOffset [in]

Specifies the number of logical units to move up or down.


## -returns



The return value specifies the new region's complexity. It can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>NULLREGION</td>
<td>Region is empty.</td>
</tr>
<tr>
<td>SIMPLEREGION</td>
<td>Region is a single rectangle.</td>
</tr>
<tr>
<td>COMPLEXREGION</td>
<td>Region is more than one rectangle.</td>
</tr>
<tr>
<td>ERROR</td>
<td>An error occurred; region is unaffected.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/3a42fc7a-4c07-4540-99a7-520f99532f33">Region Functions</a>



<a href="https://msdn.microsoft.com/5d2e8624-4d1a-44f7-821e-a54f6f538214">Regions Overview</a>
 

 

