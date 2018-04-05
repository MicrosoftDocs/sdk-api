---
UID: NF:gl.glEnableClientState
title: glEnableClientState function
author: windows-driver-content
description: The glEnableClientState and glDisableClientState functions enable and disable arrays respectively.
old-location: opengl\glenableclientstate.htm
old-project: OpenGL
ms.assetid: 02520f81-0b0d-4774-b1e2-713cf226347f
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GL_COLOR_ARRAY, GL_EDGE_FLAG_ARRAY, GL_INDEX_ARRAY, GL_NORMAL_ARRAY, GL_TEXTURE_COORD_ARRAY, GL_VERTEX_ARRAY, gl/glEnableClientState, glEnableClientState, glEnableClientState function [OpenGL], opengl.glenableclientstate
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
-	Opengl32.dll
api_name:
-	glEnableClientState
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glEnableClientState function


## -description


The <b>glEnableClientState</b> and <a href="https://msdn.microsoft.com/b3316519-00ed-45f8-9c4b-2e04c483751e">glDisableClientState</a> functions enable and disable arrays respectively.


## -parameters




### -param array

A symbolic constant for the array you want to enable or disable. This parameter can assume one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GL_COLOR_ARRAY"></a><a id="gl_color_array"></a><dl>
<dt><b>GL_COLOR_ARRAY</b></dt>
</dl>
</td>
<td width="60%">
If enabled, use color arrays with calls to <a href="https://msdn.microsoft.com/2c4d76bb-e4c9-4baa-a190-66298b8a4335">glArrayElement</a>, <a href="https://msdn.microsoft.com/fb433294-106e-48d5-ad49-4434934fe072">glDrawElements</a>, or <a href="https://msdn.microsoft.com/6ebd467b-5a63-43e4-b3fd-242c704d7d13">glDrawArrays</a>.

See also <a href="https://msdn.microsoft.com/4d9d05fb-691d-4b71-b079-c42dc7103055">glColorPointer</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_EDGE_FLAG_ARRAY"></a><a id="gl_edge_flag_array"></a><dl>
<dt><b>GL_EDGE_FLAG_ARRAY</b></dt>
</dl>
</td>
<td width="60%">
If enabled, use edge flag arrays with calls to <a href="https://msdn.microsoft.com/2c4d76bb-e4c9-4baa-a190-66298b8a4335">glArrayElement</a>, <a href="https://msdn.microsoft.com/fb433294-106e-48d5-ad49-4434934fe072">glDrawElements</a>, or <a href="https://msdn.microsoft.com/6ebd467b-5a63-43e4-b3fd-242c704d7d13">glDrawArrays</a>.

See also <a href="https://msdn.microsoft.com/e0e7e442-533d-4c41-addd-a215ce0b1c56">glEdgeFlagPointer</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_INDEX_ARRAY"></a><a id="gl_index_array"></a><dl>
<dt><b>GL_INDEX_ARRAY</b></dt>
</dl>
</td>
<td width="60%">
If enabled, use index arrays with calls to <a href="https://msdn.microsoft.com/2c4d76bb-e4c9-4baa-a190-66298b8a4335">glArrayElement</a>, <a href="https://msdn.microsoft.com/fb433294-106e-48d5-ad49-4434934fe072">glDrawElements</a>, or <a href="https://msdn.microsoft.com/6ebd467b-5a63-43e4-b3fd-242c704d7d13">glDrawArrays</a>.

See also <a href="https://msdn.microsoft.com/b435d950-1f87-4041-93e4-f1f8786cabdb">glIndexPointer</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_NORMAL_ARRAY"></a><a id="gl_normal_array"></a><dl>
<dt><b>GL_NORMAL_ARRAY</b></dt>
</dl>
</td>
<td width="60%">
If enabled, use normal arrays with calls to <a href="https://msdn.microsoft.com/2c4d76bb-e4c9-4baa-a190-66298b8a4335">glArrayElement</a>, <a href="https://msdn.microsoft.com/fb433294-106e-48d5-ad49-4434934fe072">glDrawElements</a>, or <a href="https://msdn.microsoft.com/6ebd467b-5a63-43e4-b3fd-242c704d7d13">glDrawArrays</a>.

