---
UID: NF:gl.glPushAttrib
title: glPushAttrib function
author: windows-driver-content
description: Pushes the attribute stack.
old-location: opengl\glpushattrib.htm
old-project: OpenGL
ms.assetid: 3c7b93cc-2112-4771-b422-a244821447e5
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: gl/glPushAttrib, glPushAttrib, glPushAttrib function [OpenGL], opengl.glpushattrib
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
-	glPushAttrib
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glPushAttrib function


## -description


Pushes the attribute stack.


## -parameters




### -param mask

A mask that indicates which attributes to save. The symbolic mask constants and their associated OpenGL state are as follows (the indented paragraphs list which attributes are saved):





#### GL_ACCUM_BUFFER_BIT

Accumulation buffer clear value



#### GL_COLOR_BUFFER_BIT

GL_ALPHA_TEST enable bit

 
Alpha test function and reference value

 

GL_BLEND enable bit

 

Blending source and destination functions

 

GL_DITHER enable bit

 

GL_DRAW_BUFFER setting

 

GL_LOGIC_OP enable bit

 

Logic op function

 

Color-mode and index-mode clear values

 

Color-mode and index-mode writemasks



#### GL_CURRENT_BIT

Current RGBA color

 
Current color index

 

Current normal vector

 

Current texture coordinates

 

Current raster position 

GL_CURRENT_RASTER_POSITION_VALID flag

 

RGBA color associated with current raster position

 

Color index associated with current raster position

 

Texture coordinates associated with current raster position

 

GL_EDGE_FLAG flag




#### GL_DEPTH_BUFFER_BIT

GL_DEPTH_TEST enable bit

 
Depth buffer test function

 

Depth buffer clear value

 

GL_DEPTH_WRITEMASK enable bit



#### GL_ENABLE_BIT

GL_ALPHA_TEST flag

 
GL_AUTO_NORMAL flag

 

GL_BLEND flag

 

Enable bits for the user-definable clipping planes

 

GL_COLOR_MATERIAL

 

GL_CULL_FACE flag

 

GL_DEPTH_TEST flag

 

GL_DITHER flag

 

GL_FOG flag

 

GL_LIGHT<i>i</i> where 0 &lt;= <i>i</i> &lt; GL_MAX_LIGHTS

GL_LIGHTING flag

 

GL_LINE_SMOOTH flag

 

GL_LINE_STIPPLE flag

 

GL_COLOR_LOGIC_OP flag

 

GL_INDEX_LOGIC_OP flag

 

GL_MAP1_x where x is a map type

 

GL_MAP2_x where x is a map type

 

GL_NORMALIZE flag

 

GL_POINT_SMOOTH flag

 

GL_POLYGON_OFFSET_LINE flag

 

GL_POLYGON_OFFSET_FILL flag

 

GL_POLYGON_OFFSET_POINT flag

 

GL_POLYGON_SMOOTH flag

 

GL_POLYGON_STIPPLE flag

 

GL_SCISSOR_TEST flag

 

GL_STENCIL_TEST flag

 

GL_TEXTURE_1D flag

 

GL_TEXTURE_2D flag

 

Flags GL_TEXTURE_GEN_x where x is S, T, R, or Q



#### GL_EVAL_BIT

GL_MAP1_x enable bits, where x is a map type

 
GL_MAP2_x enable bits, where x is a map type

 

1-D grid endpoints and divisions

 

2-D grid endpoints and divisions

 

GL_AUTO_NORMAL enable bit



#### GL_FOG_BIT

GL_FOG enable flag

 
Fog color

 

Fog density

 

Linear fog start

 

Linear fog end

 

Fog index

 

GL_FOG_MODE value



#### GL_HINT_BIT

GL_PERSPECTIVE_CORRECTION_HINT setting

 
GL_POINT_SMOOTH_HINT setting

 

GL_LINE_SMOOTH_HINT setting

 

GL_POLYGON_SMOOTH_HINT setting

 

GL_FOG_HINT setting



#### GL_LIGHTING_BIT

GL_COLOR_MATERIAL enable bit

 
GL_COLOR_MATERIAL_FACE value

 

Color material parameters that are tracking the current color

 

Ambient scene color

 

GL_LIGHT_MODEL_LOCAL_VIEWER value

 

GL_LIGHT_MODEL_TWO_SIDE setting

 

GL_LIGHTING enable bit

 

Enable bit for each light

 

Ambient, diffuse, and specular intensity for each light

 

