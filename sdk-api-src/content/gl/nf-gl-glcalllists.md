---
UID: NF:gl.glCallLists
title: glCallLists function
author: windows-driver-content
description: The glCallLists function executes a list of display lists.
old-location: opengl\glcalllists.htm
old-project: OpenGL
ms.assetid: 7c0a00df-91ee-44ad-9e02-97c1b078e87f
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GL_2_BYTES, GL_3_BYTES, GL_4_BYTES, GL_BYTE, GL_FLOAT, GL_INT, GL_SHORT, GL_UNSIGNED_BYTE, GL_UNSIGNED_INT, GL_UNSIGNED_SHORT, _ogl_glCallLists, gl/glCallLists, glCallLists, glCallLists function [OpenGL], opengl.glcalllists
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: gl.h
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	opengl32.dll
api_name:
-	glCallLists
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glCallLists function


## -description


The <b>glCallLists</b> function executes a list of display lists.


## -parameters




### -param n

The number of display lists to be executed.


### -param type

The type of values in <i>lists</i>. The following symbolic constants are accepted.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GL_BYTE"></a><a id="gl_byte"></a><dl>
<dt><b>GL_BYTE</b></dt>
</dl>
</td>
<td width="60%">
The <i>lists</i> parameter is treated as an array of signed bytes, each in the range -128 through 127.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_UNSIGNED_BYTE"></a><a id="gl_unsigned_byte"></a><dl>
<dt><b>GL_UNSIGNED_BYTE</b></dt>
</dl>
</td>
<td width="60%">
The <i>lists</i> parameter is treated as an array of unsigned bytes, each in the range 0 through 255.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_SHORT"></a><a id="gl_short"></a><dl>
<dt><b>GL_SHORT</b></dt>
</dl>
</td>
<td width="60%">
The <i>lists</i> parameter is treated as an array of signed 2-byte integers, each in the range -32768 through 32767.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_UNSIGNED_SHORT"></a><a id="gl_unsigned_short"></a><dl>
<dt><b>GL_UNSIGNED_SHORT</b></dt>
</dl>
</td>
<td width="60%">
The <i>lists</i> parameter is treated as an array of unsigned 2-byte integers, each in the range 0 through 65535.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_INT"></a><a id="gl_int"></a><dl>
<dt><b>GL_INT</b></dt>
</dl>
</td>
<td width="60%">
The <i>lists</i> parameter is treated as an array of signed 4-byte integers.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_UNSIGNED_INT"></a><a id="gl_unsigned_int"></a><dl>
<dt><b>GL_UNSIGNED_INT</b></dt>
</dl>
</td>
<td width="60%">
The <i>lists</i> parameter is treated as an array of unsigned 4-byte integers.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_FLOAT"></a><a id="gl_float"></a><dl>
<dt><b>GL_FLOAT</b></dt>
</dl>
</td>
<td width="60%">
The <i>lists</i> parameter is treated as an array of 4-byte, floating-point values.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_2_BYTES"></a><a id="gl_2_bytes"></a><dl>
<dt><b>GL_2_BYTES</b></dt>
</dl>
</td>
<td width="60%">
The <i>lists</i> parameter is treated as an array of unsigned bytes. Each pair of bytes specifies a single display-list name. The value of the pair is computed as 256 times the unsigned value of the first byte plus the unsigned value of the second byte.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_3_BYTES"></a><a id="gl_3_bytes"></a><dl>
<dt><b>GL_3_BYTES</b></dt>
</dl>
</td>
<td width="60%">
The <i>lists</i> parameter is treated as an array of unsigned bytes. Each triplet of bytes specifies a single display list name. The value of the triplet is computed as 65536 times the unsigned value of the first byte, plus 256 times the unsigned value of the second byte, plus the unsigned value of the third byte.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_4_BYTES"></a><a id="gl_4_bytes"></a><dl>
<dt><b>GL_4_BYTES</b></dt>
</dl>
</td>
<td width="60%">
The <i>lists</i> parameter is treated as an array of unsigned bytes. Each quadruplet of bytes specifies a single display list name. The value of the quadruplet is computed as 16777216 times the unsigned value of the first byte, plus 65536 times the unsigned value of the second byte, plus 256 times the unsigned value of the third byte, plus the unsigned value of the fourth byte.

