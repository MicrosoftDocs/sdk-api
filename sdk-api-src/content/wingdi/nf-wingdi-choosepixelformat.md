---
UID: NF:wingdi.ChoosePixelFormat
title: ChoosePixelFormat function
author: windows-sdk-content
description: The ChoosePixelFormat function attempts to match an appropriate pixel format supported by a device context to a given pixel format specification.
old-location: opengl\choosepixelformat.htm
tech.root: OpenGL
ms.assetid: 17bd0a2c-5257-4ae3-80f4-a5ad536169fb
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ChoosePixelFormat, ChoosePixelFormat function [OpenGL], _ogl_ChoosePixelFormat, opengl.choosepixelformat, wingdi/ChoosePixelFormat
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
 - Ext-MS-Win-GDI-Draw-L1-1-3.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - ChoosePixelFormat
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ChoosePixelFormat function


## -description


The <b>ChoosePixelFormat</b> function attempts to match an appropriate pixel format supported by a device context to a given pixel format specification.


## -parameters




### -param hdc

Specifies the device context that the function examines to determine the best match for the pixel format descriptor pointed to by <i>ppfd</i>.


### -param ppfd

Pointer to a <a href="https://msdn.microsoft.com/1480dea3-ae74-4e8b-b4de-fca8de5d8395">PIXELFORMATDESCRIPTOR</a> structure that specifies the requested pixel format. In this context, the members of the <b>PIXELFORMATDESCRIPTOR</b> structure that <i>ppfd</i> points to are used as follows:

<table>
<tr>
<td><i>nSize</i></td>
<td>Specifies the size of the <a href="https://msdn.microsoft.com/1480dea3-ae74-4e8b-b4de-fca8de5d8395">PIXELFORMATDESCRIPTOR</a> data structure. Set this member to <code>sizeof(PIXELFORMATDESCRIPTOR)</code>.</td>
</tr>
<tr>
<td><i>nVersion</i></td>
<td>Specifies the version number of the <a href="https://msdn.microsoft.com/1480dea3-ae74-4e8b-b4de-fca8de5d8395">PIXELFORMATDESCRIPTOR</a> data structure. Set this member to 1.</td>
</tr>
<tr>
<td><i>dwFlags</i></td>
<td>A set of bit flags that specify properties of the pixel buffer. You can combine the following bit flag constants by using bitwise-OR. If any of the following flags are set, the <b>ChoosePixelFormat</b> function attempts to match pixel formats that also have that flag or flags set. Otherwise, <b>ChoosePixelFormat</b> ignores that flag in the pixel formats: <b>PFD_DRAW_TO_WINDOW</b>, <b>PFD_DRAW_TO_BITMAP</b>, <b>PFD_SUPPORT_GDI</b>, <b>PFD_SUPPORT_OPENGL</b> If any of the following flags are set, <b>ChoosePixelFormat</b> attempts to match pixel formats that also have that flag or flags set. Otherwise, it attempts to match pixel formats without that flag set: <b>PFD_DOUBLEBUFFER PFD_STEREO</b> If the following flag is set, the function ignores the <b>PFD_DOUBLEBUFFER</b> flag in the pixel formats: <b>PFD_DOUBLEBUFFER_DONTCARE</b> If the following flag is set, the function ignores the <b>PFD_STEREO</b> flag in the pixel formats: <b>PFD_STEREO_DONTCARE</b></td>
</tr>
<tr>
<td><i>iPixelType</i></td>
<td>Specifies the type of pixel format for the function to consider: <b>PFD_TYPE_RGBA</b>, <b>PFD_TYPE_COLORINDEX</b></td>
</tr>
<tr>
<td><i>cColorBits</i></td>
<td>Zero or greater.</td>
</tr>
<tr>
<td><i>cRedBits</i></td>
<td>Not used.</td>
</tr>
<tr>
<td><i>cRedShift</i></td>
<td>Not used.</td>
</tr>
<tr>
<td><i>cGreenBits</i></td>
<td>Not used.</td>
</tr>
<tr>
<td><i>cGreenShift</i></td>
<td>Not used.</td>
</tr>
<tr>
<td><i>cBlueBits</i></td>
<td>Not used.</td>
</tr>
<tr>
<td><i>cBlueShift</i></td>
<td>Not used.</td>
</tr>
<tr>
<td><i>cAlphaBits</i></td>
<td>Zero or greater.</td>
</tr>
<tr>
<td><i>cAlphaShift</i></td>
<td>Not used.</td>
</tr>
<tr>
<td><i>cAccumBits</i></td>
<td>Zero or greater.</td>
</tr>
<tr>
<td><i>cAccumRedBits</i></td>
<td>Not used.</td>
</tr>
<tr>
<td><i>cAccumGreenBits</i></td>
<td>Not used.</td>
</tr>
<tr>
<td><i>cAccumBlueBits</i></td>
<td>Not used.</td>
</tr>
<tr>
<td><i>cAccumAlphaBits</i></td>
<td>Not used.</td>
</tr>
<tr>
<td><i>cDepthBits</i></td>
<td>Zero or greater.</td>
</tr>
<tr>
<td><i>cStencilBits</i></td>
<td>Zero or greater.</td>
</tr>
<tr>
<td><i>cAuxBuffers</i></td>
<td>Zero or greater.</td>
</tr>
<tr>
<td><i>iLayerType</i></td>
<td>Specifies one of the following layer type values: <b>PFD_MAIN_PLANE</b>, <b>PFD_OVERLAY_PLANE</b>, <b>PFD_UNDERLAY_PLANE</b></td>
</tr>
<tr>
<td><i>bReserved</i></td>
<td>Not used.</td>
</tr>
<tr>
<td><i>dwLayerMask</i></td>
<td>Not used.</td>
</tr>
<tr>
<td><i>dwVisibleMask</i></td>
<td>Not used.</td>
</tr>
<tr>
<td><i>dwDamageMask</i></td>
<td>Not used.</td>
</tr>
</table>
 

