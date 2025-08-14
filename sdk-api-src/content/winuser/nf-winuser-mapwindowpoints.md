---
UID: NF:winuser.MapWindowPoints
title: MapWindowPoints function (winuser.h)
description: The MapWindowPoints function converts (maps) a set of points from a coordinate space relative to one window to a coordinate space relative to another window.
helpviewer_keywords: ["MapWindowPoints","MapWindowPoints function [Windows GDI]","_win32_MapWindowPoints","gdi.mapwindowpoints","winuser/MapWindowPoints"]
old-location: gdi\mapwindowpoints.htm
tech.root: gdi
ms.assetid: 01c3b794-c1ca-467f-a4da-c6622453ee97
ms.date: 12/05/2018
ms.keywords: MapWindowPoints, MapWindowPoints function [Windows GDI], _win32_MapWindowPoints, gdi.mapwindowpoints, winuser/MapWindowPoints
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MapWindowPoints
 - winuser/MapWindowPoints
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-window-ext-l1-1-1.dll
 - ext-ms-win-ntuser-window-l1-1-6.dll
 - ext-ms-win-ntuser-window-l1-1-5.dll
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
req.apiset: ext-ms-win-ntuser-window-l1-1-2 (introduced in Windows 10, version 10.0.10240)
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

A pointer to an array of <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structures that contain the set of points to be converted. The points are in device units. This parameter can also point to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure, in which case the <i>cPoints</i> parameter should be set to 2.

### -param cPoints [in]

The number of <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structures in the array pointed to by the <i>lpPoints</i> parameter.

## -returns

If the function succeeds, the low-order word of the return value is the number of pixels added to the horizontal coordinate of each source point in order to compute the horizontal coordinate of each destination point. (In addition to that, if precisely one of <i>hWndFrom</i> and <i>hWndTo</i> is mirrored, then each resulting horizontal coordinate is multiplied by -1.) The high-order word is the number of pixels added to the vertical coordinate of each source point in order to compute the vertical coordinate of each destination point.

If the function fails, the return value is zero. Call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror">SetLastError</a> prior to calling this method to differentiate an error return value from a legitimate "0" return value.

## -remarks

If <i>hWndFrom</i> or <i>hWndTo</i> (or both) are mirrored windows (that is, have <b>WS_EX_LAYOUTRTL</b> extended style) and precisely two points are passed in <i>lpPoints</i>, <b>MapWindowPoints</b> will interpret those two points as a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> and possibly automatically swap the left and right fields of that rectangle to ensure that left is not greater than right. If any number of points other than 2 is passed in <i>lpPoints</i>, then <b>MapWindowPoints</b> will correctly map the coordinates of each of those points separately, so if you pass in a pointer to an array of more than one rectangle in <i>lpPoints</i>, the new rectangles may get their left field greater than right. Thus, to guarantee the correct transformation of rectangle coordinates, you must call <b>MapWindowPoints</b> with one <b>RECT</b> pointer at a time, as shown in the following example:


```cpp

   RECT        rc[10];

   for(int i = 0; i < (sizeof(rc)/sizeof(rc[0])); i++)
   {
       MapWindowPoints(hWnd1, hWnd2, (LPPOINT)(&rc[i]), (sizeof(RECT)/sizeof(POINT)) );
   }

```


Also, if you need to map precisely two independent points and don't want the <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> logic applied to them by <b>MapWindowPoints</b>, to guarantee the correct result you must call <b>MapWindowPoints</b> with one <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> pointer at a time, as shown in the following example:


```cpp

   POINT pt[2];

   MapWindowPoints(hWnd1, hWnd2, &pt[0], 1);
   MapWindowPoints(hWnd1, hWnd2, &pt[1], 1);

```

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-clienttoscreen">ClientToScreen</a>



<a href="/windows/desktop/gdi/coordinate-space-and-transformation-functions">Coordinate Space and Transformation Functions</a>



<a href="/windows/desktop/gdi/coordinate-spaces-and-transformations">Coordinate Spaces and Transformations Overview</a>



<a href="/windows/win32/api/windef/ns-windef-point">POINT</a>



<a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>



<a href="/windows/desktop/api/winuser/nf-winuser-screentoclient">ScreenToClient</a>