</td>
</tr>
</table>
 


### -param lists

The address of an array of name offsets in the display list. The pointer type is void because the offsets can be bytes, shorts, ints, or floats, depending on the value of <i>type</i>.


## -returns



This function does not return a value.




## -remarks



The <b>glCallLists</b> function causes each display list in the list of names passed as <i>lists</i> to be executed. As a result, the functions saved in each display list are executed in order, just as if they were called without using a display list. Names of display lists that have not been defined are ignored.

The <b>glCallLists</b> function provides an efficient means for executing display lists. The <i>n</i> parameter specifies the number of lists with various name formats (specified by the <i>type</i> parameter) <b>glCallLists</b> executes.

The list of display list names is not null-terminated. Rather, <i>n</i> specifies how many names are to be taken from <i>lists</i>.

The <a href="https://msdn.microsoft.com/df82f699-b2af-471a-83f3-5620857ba45d">glListBase</a> function makes an additional level of indirection available. The <b>glListBase</b> function specifies an unsigned offset that is added to each display list name specified in <i>lists</i> before that display list is executed.

The <b>glCallLists</b> function can appear inside a display list. To avoid the possibility of infinite recursion resulting from display lists calling one another, a limit is placed on the nesting level of display lists during display list execution. This limit must be at least 64, and it depends on the implementation.

The OpenGL state is not saved and restored across a call to <b>glCallLists</b>. Thus, changes made to the OpenGL state during the execution of the display lists remain after execution is completed. Use <a href="https://msdn.microsoft.com/3c7b93cc-2112-4771-b422-a244821447e5">glPushAttrib</a>, <a href="https://msdn.microsoft.com/6a11392c-d5af-47bb-a66a-691730a58260">glPopAttrib</a>, <a href="https://msdn.microsoft.com/97d8e644-50bb-4130-b6b7-d87df4468e73">glPushMatrix</a>, and <a href="https://msdn.microsoft.com/7b4fc26e-36c8-4252-aba7-2e8ec6b34f91">glPopMatrix</a> to preserve the OpenGL state across <b>glCallLists</b> calls.

You can execute display lists between a call to <a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>
 and the corresponding call to <a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>, as long as the display list includes only functions that are allowed in this interval.

The following functions retrieve information related to the <b>glCallLists</b> function:


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_LIST_BASE

<b>glGet</b> with argument GL_MAX_LIST_NESTING


<a href="https://msdn.microsoft.com/86ef3684-8047-4ee4-befd-ec26bcd036c3">glIsList</a>





## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/9373d32e-b11e-4a80-8713-da2c1d8d9368">glCallList</a>



<a href="https://msdn.microsoft.com/979ab352-99db-4822-922c-a1813b9fcfce">glDeleteLists</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/07a97e89-1fbe-4405-b1b0-c4c47b098633">glGenLists</a>



<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a>



<a href="https://msdn.microsoft.com/86ef3684-8047-4ee4-befd-ec26bcd036c3">glIsList</a>



<a href="https://msdn.microsoft.com/df82f699-b2af-471a-83f3-5620857ba45d">glListBase</a>



<a href="https://msdn.microsoft.com/9c6556d4-855f-4cba-94cc-27b5f1e4607a">glNewList</a>



<a href="https://msdn.microsoft.com/6a11392c-d5af-47bb-a66a-691730a58260">glPopAttrib</a>



<a href="https://msdn.microsoft.com/7b4fc26e-36c8-4252-aba7-2e8ec6b34f91">glPopMatrix</a>



<a href="https://msdn.microsoft.com/3c7b93cc-2112-4771-b422-a244821447e5">glPushAttrib</a>



<a href="https://msdn.microsoft.com/97d8e644-50bb-4130-b6b7-d87df4468e73">glPushMatrix</a>
 

 