<i></i>


## -returns



If the function succeeds, the return value is a pixel format index (one-based) that is the closest match to the given pixel format descriptor.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



You must ensure that the pixel format matched by the <b>ChoosePixelFormat</b> function satisfies your requirements. For example, if you request a pixel format with a 24-bit RGB color buffer but the device context offers only 8-bit RGB color buffers, the function returns a pixel format with an 8-bit RGB color buffer.


#### Examples

The following code sample shows how to use <b>ChoosePixelFormat</b> to match a specified pixel format.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>PIXELFORMATDESCRIPTOR pfd = { 
    sizeof(PIXELFORMATDESCRIPTOR),  //  size of this pfd  
    1,                     // version number  
    PFD_DRAW_TO_WINDOW |   // support window  
    PFD_SUPPORT_OPENGL |   // support OpenGL  
    PFD_DOUBLEBUFFER,      // double buffered  
    PFD_TYPE_RGBA,         // RGBA type  
    24,                    // 24-bit color depth  
    0, 0, 0, 0, 0, 0,      // color bits ignored  
    0,                     // no alpha buffer  
    0,                     // shift bit ignored  
    0,                     // no accumulation buffer  
    0, 0, 0, 0,            // accum bits ignored  
    32,                    // 32-bit z-buffer      
    0,                     // no stencil buffer  
    0,                     // no auxiliary buffer  
    PFD_MAIN_PLANE,        // main layer  
    0,                     // reserved  
    0, 0, 0                // layer masks ignored  
    }; 
    HDC  hdc;
    int  iPixelFormat; 
 
iPixelFormat = ChoosePixelFormat(hdc, &amp;pfd);</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/9692a30d-c7d4-40c7-a265-72c4ebabd5f2">DescribePixelFormat</a>



<a href="https://msdn.microsoft.com/e9a65f3a-6932-462f-b342-a993d222fae8">GetPixelFormat</a>



<a href="https://msdn.microsoft.com/589a86f1-598d-4175-97fc-27ca0b254935">OpenGL on Windows</a>



<a href="https://msdn.microsoft.com/f8d74078-a7e7-4d95-857a-f51d5d70598e">SetPixelFormat</a>



<a href="https://msdn.microsoft.com/866841db-b137-4f65-856d-b9df5bde12fb">Windows Functions</a>
 

 

