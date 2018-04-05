---
UID: NF:gl.glPopAttrib
title: glPopAttrib function
author: windows-driver-content
description: Pops the attribute stack.
old-location: opengl\glpopattrib.htm
old-project: OpenGL
ms.assetid: 6a11392c-d5af-47bb-a66a-691730a58260
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: gl/glPopAttrib, glPopAttrib, glPopAttrib function [OpenGL], opengl.glpopattrib
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
-	glPopAttrib
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glPopAttrib function


## -description


Pops the attribute stack.


## -parameters






## -returns



This function does not return a value.




## -remarks



The <a href="https://msdn.microsoft.com/3c7b93cc-2112-4771-b422-a244821447e5">glPushAttrib</a> function takes one argument, a mask that indicates which groups of state variables to save on the attribute stack. Symbolic constants are used to set bits in the mask. The mask parameter is typically constructed by <b>OR</b>ing several of these constants together. The special mask GL_ALL_ATTRIB_BITS can be used to save all stackable states.



The <b>glPopAttrib</b> function restores the values of the state variables saved with the last <a href="https://msdn.microsoft.com/3c7b93cc-2112-4771-b422-a244821447e5">glPushAttrib</a> command. Those not saved are left unchanged.



It is an error to push attributes onto a full stack, or to pop attributes off an empty stack. In either case, the error flag is set and no other change is made to the OpenGL state.



Initially, the attribute stack is empty.



Not all values for the OpenGL state can be saved on the attribute stack. For example, pixel pack and unpack state, render mode state, and select and feedback state cannot be saved.



The depth of the attribute stack depends on the implementation, but it must be at least 16.



The following functions retrieve information related to <a href="https://msdn.microsoft.com/3c7b93cc-2112-4771-b422-a244821447e5">glPushAttrib</a> and <b>glPopAttrib</b>:


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_ATTRIB_STACK_DEPTH 




<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_MAX_ATTRIB_STACK_DEPTH 






## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a>



<a href="https://msdn.microsoft.com/8ff5ee0a-95c1-4321-8aa8-3d9d144d1ef6">glGetClipPlane</a>



<a href="https://msdn.microsoft.com/18f0368f-054f-4b84-8397-3f9ee4aa07fa">glGetError</a>



<a href="https://msdn.microsoft.com/a2d41afd-78d9-4c59-92d5-3334d14a42f3">glGetLight</a>



<a href="https://msdn.microsoft.com/6476ccd2-a3d2-463d-9e6d-da6133dd569c">glGetMap</a>



<a href="https://msdn.microsoft.com/79409f4e-1e39-4fca-adc8-d48253853ce3">glGetMaterial</a>



<a href="https://msdn.microsoft.com/31f91d40-b52f-4231-a7bf-e2a387be5191">glGetPixelMap</a>



<a href="https://msdn.microsoft.com/95c1ebfa-8465-4bc1-b3f5-eed696a83816">glGetPolygonStipple</a>



<a href="https://msdn.microsoft.com/768e6ec2-3f00-44e6-b3cb-de0f06d6a73d">glGetString</a>



<a href="https://msdn.microsoft.com/9dd0d7ac-f3e0-43a8-8458-2664965cce7c">glGetTexEnv</a>



<a href="https://msdn.microsoft.com/92510f08-1a01-4883-9dd7-1c39f4cc9b6a">glGetTexGen</a>



<a href="https://msdn.microsoft.com/d7235df4-2dd8-4537-aadd-284c130a3f99">glGetTexImage</a>



<a href="https://msdn.microsoft.com/04aa02ef-5c9a-4b8a-a77f-fd5985c76fe2">glGetTexLevelParameter</a>



<a href="https://msdn.microsoft.com/e95bec46-cfb5-4443-86fc-7a2721918ea9">glGetTexParameter</a>



<a href="https://msdn.microsoft.com/18df5a6f-dc21-434d-a2e8-2c58597df037">glIsEnabled</a>
 

 

