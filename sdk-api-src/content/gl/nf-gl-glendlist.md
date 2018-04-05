---
UID: NF:gl.glEndList
title: glEndList function
author: windows-driver-content
description: The glNewList and glEndList functions create or replace a display list.
old-location: opengl\glendlist.htm
old-project: OpenGL
ms.assetid: dd749932-7b3c-47e5-8d91-90d272a7dc41
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: gl/glEndList, glEndList, glEndList function [OpenGL], opengl.glendlist
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
-	glEndList
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glEndList function


## -description


The <a href="https://msdn.microsoft.com/9c6556d4-855f-4cba-94cc-27b5f1e4607a">glNewList</a> and <b>glEndList</b> functions create or replace a display list.


## -parameters






## -returns



This function does not return a value.




## -remarks



Display lists are groups of OpenGL commands that have been stored for subsequent execution. The display lists are created with <a href="https://msdn.microsoft.com/9c6556d4-855f-4cba-94cc-27b5f1e4607a">glNewList</a>. All subsequent commands are placed in the display list, in the order issued, until <b>glEndList</b> is called.

The <a href="https://msdn.microsoft.com/9c6556d4-855f-4cba-94cc-27b5f1e4607a">glNewList</a> function has two parameters. The first parameter, <i>list</i>, is a positive integer that becomes the unique name for the display list. Names can be created and reserved with <a href="https://msdn.microsoft.com/07a97e89-1fbe-4405-b1b0-c4c47b098633">glGenLists</a> and tested for uniqueness with <a href="https://msdn.microsoft.com/86ef3684-8047-4ee4-befd-ec26bcd036c3">glIsList</a>. The second parameter, <i>mode</i>, is a symbolic constant that can assume one of the two preceding values.

Certain commands are not compiled into the display list, but are executed immediately, regardless of the display list mode. These commands are <a href="https://msdn.microsoft.com/4d9d05fb-691d-4b71-b079-c42dc7103055">glColorPointer</a>, <a href="https://msdn.microsoft.com/979ab352-99db-4822-922c-a1813b9fcfce">glDeleteLists</a>, <a href="https://msdn.microsoft.com/b3316519-00ed-45f8-9c4b-2e04c483751e">glDisableClientState</a>, 
<a href="https://msdn.microsoft.com/e0e7e442-533d-4c41-addd-a215ce0b1c56">glEdgeFlagPointer</a>, 
<a href="https://msdn.microsoft.com/02520f81-0b0d-4774-b1e2-713cf226347f">glEnableClientState</a>, 
<a href="https://msdn.microsoft.com/fe3773a7-c264-4d49-8f90-1f2319f9af4f">glFeedbackBuffer</a>, 
<a href="https://msdn.microsoft.com/1dcb4767-02ea-41d8-bf1f-d61d20873d4f">glFinish</a>, 
<a href="https://msdn.microsoft.com/7544b724-472f-4055-8f1c-64ddb58caaf3">glFlush</a>, 
<a href="https://msdn.microsoft.com/07a97e89-1fbe-4405-b1b0-c4c47b098633">glGenLists</a>, 
<a href="https://msdn.microsoft.com/b435d950-1f87-4041-93e4-f1f8786cabdb">glIndexPointer</a>, <a href="https://msdn.microsoft.com/f1133949-d755-43e3-bf29-8e4c7fb17980">glInterleavedArrays</a>, 
<a href="https://msdn.microsoft.com/18df5a6f-dc21-434d-a2e8-2c58597df037">glIsEnabled</a>, 
<a href="https://msdn.microsoft.com/86ef3684-8047-4ee4-befd-ec26bcd036c3">glIsList</a>, 
<a href="https://msdn.microsoft.com/6ffb0522-87cc-4be1-a5b1-f6fd30e04b43">glNormalPointer</a>, <a href="https://msdn.microsoft.com/030a3955-35bf-4862-9691-54b0c24514e8">glPopClientAttrib</a>, <a href="https://msdn.microsoft.com/c12255eb-8802-4602-b1fa-ab157201ae5c">glPixelStore</a>, 
<a href="https://msdn.microsoft.com/69f28af6-1023-4546-95ff-169525c23b07">glPushClientAttrib</a>, 
<a href="https://msdn.microsoft.com/41fbad5c-b8ca-456d-bbfc-b48c176e15b0">glReadPixels</a>, 
<a href="https://msdn.microsoft.com/bcbc3bba-c552-425b-8284-6cadff0c9f56">glRenderMode</a>, 
<a href="https://msdn.microsoft.com/b5c64364-1f47-4281-96b5-95c3f5c8e753">glSelectBuffer</a>, <a href="https://msdn.microsoft.com/c3640a1b-ccc7-4f1a-94a5-a164f7377dbc">glTexCoordPointer</a>, 
<a href="https://msdn.microsoft.com/e5f97fdc-9448-4389-8533-3855a3213feb">glVertexPointer</a>, and all of the <a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> routines.

Similarly, <a href="https://msdn.microsoft.com/e8b9c692-5239-47de-86eb-80c247c60e1d">glTexImage2D</a> and <a href="https://msdn.microsoft.com/4f537b89-2ea2-4e2e-8c57-c372bf53f12c">glTexImage1D</a> are executed immediately and not compiled into the display list when their first argument is GL_PROXY_TEXTURE_2D or GL_PROXY_TEXTURE_1D, respectively.

When the <b>glEndList</b> function is encountered, the display list definition is completed by associating the list with the unique name <i>list</i> (specified in the <a href="https://msdn.microsoft.com/9c6556d4-855f-4cba-94cc-27b5f1e4607a">glNewList</a> command). If a display list with name <i>list</i> already exists, it is replaced only when <b>glEndList</b> is called.

The <a href="https://msdn.microsoft.com/9373d32e-b11e-4a80-8713-da2c1d8d9368">glCallList</a> and <a href="https://msdn.microsoft.com/7c0a00df-91ee-44ad-9e02-97c1b078e87f">glCallLists</a> functions can be entered into display lists. The commands in the display list or lists executed by <b>glCallList</b> or <b>glCallLists</b> are not included in the display list being created, even if the list creation mode is GL_COMPILE_AND_EXECUTE.

The following function retrieves information related to <a href="https://msdn.microsoft.com/9c6556d4-855f-4cba-94cc-27b5f1e4607a">glNewList</a>:


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_MATRIX_MODE




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/9373d32e-b11e-4a80-8713-da2c1d8d9368">glCallList</a>



<a href="https://msdn.microsoft.com/7c0a00df-91ee-44ad-9e02-97c1b078e87f">glCallLists</a>



<a href="https://msdn.microsoft.com/979ab352-99db-4822-922c-a1813b9fcfce">glDeleteLists</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/07a97e89-1fbe-4405-b1b0-c4c47b098633">glGenLists</a>



<a href="https://msdn.microsoft.com/86ef3684-8047-4ee4-befd-ec26bcd036c3">glIsList</a>



<a href="https://msdn.microsoft.com/9c6556d4-855f-4cba-94cc-27b5f1e4607a">glNewList</a>
 

 

