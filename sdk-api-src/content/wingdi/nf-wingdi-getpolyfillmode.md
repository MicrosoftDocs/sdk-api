---
UID: NF:wingdi.GetPolyFillMode
title: GetPolyFillMode function
author: windows-sdk-content
description: The GetPolyFillMode function retrieves the current polygon fill mode.
old-location: gdi\getpolyfillmode.htm
old-project: gdi
ms.assetid: febf96fb-bf2e-4eb2-ab5f-89741a1decad
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetPolyFillMode, GetPolyFillMode function [Windows GDI], _win32_GetPolyFillMode, gdi.getpolyfillmode, wingdi/GetPolyFillMode
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
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - GetPolyFillMode
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetPolyFillMode function


## -description


The <b>GetPolyFillMode</b> function retrieves the current polygon fill mode.


## -parameters




### -param hdc [in]

Handle to the device context.


## -returns



If the function succeeds, the return value specifies the polygon fill mode, which can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>ALTERNATE</td>
<td>Selects alternate mode (fills area between odd-numbered and even-numbered polygon sides on each scan line).</td>
</tr>
<tr>
<td>WINDING</td>
<td>Selects winding mode (fills any region with a nonzero winding value).</td>
</tr>
</table>
 

If an error occurs, the return value is zero.




## -see-also




<a href="https://msdn.microsoft.com/3a42fc7a-4c07-4540-99a7-520f99532f33">Region Functions</a>



<a href="https://msdn.microsoft.com/5d2e8624-4d1a-44f7-821e-a54f6f538214">Regions Overview</a>



<a href="https://msdn.microsoft.com/233926c4-2658-405d-89b6-05ece844623d">SetPolyFillMode</a>
 

 