Direction, position, exponent, and cutoff angle for each light

 

Constant, linear, and quadratic attenuation factors for each light

 

Ambient, diffuse, specular, and emissive color for each material

 

Ambient, diffuse, and specular color indexes for each material

 

Specular exponent for each material 

GL_SHADE_MODEL setting 




#### GL_LINE_BIT

GL_LINE_SMOOTH flag

 
GL_LINE_STIPPLE enable bit

 

Line stipple pattern and repeat counter

 

Line width



#### GL_LIST_BIT

GL_LIST_BASE setting



#### GL_PIXEL_MODE_BIT

GL_RED_BIAS and GL_RED_SCALE settings

 
GL_GREEN_BIAS and GL_GREEN_SCALE values

 

GL_BLUE_BIAS and GL_BLUE_SCALE

 

GL_ALPHA_BIAS and GL_ALPHA_SCALE

 

GL_DEPTH_BIAS and GL_DEPTH_SCALE

 

GL_INDEX_OFFSET and GL_INDEX_SHIFT values

 

GL_MAP_COLOR and GL_MAP_STENCIL flags

 

GL_ZOOM_X and GL_ZOOM_Y factors

 

GL_READ_BUFFER setting



#### GL_POINT_BIT

GL_POINT_SMOOTH flag

 
Point size



#### GL_POLYGON_BIT

GL_CULL_FACE enable bit

 
GL_CULL_FACE_MODE value

 

GL_FRONT_FACE indicator

 

GL_POLYGON_MODE setting

 

GL_POLYGON_SMOOTH flag

 

GL_POLYGON_STIPPLE enable bit

 

GL_POLYGON_OFFSET_FILL flag

 

GL_POLYGON_OFFSET_LINE flag

 

GL_POLYGON_OFFSET_POINT flag

 

GL_POLYGON_OFFSET_FACTOR

 

GL_POLYGON_OFFSET_UNITS



#### GL_POLYGON_STIPPLE_BIT

Polygon stipple image 



#### GL_SCISSOR_BIT

GL_SCISSOR_TEST flag

 
Scissor box 




#### GL_STENCIL_BUFFER_BIT

GL_STENCIL_TEST enable bit

 
Stencil function and reference value

 

Stencil value mask

 

Stencil fail, pass, and depth buffer pass actions

 

Stencil buffer clear value

 

Stencil buffer writemask



#### GL_TEXTURE_BIT

Enable bits for the four texture coordinates

 
Border color for each texture image

 

Minification function for each texture image

 

Magnification function for each texture image

 

Texture coordinates and wrap mode for each texture image

 

Color and mode for each texture environment

 

Enable bits GL_TEXTURE_GEN_<i>x</i>; <i>x</i> is S, T, R, and Q

 

GL_TEXTURE_GEN_MODE setting for S, T, R, and Q

 

glTexGen plane equations for S, T, R, and Q 

 



#### GL_TRANSFORM_BIT

Coefficients of the six clipping planes

 
Enable bits for the user-definable clipping planes

 

GL_MATRIX_MODE value

 

GL_NORMALIZE flag



#### GL_VIEWPORT_BIT

Depth range (near and far)

 
Viewport origin and extent



## -returns



This function does not return a value.




## -remarks



The <b>glPushAttrib</b> function takes one argument, a mask that indicates which groups of state variables to save on the attribute stack. Symbolic constants are used to set bits in the mask. The mask parameter is typically constructed by applying the logical <b>OR</b> operation to several of these constants. You can use the special mask GL_ALL_ATTRIB_BITS to save all stackable states.



The <a href="https://msdn.microsoft.com/6a11392c-d5af-47bb-a66a-691730a58260">glPopAttrib</a> function restores the values of the state variables saved with the last <b>glPushAttrib</b> command. Those not saved are left unchanged.



It is an error to push attributes onto a full stack, or to pop attributes off an empty stack. In either case, the error flag is set and no other change is made to the OpenGL state.



Initially, the attribute stack is empty.



Not all values for the OpenGL state can be saved on the attribute stack. For example, you cannot save pixel pack and unpack state, render mode state, and select and feedback state.



The depth of the attribute stack depends on the implementation, but it must be at least 16.



The following functions retrieve information related to <b>glPushAttrib</b> and <a href="https://msdn.microsoft.com/6a11392c-d5af-47bb-a66a-691730a58260">glPopAttrib</a>:


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
 

 

