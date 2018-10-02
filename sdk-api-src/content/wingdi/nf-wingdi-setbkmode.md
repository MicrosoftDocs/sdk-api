---
UID: NF:wingdi.SetBkMode
title: SetBkMode function
author: windows-sdk-content
description: The SetBkMode function sets the background mix mode of the specified device context. The background mix mode is used with text, hatched brushes, and pen styles that are not solid lines.
old-location: gdi\setbkmode.htm
tech.root: gdi
ms.assetid: 60e4467a-14ab-421e-b174-4b9c0134ce72
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: OPAQUE, SetBkMode, SetBkMode function [Windows GDI], TRANSPARENT, _win32_SetBkMode, gdi.setbkmode, wingdi/SetBkMode
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
 - Ext-MS-Win-GDI-Draw-l1-1-1.dll
 - ext-ms-win-gdi-draw-l1-1-2.dll
 - Ext-MS-Win-GDI-Draw-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - SetBkMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetBkMode function


## -description


The <b>SetBkMode</b> function sets the background mix mode of the specified device context. The background mix mode is used with text, hatched brushes, and pen styles that are not solid lines.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param mode [in]

The background mode. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="OPAQUE"></a><a id="opaque"></a><dl>
<dt><b>OPAQUE</b></dt>
</dl>
</td>
<td width="60%">
Background is filled with the current background color before the text, hatched brush, or pen is drawn.

</td>
</tr>
<tr>
<td width="40%"><a id="TRANSPARENT"></a><a id="transparent"></a><dl>
<dt><b>TRANSPARENT</b></dt>
</dl>
</td>
<td width="60%">
Background remains untouched.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the return value specifies the previous background mode.

If the function fails, the return value is zero.




## -remarks



The <b>SetBkMode</b> function affects the line styles for lines drawn using a pen created by the <a href="https://msdn.microsoft.com/882facd2-7e06-48f6-82e4-f20e4d5adc92">CreatePen</a> function. <b>SetBkMode</b> does not affect lines drawn using a pen created by the <a href="https://msdn.microsoft.com/a1e81314-4fe6-481f-af96-24ebf56332cf">ExtCreatePen</a> function.


#### Examples

To see how to make the background of a  hatch brush transparent or opaque, refer to the example shown in the <a href="https://msdn.microsoft.com/0b5849d6-1e22-4ac5-980c-2f2a73b16adb">CreateHatchBrush</a>   topic.

The next example draws a string 36 times, rotating it 10 degrees 
counterclockwise each time. It also sets the background mode to transparent to make the text visible.


```cpp
#include "strsafe.h"
LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    int wmId, wmEvent;
    PAINTSTRUCT ps;
    HDC hdc;

    switch (message)
    {
    
    case WM_PAINT:
        {
        hdc = BeginPaint(hWnd, &ps);
        RECT rc; 
        int angle; 
        HGDIOBJ hfnt, hfntPrev; 
        WCHAR lpszRotate[22] = TEXT("String to be rotated.");
        HRESULT hr; 
        size_t pcch = 22;
 
// Allocate memory for a LOGFONT structure. 
 
PLOGFONT plf = (PLOGFONT) LocalAlloc(LPTR, sizeof(LOGFONT)); 
 
 
// Specify a font typeface name and weight. 
 
hr = StringCchCopy(plf->lfFaceName, 6, TEXT("Arial"));
if (FAILED(hr))
{
// TODO: write error handler
}

plf->lfWeight = FW_NORMAL; 
 
// Retrieve the client-rectangle dimensions. 
 
GetClientRect(hWnd, &rc); 
 
// Set the background mode to transparent for the 
// text-output operation. 
 
SetBkMode(hdc, TRANSPARENT); 
 
// Draw the string 36 times, rotating 10 degrees 
// counter-clockwise each time. 
 
for (angle = 0; angle < 3600; angle += 100) 
{ 
    plf->lfEscapement = angle; 
    hfnt = CreateFontIndirect(plf); 
    hfntPrev = SelectObject(hdc, hfnt);
    
    //
    // The StringCchLength call is fitted to the lpszRotate string
    //
    hr = StringCchLength(lpszRotate, 22, &pcch);
    if (FAILED(hr))
    {
    // TODO: write error handler
    } 
    TextOut(hdc, rc.right / 2, rc.bottom / 2, 
        lpszRotate, pcch); 
    SelectObject(hdc, hfntPrev); 
    DeleteObject(hfnt); 
} 
 
// Reset the background mode to its default. 
 
SetBkMode(hdc, OPAQUE); 
 
// Free the memory allocated for the LOGFONT structure. 
 
LocalFree((LOCALHANDLE) plf); 
        EndPaint(hWnd, &ps);
        break;
        }
    case WM_DESTROY:
        PostQuitMessage(0);
        break;
    default:
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
    return 0;
}

```


<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/882facd2-7e06-48f6-82e4-f20e4d5adc92">CreatePen</a>



<a href="https://msdn.microsoft.com/a1e81314-4fe6-481f-af96-24ebf56332cf">ExtCreatePen</a>



<a href="https://msdn.microsoft.com/3faedb48-3163-48fd-b26e-712de9c4bfaf">GetBkMode</a>



<a href="https://msdn.microsoft.com/ec18323e-c13b-4328-83bf-9e4ed4a712b8">Painting and Drawing Functions</a>



<a href="https://msdn.microsoft.com/8e6034af-4dea-4579-b476-52f6dd3d5bc7">Painting and Drawing Overview</a>
 

 

