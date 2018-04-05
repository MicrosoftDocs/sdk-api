---
UID: NF:gl.glPopClientAttrib
title: glPopClientAttrib function
author: windows-driver-content
description: The glPushClientAttrib and glPopClientAttrib functions save and restore groups of client-state variables on the client-attribute stack.
old-location: opengl\glpopclientattrib.htm
old-project: OpenGL
ms.assetid: 030a3955-35bf-4862-9691-54b0c24514e8
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: gl/glPopClientAttrib, glPopClientAttrib, glPopClientAttrib function [OpenGL], opengl.glpopclientattrib
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
-	glPopClientAttrib
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glPopClientAttrib function


## -description


The <a href="https://msdn.microsoft.com/69f28af6-1023-4546-95ff-169525c23b07">glPushClientAttrib</a> and <b>glPopClientAttrib</b> functions save and restore groups of client-state variables on the client-attribute stack.




## -parameters






## -returns



This function does not return a value.




## -remarks



The <b>glPushClientAttrib</b> function uses its mask parameter to determine which groups of client-state variables are saved on the client-attribute stack. You can use the bitwise OR operator to join together accepted symbolic constants to set bits and construct a mask. 

The <b>glPopClientAttrib</b> function restores the values of the client-state variables last saved with <b>glPushclientAttrib</b>. Client-state variables not previously saved are left unchanged. Pushing attributes onto a full client-attribute stack or popping attributes off an empty stack sets an error flag and no other change is made to the OpenGL state. By default the client attribute stack is empty.

Some OpenGL client-state values cannot be saved on the client-attribute stack. For example, you cannot save the select or feedback states on the client-attribute stack. The depth of the client-attribute stack is at least 16.

The <b>glPushclientAttrib</b> and <b>glPopClientAttrib</b> functions are not compiled into display lists, but are executed immediately.

The <b>glPushClientAttrib</b> and <b>glPopClientAttrib</b> functions can only push and pop pixel storage modes and vertex array client states. You must use <a href="https://msdn.microsoft.com/3c7b93cc-2112-4771-b422-a244821447e5">glPushAttrib</a> and <a href="https://msdn.microsoft.com/6a11392c-d5af-47bb-a66a-691730a58260">glPopAttrib</a> to push and pop states that are kept on the server.

<div class="alert"><b>Note</b>  The <b>glPushClientAttrib</b> and <b>glPopClientAttrib</b> functions are only available in OpenGL version 1.1 or later.
</div>
<div> </div>
The following functions retrieve information related to <b>glPushClientAttrib</b> and <b>glPopClientAttrib</b>:


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_CLIENT_ATTRIB_STACK_DEPTH


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_MAX_CLIENT_ATTRIB_STACK_DEPTH




## -see-also




<a href="https://msdn.microsoft.com/4d9d05fb-691d-4b71-b079-c42dc7103055">glColorPointer</a>



<a href="https://msdn.microsoft.com/b3316519-00ed-45f8-9c4b-2e04c483751e">glDisableClientState</a>



<a href="https://msdn.microsoft.com/e0e7e442-533d-4c41-addd-a215ce0b1c56">glEdgeFlagPointer</a>



<a href="https://msdn.microsoft.com/02520f81-0b0d-4774-b1e2-713cf226347f">glEnableClientState</a>



<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a>



<a href="https://msdn.microsoft.com/18f0368f-054f-4b84-8397-3f9ee4aa07fa">glGetError</a>



<a href="https://msdn.microsoft.com/b435d950-1f87-4041-93e4-f1f8786cabdb">glIndexPointer</a>



<a href="https://msdn.microsoft.com/9c6556d4-855f-4cba-94cc-27b5f1e4607a">glNewList</a>



<a href="https://msdn.microsoft.com/6ffb0522-87cc-4be1-a5b1-f6fd30e04b43">glNormalPointer</a>



<a href="https://msdn.microsoft.com/c12255eb-8802-4602-b1fa-ab157201ae5c">glPixelStore</a>



<a href="https://msdn.microsoft.com/3c7b93cc-2112-4771-b422-a244821447e5">glPushAttrib</a>



<a href="https://msdn.microsoft.com/c3640a1b-ccc7-4f1a-94a5-a164f7377dbc">glTexCoordPointer</a>



<a href="https://msdn.microsoft.com/e5f97fdc-9448-4389-8533-3855a3213feb">glVertexPointer</a>
 

 

