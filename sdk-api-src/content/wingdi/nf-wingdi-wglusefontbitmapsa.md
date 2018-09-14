---
UID: NF:wingdi.wglUseFontBitmapsA
title: wglUseFontBitmapsA function
author: windows-sdk-content
description: The wglUseFontBitmaps function creates a set of bitmap display lists for use in the current OpenGL rendering context.
old-location: opengl\wglusefontbitmaps.htm
tech.root: OpenGL
ms.assetid: c671965c-9b9d-4206-b467-4884ffd351eb
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: "_ogl_wglUseFontBitmaps, opengl.wglusefontbitmaps, wglUseFontBitmaps, wglUseFontBitmaps function [OpenGL], wglUseFontBitmapsA, wglUseFontBitmapsW, wingdi/wglUseFontBitmaps, wingdi/wglUseFontBitmapsA, wingdi/wglUseFontBitmapsW"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wingdi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: wglUseFontBitmapsW (Unicode) and wglUseFontBitmapsA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - opengl32.dll
api_name:
 - wglUseFontBitmaps
 - wglUseFontBitmapsA
 - wglUseFontBitmapsW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# wglUseFontBitmapsA function


## -description


The <b>wglUseFontBitmaps</b> function creates a set of bitmap display lists for use in the current OpenGL rendering context. The set of bitmap display lists is based on the glyphs in the currently selected font in the device context. You can then use bitmaps to draw characters in an OpenGL image.

The <b>wglUseFontBitmaps</b> function creates <i>count</i> display lists, one for each of a run of <i>count</i> glyphs that begins with the first glyph in the <i>hdc</i> parameter's selected fonts.


## -parameters




### -param arg1

TBD


### -param arg2

TBD


### -param arg3

TBD


### -param arg4

TBD






#### - count

Specifies the number of glyphs in the run of glyphs that will be used to form glyph bitmap display lists. The function creates <i>count</i> display lists, one for each glyph in the run.


#### - first

Specifies the first glyph in the run of glyphs that will be used to form glyph bitmap display lists.


#### - listBase

Specifies a starting display list.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The <b>wglUseFontBitmaps</b> function defines <i>count</i> display lists in the current OpenGL rendering context. Each display list has an identifying number, starting at <i>listBase</i>. Each display list consists of a single call to <a href="https://msdn.microsoft.com/3cd8e41b-016b-4610-833a-048b5e50ae7c">glBitmap</a>. The definition of bitmap <i>listBase</i> + <i>i</i> is taken from the glyph <i>first</i> + <i>i</i> of the font currently selected in the device context specified by <i>hdc</i>. If a glyph is not defined, then the function defines an empty display list for it.

The <b>wglUseFontBitmaps</b> function creates bitmap text in the plane of the screen. It enables the labeling of objects in OpenGL.

In the current version of Microsoft's implementation of OpenGL, you cannot make GDI calls to a device context that has a double-buffered pixel format. Therefore, you cannot use the GDI fonts and text functions with such device contexts. You can use the <b>wglUseFontBitmaps</b> function to circumvent this limitation and draw text in a double-buffered device context.

The function determines the parameters of each call to <b>glBitmap</b> as follows.

<table>
<tr>
<th>glBitmap Parameter</th>
<th>Meaning</th>
</tr>
<tr>
<td><i>width</i></td>
<td>The width of the glyph's bitmap, as returned in the <b>gmBlackBoxX</b> member of the glyph's <a href="https://msdn.microsoft.com/a6fa3813-56f7-4b54-b21d-8aabc2309a34">GLYPHMETRICS</a> structure.</td>
</tr>
<tr>
<td><i>height</i></td>
<td>The height of the glyph's bitmap, as returned in the <b>gmBlackBoxY</b> member of the glyph's <b>GLYPHMETRICS</b> structure.</td>
</tr>
<tr>
<td><i>xorig</i></td>
<td>The x offset of the glyph's origin, as returned in the <b>gmptGlyphOrigin.x</b> member of the glyph's <b>GLYPHMETRICS</b> structure.</td>
</tr>
<tr>
<td><i>yorig</i></td>
<td>The y offset of the glyph's origin, as returned in the <b>gmptGlyphOrigin.y</b> member of the glyph's <b>GLYPHMETRICS</b> structure.</td>
</tr>
<tr>
<td><i>xmove</i></td>
<td>The horizontal distance to the origin of the next character cell, as returned in the <b>gmCellIncX</b> member of the glyph's <b>GLYPHMETRICS</b> structure.</td>
</tr>
<tr>
<td><i>ymove</i></td>
<td>The vertical distance to the origin of the next character cell as returned in the <b>gmCellIncY</b> member of the glyph's <b>GLYPHMETRICS</b> structure.</td>
</tr>
<tr>
<td><i>bitmap</i></td>
<td>The bitmap for the glyph, as returned by <a href="https://msdn.microsoft.com/08f06007-5b21-44ab-b234-21a58c94ed4e">GetGlyphOutline</a> with <i>uFormat</i> equal to 1.</td>
</tr>
</table>
 


#### Examples

The following code example shows how to use <b>wglUseFontBitmaps</b> to draw some text.


```cpp
HDC    hdc; 
HGLRC  hglrc; 
 
// create a rendering context  
hglrc = wglCreateContext (hdc); 
 
// make it the calling thread's current rendering context  
wglMakeCurrent (hdc, hglrc); 
 
// now we can call OpenGL API  
 
// make the system font the device context's selected font  
SelectObject (hdc, GetStockObject (SYSTEM_FONT)); 
 
// create the bitmap display lists  
// we're making images of glyphs 0 thru 254  
// the display list numbering starts at 1000, an arbitrary choice  
wglUseFontBitmaps (hdc, 0, 255, 1000); 
 
// display a string:  
// indicate start of glyph display lists  
glListBase (1000); 
// now draw the characters in a string  
glCallLists (24, GL_UNSIGNED_BYTE, "Hello Windows OpenGL World");
```





## -see-also




<a href="https://msdn.microsoft.com/a6fa3813-56f7-4b54-b21d-8aabc2309a34">GLYPHMETRICS</a>



<a href="https://msdn.microsoft.com/08f06007-5b21-44ab-b234-21a58c94ed4e">GetGlyphOutline</a>



<a href="https://msdn.microsoft.com/589a86f1-598d-4175-97fc-27ca0b254935">OpenGL on Windows</a>



<a href="https://msdn.microsoft.com/52053370-d88b-4faf-bdcd-4663c6d5270d">WGL Functions</a>



<a href="https://msdn.microsoft.com/3cd8e41b-016b-4610-833a-048b5e50ae7c">glBitmap</a>



<a href="https://msdn.microsoft.com/7c0a00df-91ee-44ad-9e02-97c1b078e87f">glCallLists</a>



<a href="https://msdn.microsoft.com/df82f699-b2af-471a-83f3-5620857ba45d">glListBase</a>



<a href="https://msdn.microsoft.com/08a86563-c6ca-4efb-9096-bc487fc5037c">wglUseFontOutlines</a>
 

 

