---
UID: NF:winuser.MapWindowPoints
title: MapWindowPoints function
author: windows-sdk-content
description: The MapWindowPoints function converts (maps) a set of points from a coordinate space relative to one window to a coordinate space relative to another window.
old-location: gdi\mapwindowpoints.htm
tech.root: gdi
ms.assetid: 01c3b794-c1ca-467f-a4da-c6622453ee97
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: MapWindowPoints, MapWindowPoints function [Windows GDI], _win32_MapWindowPoints, gdi.mapwindowpoints, winuser/MapWindowPoints
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winuser.h
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - user32.dll
 - Ext-MS-Win-NTUser-GUI-l1-1-0.dll
 - Ext-MS-Win-NTUser-GUI-l1-1-1.dll
 - Ext-MS-Win-NTUser-Window-l1-1-2.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
 - minuser.dll
 - api-ms-win-ntuser-ie-gui-l1-1-0.dll
 - ie_stubs.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - MapWindowPoints
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MapWindowPoints function


## -description


The <b>MapWindowPoints</b> function converts (maps) a set of points from a coordinate space relative to one window to a coordinate space relative to another window.


## -parameters




### -param hWndFrom [in]

A handle to the window from which points are converted. If this parameter is <b>NULL</b> or HWND_DESKTOP, the points are presumed to be in screen coordinates.


### -param hWndTo [in]

A handle to the window to which points are converted. If this parameter is <b>NULL</b> or HWND_DESKTOP, the points are converted to screen coordinates.


### -param lpPoints [in, out]

A pointer to an array of <a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a> structures that contain the set of points to be converted. The points are in device units. This parameter can also point to a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure, in which case the <i>cPoints</i> parameter should be set to 2.


### -param cPoints [in]

The number of <a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a> structures in the array pointed to by the <i>lpPoints</i> parameter.


## -returns



If the function succeeds, the low-order word of the return value is the number of pixels added to the horizontal coordinate of each source point in order to compute the horizontal coordinate of each destination point. (In addition to that, if precisely one of <i>hWndFrom</i> and <i>hWndTo</i> is mirrored, then each resulting horizontal coordinate is multiplied by -1.) The high-order word is the number of pixels added to the vertical coordinate of each source point in order to compute the vertical coordinate of each destination point.

If the function fails, the return value is zero. Call <a href="https://msdn.microsoft.com/d9da833f-36ca-4046-8d2f-cd4449dd3c63">SetLastError</a> prior to calling this method to differentiate an error return value from a legitimate "0" return value.




## -remarks



If <i>hWndFrom</i> or <i>hWndTo</i> (or both) are mirrored windows (that is, have <b>WS_EX_LAYOUTRTL</b> extended style) and precisely two points are passed in <i>lpPoints</i>, <b>MapWindowPoints</b> will interpret those two points as a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> and possibly automatically swap the left and right fields of that rectangle to ensure that left is not greater than right. If any number of points other than 2 is passed in <i>lpPoints</i>, then <b>MapWindowPoints</b> will correctly map the coordinates of each of those points separately, so if you pass in a pointer to an array of more than one rectangle in <i>lpPoints</i>, the new rectangles may get their left field greater than right. Thus, to guarantee the correct transformation of rectangle coordinates, you must call <b>MapWindowPoints</b> with one <b>RECT</b> pointer at a time, as shown in the following example:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
   RECT        rc[10];

   for(int i = 0; i &lt; (sizeof(rc)/sizeof(rc[0])); i++)
   {
       MapWindowPoints(hWnd1, hWnd2, (LPPOINT)(&amp;rc[i]), (sizeof(RECT)/sizeof(POINT)) );
   }
</pre>
</td>
</tr>
</table></span></div>
Also, if you need to map precisely two independent points and don't want the <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> logic applied to them by <b>MapWindowPoints</b>, to guarantee the correct result you must call <b>MapWindowPoints</b> with one <a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a> pointer at a time, as shown in the following example:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
   POINT pt[2];

   MapWindowPoints(hWnd1, hWnd2, &amp;pt[0], 1);
   MapWindowPoints(hWnd1, hWnd2, &amp;pt[1], 1);
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/3b1e2699-7f5f-444d-9072-f2ca7c8fa511">ClientToScreen</a>



<a href="https://msdn.microsoft.com/3ebcabf2-9718-47b2-aba0-7cc28fa42e5a">Coordinate Space and Transformation Functions</a>



<a href="https://msdn.microsoft.com/cfb02788-9b73-4451-9e68-2ad310e0e527">Coordinate Spaces and Transformations Overview</a>



<a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a>



<a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>



<a href="https://msdn.microsoft.com/5d3e65d1-e0c8-4063-b2e8-dd9f482d3378">ScreenToClient</a>
 

 

