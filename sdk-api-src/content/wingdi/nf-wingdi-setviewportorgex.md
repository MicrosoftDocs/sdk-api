---
UID: NF:wingdi.SetViewportOrgEx
title: SetViewportOrgEx function (wingdi.h)

description: The SetViewportOrgEx function specifies which device point maps to the window origin (0,0).
old-location: gdi\setviewportorgex.htm
tech.root: gdi
ms.assetid: d3b6326e-9fec-42a1-8d2e-d1ad4fcc79a4

ms.date: 12/05/2018
ms.keywords: SetViewportOrgEx, SetViewportOrgEx function [Windows GDI], _win32_SetViewportOrgEx, gdi.setviewportorgex, wingdi/SetViewportOrgEx
ms.topic: function
f1_keywords: 
 - "wingdi/SetViewportOrgEx"
dev_langs:
 - c++
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
 - SetViewportOrgEx
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetViewportOrgEx function


## -description


The <b>SetViewportOrgEx</b> function specifies which device point maps to the window origin (0,0).


## -parameters




### -param hdc [in]

A handle to the device context.


### -param x [in]

The x-coordinate, in device units, of the new viewport origin.


### -param y [in]

The y-coordinate, in device units, of the new viewport origin.


### -param lppt [out]

A pointer to a <a href="https://docs.microsoft.com/previous-versions/dd162805(v=vs.85)">POINT</a> structure that receives the previous viewport origin, in device coordinates. If <i>lpPoint</i> is <b>NULL</b>, this parameter is not used.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



This function (along with <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-setviewportextex">SetViewportExtEx</a> and <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-setwindowextex">SetWindowExtEx</a>) helps define the mapping from the logical coordinate space (also known as a <i>window</i>) to the device coordinate space (the <i>viewport</i>). <b>SetViewportOrgEx</b> specifies which device point maps to the logical point (0,0). It has the effect of shifting the axes so that the logical point (0,0) no longer refers to the upper-left corner.


```cpp

//map the logical point (0,0) to the device point (xViewOrg, yViewOrg) 
SetViewportOrgEx ( hdc, xViewOrg, yViewOrg, NULL)

```


This is related to the <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-setwindoworgex">SetWindowOrgEx</a> function. Generally, you will use one function or the other, but not both. Regardless of your use of <b>SetWindowOrgEx</b> and <b>SetViewportOrgEx</b>, the device point (0,0) is always the upper-left corner.


#### Examples

For an example, see <a href="https://docs.microsoft.com/windows/desktop/gdi/redrawing-in-the-update-region">Redrawing in the Update Region</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/gdi/coordinate-space-and-transformation-functions">Coordinate Space and Transformation Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/coordinate-spaces-and-transformations">Coordinate Spaces and Transformations Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-getviewportorgex">GetViewportOrgEx</a>



<a href="https://docs.microsoft.com/previous-versions/dd162805(v=vs.85)">POINT</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-setwindoworgex">SetWindowOrgEx</a>
 

 