See also <a href="https://msdn.microsoft.com/6ffb0522-87cc-4be1-a5b1-f6fd30e04b43">glNormalPointer</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_TEXTURE_COORD_ARRAY"></a><a id="gl_texture_coord_array"></a><dl>
<dt><b>GL_TEXTURE_COORD_ARRAY</b></dt>
</dl>
</td>
<td width="60%">
If enabled, use texture coordinate arrays with calls to <a href="https://msdn.microsoft.com/2c4d76bb-e4c9-4baa-a190-66298b8a4335">glArrayElement</a>, <a href="https://msdn.microsoft.com/fb433294-106e-48d5-ad49-4434934fe072">glDrawElements</a>, or <a href="https://msdn.microsoft.com/6ebd467b-5a63-43e4-b3fd-242c704d7d13">glDrawArrays</a>.

See also <a href="https://msdn.microsoft.com/c3640a1b-ccc7-4f1a-94a5-a164f7377dbc">glTexCoordPointer</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_VERTEX_ARRAY"></a><a id="gl_vertex_array"></a><dl>
<dt><b>GL_VERTEX_ARRAY</b></dt>
</dl>
</td>
<td width="60%">
If enabled, use vertex arrays with calls to <a href="https://msdn.microsoft.com/2c4d76bb-e4c9-4baa-a190-66298b8a4335">glArrayElement</a>, <a href="https://msdn.microsoft.com/fb433294-106e-48d5-ad49-4434934fe072">glDrawElements</a>, or <a href="https://msdn.microsoft.com/6ebd467b-5a63-43e4-b3fd-242c704d7d13">glDrawArrays</a>.

See also <a href="https://msdn.microsoft.com/e5f97fdc-9448-4389-8533-3855a3213feb">glVertexPointer</a>.

</td>
</tr>
</table>
 


## -returns



This function does not return a value.




## -remarks



The <b>glEnableClientState</b> and <b>glDisableClientState</b> functions enable and disable various individual arrays. Use <a href="https://msdn.microsoft.com/18df5a6f-dc21-434d-a2e8-2c58597df037">glIsEnabled</a> or <a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> to determine the current setting of any capability.

Calling <b>glEnableClientState</b> and <b>glDisableClientState</b> between calls to <a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a> and the corresponding call to <a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a> can cause an error. If no error is generated, the behavior is undefined.

<div class="alert"><b>Note</b>  The <b>glEnableClientState</b> and <b>glDisableClientState</b> functions are only available in OpenGL version 1.1 or later.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/2c4d76bb-e4c9-4baa-a190-66298b8a4335">glArrayElement</a>



<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/4d9d05fb-691d-4b71-b079-c42dc7103055">glColorPointer</a>



<a href="https://msdn.microsoft.com/b3316519-00ed-45f8-9c4b-2e04c483751e">glDisableClientState</a>



<a href="https://msdn.microsoft.com/6ebd467b-5a63-43e4-b3fd-242c704d7d13">glDrawArrays</a>



<a href="https://msdn.microsoft.com/fb433294-106e-48d5-ad49-4434934fe072">glDrawElements</a>



<a href="https://msdn.microsoft.com/e0e7e442-533d-4c41-addd-a215ce0b1c56">glEdgeFlagPointer</a>



<a href="https://msdn.microsoft.com/cd4590dd-ae41-47c9-9861-10d72318840f">glEnable</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/6f85c508-9335-4474-8cc5-e67c7421a8e4">glGetPointerv</a>



<a href="https://msdn.microsoft.com/b435d950-1f87-4041-93e4-f1f8786cabdb">glIndexPointer</a>



<a href="https://msdn.microsoft.com/f1133949-d755-43e3-bf29-8e4c7fb17980">glInterleavedArrays</a>



<a href="https://msdn.microsoft.com/6ffb0522-87cc-4be1-a5b1-f6fd30e04b43">glNormalPointer</a>



<a href="https://msdn.microsoft.com/c3640a1b-ccc7-4f1a-94a5-a164f7377dbc">glTexCoordPointer</a>



<a href="https://msdn.microsoft.com/e5f97fdc-9448-4389-8533-3855a3213feb">glVertexPointer</a>
 

 

