---
UID: NF:gl.glDisable
title: glDisable function
author: windows-driver-content
description: The glEnable and glDisable functions enable or disable OpenGL capabilities.
old-location: opengl\gldisable.htm
old-project: OpenGL
ms.assetid: 094f730e-5e2b-485e-8d9d-fee2902d3d5f
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: gl/glDisable, glDisable, glDisable function [OpenGL], opengl.gldisable
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
-	glDisable
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glDisable function


## -description


The <a href="https://msdn.microsoft.com/cd4590dd-ae41-47c9-9861-10d72318840f">glEnable</a> and <b>glDisable</b> functions enable or disable OpenGL capabilities.


## -parameters




### -param cap

A symbolic constant indicating an OpenGL capability.

For discussion of the values <i>cap</i> can take, see the following Remarks section.


## -returns



This function does not return a value.




## -remarks



The <a href="https://msdn.microsoft.com/cd4590dd-ae41-47c9-9861-10d72318840f">glEnable</a> and <b>glDisable</b> functions enable and disable various OpenGL graphics capabilities. Use <a href="https://msdn.microsoft.com/18df5a6f-dc21-434d-a2e8-2c58597df037">glIsEnabled</a> or <a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> to determine the current setting of any capability.

Both <a href="https://msdn.microsoft.com/cd4590dd-ae41-47c9-9861-10d72318840f">glEnable</a> and <b>glDisable</b> take a single argument, <i>cap</i>, which can assume one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>GL_ALPHA_TEST</td>
<td>If enabled, do alpha testing. See <a href="https://msdn.microsoft.com/6c0c06b5-1bad-4590-a262-f134f63f0936">glAlphaFunc</a>.</td>
</tr>
<tr>
<td>GL_AUTO_NORMAL</td>
<td>If enabled, compute surface normal vectors analytically when either GL_MAP2_VERTEX_3 or GL_MAP2_VERTEX_4 has generated vertices. See <a href="https://msdn.microsoft.com/8365a9bd-156b-4f57-8ceb-1edcbcea9eb4">glMap2</a>.</td>
</tr>
<tr>
<td>GL_BLEND</td>
<td>If enabled, blend the incoming RGBA color values with the values in the color buffers. See <a href="https://msdn.microsoft.com/6756774b-5eef-419a-a653-0b251aed65a0">glBlendFunc</a>.</td>
</tr>
<tr>
<td>GL_CLIP_PLANE<i>i</i></td>
<td>If enabled, clip geometry against user-defined clipping plane <i>i</i>. See <a href="https://msdn.microsoft.com/b70d2c30-7502-4399-8c08-5ec9a2a1919c">glClipPlane</a>.</td>
</tr>
<tr>
<td>GL_COLOR_LOGIC_OP</td>
<td>If enabled, apply the current logical operation to the incoming RGBA color and color buffer values. See <a href="https://msdn.microsoft.com/29edf9bd-f3b8-4de7-9afb-07714f4efd92">glLogicOp</a>.</td>
</tr>
<tr>
<td>GL_COLOR_MATERIAL</td>
<td>If enabled, have one or more material parameters track the current color. See <a href="https://msdn.microsoft.com/6dbef2c2-f902-4f25-8a87-9e3d710dd807">glColorMaterial</a>.</td>
</tr>
<tr>
<td>GL_CULL_FACE</td>
<td>If enabled, cull polygons based on their winding in window coordinates. See <a href="https://msdn.microsoft.com/53bf05b5-a68b-4d96-b4e7-2878a0a86a13">glCullFace</a>.</td>
</tr>
<tr>
<td>GL_DEPTH_TEST</td>
<td>If enabled, do depth comparisons and update the depth buffer. See <a href="https://msdn.microsoft.com/6ab8774a-8887-4c1e-b567-4492c0a60cf2">glDepthFunc</a> and <a href="https://msdn.microsoft.com/44aed5e5-4bd2-4e7f-ad05-1cf4be5254a5">glDepthRange</a>.</td>
</tr>
<tr>
<td>GL_DITHER</td>
<td>If enabled, dither color components or indexes before they are written to the color buffer.</td>
</tr>
<tr>
<td>GL_FOG</td>
<td>If enabled, blend a fog color into the post-texturing color. See <a href="https://msdn.microsoft.com/019c2006-679a-4611-8156-f6665d3ef5b2">glFog</a>.</td>
</tr>
<tr>
<td>GL_INDEX_LOGIC_OP</td>
<td>If enabled, apply the current logical operation to the incoming index and color buffer indices. See <a href="https://msdn.microsoft.com/29edf9bd-f3b8-4de7-9afb-07714f4efd92">glLogicOp</a>.</td>
</tr>
<tr>
<td>GL_LIGHT<i>i</i></td>
<td>If enabled, include light <i>i</i> in the evaluation of the lighting equation. See <a href="https://msdn.microsoft.com/8214765c-5722-4df0-88ed-3a5ac039aac4">glLightModel</a> and <a href="https://msdn.microsoft.com/004f0f53-4c72-48df-8231-6b39df464061">glLight</a>.</td>
</tr>
<tr>
<td>GL_LIGHTING</td>
<td>If enabled, use the current lighting parameters to compute the vertex color or index. If disabled, associate the current color or index with each vertex. See <a href="https://msdn.microsoft.com/a3f55129-da54-48ca-a629-88fed936551e">glMaterial</a>, <b>glLightModel</b>, and <b>glLight</b>.</td>
</tr>
<tr>
<td>GL_LINE_SMOOTH</td>
<td>If enabled, draw lines with correct filtering. If disabled, draw aliased lines. See <a href="https://msdn.microsoft.com/13a69fd7-5eee-42ec-bd05-5bd3c838d4d7">glLineWidth</a>.</td>
</tr>
<tr>
<td>GL_LINE_STIPPLE</td>
<td>If enabled, use the current line stipple pattern when drawing lines. See <a href="https://msdn.microsoft.com/256d968c-9e72-4aec-9faf-afe70f1087a8">glLineStipple</a>.</td>
</tr>
<tr>
<td>GL_LOGIC_OP</td>
<td>If enabled, apply the currently selected logical operation to the incoming and color-buffer indexes. See <a href="https://msdn.microsoft.com/29edf9bd-f3b8-4de7-9afb-07714f4efd92">glLogicOp</a>.</td>
</tr>
<tr>
<td>GL_MAP1_COLOR_4</td>
<td>If enabled, calls to <a href="https://msdn.microsoft.com/a170a84f-780a-42a5-a085-9ce355cf8825">glEvalCoord1</a>, <a href="https://msdn.microsoft.com/22cb0129-3cbe-4aa6-a3ac-b89576dfe71b">glEvalMesh1</a>, and <a href="https://msdn.microsoft.com/0cc70e14-eb22-4d04-a6c1-3943933a558e">glEvalPoint1</a> generate RGBA values. See also <a href="https://msdn.microsoft.com/47b0bd46-aa79-4146-8503-cddcc8b7b242">glMap1</a>.</td>
</tr>
<tr>
<td>GL_MAP1_INDEX</td>
<td>If enabled, calls to <b>glEvalCoord1</b>, <b>glEvalMesh1</b>, and <b>glEvalPoint1</b> generate color indexes. See also <b>glMap1</b>.</td>
</tr>
<tr>
<td>GL_MAP1_NORMAL</td>
<td>If enabled, calls to <a href="https://msdn.microsoft.com/a170a84f-780a-42a5-a085-9ce355cf8825">glEvalCoord1</a>, <a href="https://msdn.microsoft.com/22cb0129-3cbe-4aa6-a3ac-b89576dfe71b">glEvalMesh1</a>, and <a href="https://msdn.microsoft.com/0cc70e14-eb22-4d04-a6c1-3943933a558e">glEvalPoint1</a> generate normals. See also <a href="https://msdn.microsoft.com/47b0bd46-aa79-4146-8503-cddcc8b7b242">glMap1</a>.</td>
</tr>
<tr>
<td>GL_MAP1_TEXTURE_COORD_1</td>
<td>If enabled, calls to <b>glEvalCoord1</b>, <b>glEvalMesh1</b>, and <b>glEvalPoint1</b> generate <i>s</i> texture coordinates. See also <b>glMap1</b>.</td>
</tr>
<tr>
<td>GL_MAP1_TEXTURE_COORD_2</td>
<td>If enabled, calls to <a href="https://msdn.microsoft.com/a170a84f-780a-42a5-a085-9ce355cf8825">glEvalCoord1</a>, <a href="https://msdn.microsoft.com/22cb0129-3cbe-4aa6-a3ac-b89576dfe71b">glEvalMesh1</a>, and <a href="https://msdn.microsoft.com/0cc70e14-eb22-4d04-a6c1-3943933a558e">glEvalPoint1</a> generate <i>s</i> and <i>t</i> texture coordinates. See also <a href="https://msdn.microsoft.com/47b0bd46-aa79-4146-8503-cddcc8b7b242">glMap1</a>.</td>
</tr>
<tr>
<td>GL_MAP1_TEXTURE_COORD_3</td>
<td>If enabled, calls to <b>glEvalCoord1</b>, <b>glEvalMesh1</b>, and <b>glEvalPoint1</b> generate <i>s</i>, <i>t</i>, and <i>r</i> texture coordinates. See also <b>glMap1</b>.</td>
</tr>
<tr>
<td>GL_MAP1_TEXTURE_COORD_4</td>
<td>If enabled, calls to <a href="https://msdn.microsoft.com/a170a84f-780a-42a5-a085-9ce355cf8825">glEvalCoord1</a>, <a href="https://msdn.microsoft.com/22cb0129-3cbe-4aa6-a3ac-b89576dfe71b">glEvalMesh1</a>, and <a href="https://msdn.microsoft.com/0cc70e14-eb22-4d04-a6c1-3943933a558e">glEvalPoint1</a> generate <i>s</i>, <i>t</i>, <i>r</i>, and <i>q</i> texture coordinates. See also <a href="https://msdn.microsoft.com/47b0bd46-aa79-4146-8503-cddcc8b7b242">glMap1</a>.</td>
</tr>
<tr>
<td>GL_MAP1_VERTEX_3</td>
<td>If enabled, calls to <b>glEvalCoord1</b>, <b>glEvalMesh1</b>, and <b>glEvalPoint1</b> generate <i>x</i>, <i>y</i>, and <i>z</i> vertex coordinates. See also <b>glMap1</b>.</td>
</tr>
<tr>
<td>GL_MAP1_VERTEX_4</td>
<td>If enabled, calls to <a href="https://msdn.microsoft.com/a170a84f-780a-42a5-a085-9ce355cf8825">glEvalCoord1</a>, <a href="https://msdn.microsoft.com/22cb0129-3cbe-4aa6-a3ac-b89576dfe71b">glEvalMesh1</a>, and <a href="https://msdn.microsoft.com/0cc70e14-eb22-4d04-a6c1-3943933a558e">glEvalPoint1</a> generate homogeneous <i>x</i>, <i>y</i>, <i>z</i>, and <i>w</i> vertex coordinates. See also <a href="https://msdn.microsoft.com/47b0bd46-aa79-4146-8503-cddcc8b7b242">glMap1</a>.</td>
</tr>
<tr>
<td>GL_MAP2_COLOR_4</td>
<td>If enabled, calls to <a href="https://msdn.microsoft.com/a170a84f-780a-42a5-a085-9ce355cf8825">glEvalCoord2</a>, <a href="https://msdn.microsoft.com/22cb0129-3cbe-4aa6-a3ac-b89576dfe71b">glEvalMesh2</a>, and <a href="https://msdn.microsoft.com/0cc70e14-eb22-4d04-a6c1-3943933a558e">glEvalPoint2</a> generate RGBA values. See also <a href="https://msdn.microsoft.com/8365a9bd-156b-4f57-8ceb-1edcbcea9eb4">glMap2</a>.</td>
</tr>
<tr>
<td>GL_MAP2_INDEX</td>
<td>If enabled, calls to <b>glEvalCoord2</b>, <b>glEvalMesh2</b>, and <b>glEvalPoint2</b> generate color indexes. See also <b>glMap2</b>.</td>
</tr>
<tr>
<td>GL_MAP2_NORMAL</td>
<td>If enabled, calls to <a href="https://msdn.microsoft.com/a170a84f-780a-42a5-a085-9ce355cf8825">glEvalCoord2</a>, <a href="https://msdn.microsoft.com/22cb0129-3cbe-4aa6-a3ac-b89576dfe71b">glEvalMesh2</a>, and <a href="https://msdn.microsoft.com/0cc70e14-eb22-4d04-a6c1-3943933a558e">glEvalPoint2</a> generate normals. See also <a href="https://msdn.microsoft.com/8365a9bd-156b-4f57-8ceb-1edcbcea9eb4">glMap2</a>.</td>
</tr>
<tr>
<td>GL_MAP2_TEXTURE_COORD_1</td>
<td>If enabled, calls to <b>glEvalCoord2</b>, <b>glEvalMesh2</b>, and <b>glEvalPoint2</b> generate <i>s</i> texture coordinates. See also <b>glMap2</b>.</td>
</tr>
<tr>
<td>GL_MAP2_TEXTURE_COORD_2</td>
<td>If enabled, calls to <a href="https://msdn.microsoft.com/a170a84f-780a-42a5-a085-9ce355cf8825">glEvalCoord2</a>, <a href="https://msdn.microsoft.com/22cb0129-3cbe-4aa6-a3ac-b89576dfe71b">glEvalMesh2</a>, and <a href="https://msdn.microsoft.com/0cc70e14-eb22-4d04-a6c1-3943933a558e">glEvalPoint2</a> generate <i>s</i> and <i>t</i> texture coordinates. See also <a href="https://msdn.microsoft.com/8365a9bd-156b-4f57-8ceb-1edcbcea9eb4">glMap2</a>.</td>
</tr>
<tr>
<td>GL_MAP2_TEXTURE_COORD_3</td>
<td>If enabled, calls to <b>glEvalCoord2</b>, <b>glEvalMesh2</b>, and <b>glEvalPoint2</b> generate <i>s</i>, <i>t</i>, and <i>r</i> texture coordinates. See also <b>glMap2</b>.</td>
</tr>
<tr>
<td>GL_MAP2_TEXTURE_COORD_4</td>
<td>If enabled, calls to <a href="https://msdn.microsoft.com/a170a84f-780a-42a5-a085-9ce355cf8825">glEvalCoord2</a>, <a href="https://msdn.microsoft.com/22cb0129-3cbe-4aa6-a3ac-b89576dfe71b">glEvalMesh2</a>, and <a href="https://msdn.microsoft.com/0cc70e14-eb22-4d04-a6c1-3943933a558e">glEvalPoint2</a> generate <i>s</i>, <i>t</i>, <i>r</i>, and <i>q</i> texture coordinates. See also <a href="https://msdn.microsoft.com/8365a9bd-156b-4f57-8ceb-1edcbcea9eb4">glMap2</a>.</td>
</tr>
<tr>
<td>GL_MAP2_VERTEX_3</td>
<td>If enabled, calls to <b>glEvalCoord2</b>, <b>glEvalMesh2</b>, and <b>glEvalPoint2</b> generate <i>x</i>, <i>y</i>, and <i>z</i> vertex coordinates. See also <b>glMap2</b>.</td>
</tr>
<tr>
<td>GL_MAP2_VERTEX_4</td>
<td>If enabled, calls to <a href="https://msdn.microsoft.com/a170a84f-780a-42a5-a085-9ce355cf8825">glEvalCoord2</a>, <a href="https://msdn.microsoft.com/22cb0129-3cbe-4aa6-a3ac-b89576dfe71b">glEvalMesh2</a>, and <a href="https://msdn.microsoft.com/0cc70e14-eb22-4d04-a6c1-3943933a558e">glEvalPoint2</a> generate homogeneous <i>x</i>, <i>y</i>, <i>z</i>, and <i>w</i> vertex coordinates. See also <a href="https://msdn.microsoft.com/8365a9bd-156b-4f57-8ceb-1edcbcea9eb4">glMap2</a>.</td>
</tr>
<tr>
<td>GL_NORMALIZE</td>
<td>If enabled, normal vectors specified with <b>glNormal</b> are scaled to unit length after transformation. See <a href="https://msdn.microsoft.com/e90bfed4-ab72-43d2-b7b5-37a9fd6ecb4c">glNormal</a>.</td>
</tr>
<tr>
<td>GL_POINT_SMOOTH</td>
<td>If enabled, draw points with proper filtering. If disabled, draw aliased points. See <a href="https://msdn.microsoft.com/efa35fa8-721a-48e5-bf59-d33b9bbe7f73">glPointSize</a>.</td>
</tr>
<tr>
<td>GL_POLYGON_OFFSET_FILL</td>
<td>If enabled, and if the polygon is rendered in GL_FILL mode, an offset is added to depth values of a polygon's fragments before the depth comparison is performed. See <a href="https://msdn.microsoft.com/06bc1aba-1692-40f0-8535-2cb65b487490">glPolygonOffset</a><b>.</b></td>
</tr>
<tr>
<td>GL_POLYGON_OFFSET_LINE</td>
<td>If enabled, and if the polygon is rendered in GL_LINE mode, an offset is added to depth values of a polygon's fragments before the depth comparison is performed. See <b>glPolygonOffset</b>.</td>
</tr>
<tr>
<td>GL_POLYGON_OFFSET_POINT</td>
<td>If enabled, an offset is added to depth values of a polygon's fragments before the depth comparison is performed, if the polygon is rendered in GL_POINT mode. See <a href="https://msdn.microsoft.com/06bc1aba-1692-40f0-8535-2cb65b487490">glPolygonOffset</a>.</td>
</tr>
<tr>
<td>GL_POLYGON_SMOOTH</td>
<td>If enabled, draw polygons with proper filtering. If disabled, draw aliased polygons. See <a href="https://msdn.microsoft.com/d8781bae-e78c-40fb-9f33-c742c70ebda1">glPolygonMode</a>.</td>
</tr>
<tr>
<td>GL_POLYGON_STIPPLE</td>
<td>If enabled, use the current polygon stipple pattern when rendering polygons. See <a href="https://msdn.microsoft.com/e066f9cf-36da-4a3b-a34f-2f8a6f5a0ae6">glPolygonStipple</a>.</td>
</tr>
<tr>
<td>GL_SCISSOR_TEST</td>
<td>If enabled, discard fragments that are outside the scissor rectangle. See <a href="https://msdn.microsoft.com/c06a1d20-bf7b-4283-b0fe-8bd80bece4ce">glScissor</a>.</td>
</tr>
<tr>
<td>GL_STENCIL_TEST</td>
<td>If enabled, do stencil testing and update the stencil buffer. See <a href="https://msdn.microsoft.com/6c84415b-4d22-494b-90f2-6243d1406725">glStencilFunc</a> and <a href="https://msdn.microsoft.com/16809735-5624-49cf-bfa5-9908d008b234">glStencilOp</a>.</td>
</tr>
<tr>
<td>GL_TEXTURE_1D</td>
<td>If enabled, one-dimensional texturing is performed (unless two-dimensional texturing is also enabled). See <a href="https://msdn.microsoft.com/4f537b89-2ea2-4e2e-8c57-c372bf53f12c">glTexImage1D</a>.</td>
</tr>
<tr>
<td>GL_TEXTURE_2D</td>
<td>If enabled, two-dimensional texturing is performed. See <a href="https://msdn.microsoft.com/e8b9c692-5239-47de-86eb-80c247c60e1d">glTexImage2D</a>.</td>
</tr>
<tr>
<td>GL_TEXTURE_GEN_Q</td>
<td>If enabled, the <i>q</i> texture coordinate is computed using the texture-generation function defined with <a href="https://msdn.microsoft.com/958c2932-c220-412c-a85e-eed613332dea">glTexGen</a>. Otherwise, the current <i>q</i> texture coordinate is used.</td>
</tr>
<tr>
<td>GL_TEXTURE_GEN_R</td>
<td>If enabled, the <i>r</i> texture coordinate is computed using the texture generation function defined with <a href="https://msdn.microsoft.com/958c2932-c220-412c-a85e-eed613332dea">glTexGen</a>. If disabled, the current <i>r</i> texture coordinate is used.</td>
</tr>
<tr>
<td>GL_TEXTURE_GEN_S</td>
<td>If enabled, the <i>s</i> texture coordinate is computed using the texture generation function defined with <b>glTexGen</b>. If disabled, the current <i>s</i> texture coordinate is used.</td>
</tr>
<tr>
<td>GL_TEXTURE_GEN_T</td>
<td>If enabled, the <i>t</i> texture coordinate is computed using the texture generation function defined with <a href="https://msdn.microsoft.com/958c2932-c220-412c-a85e-eed613332dea">glTexGen</a>. If disabled, the current <i>t</i> texture coordinate is used.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/6c0c06b5-1bad-4590-a262-f134f63f0936">glAlphaFunc</a>



<a href="https://msdn.microsoft.com/2c4d76bb-e4c9-4baa-a190-66298b8a4335">glArrayElement</a>



<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/6756774b-5eef-419a-a653-0b251aed65a0">glBlendFunc</a>



<a href="https://msdn.microsoft.com/b70d2c30-7502-4399-8c08-5ec9a2a1919c">glClipPlane</a>



<a href="https://msdn.microsoft.com/6dbef2c2-f902-4f25-8a87-9e3d710dd807">glColorMaterial</a>



<a href="https://msdn.microsoft.com/4d9d05fb-691d-4b71-b079-c42dc7103055">glColorPointer</a>



<a href="https://msdn.microsoft.com/53bf05b5-a68b-4d96-b4e7-2878a0a86a13">glCullFace</a>



<a href="https://msdn.microsoft.com/6ab8774a-8887-4c1e-b567-4492c0a60cf2">glDepthFunc</a>



<a href="https://msdn.microsoft.com/44aed5e5-4bd2-4e7f-ad05-1cf4be5254a5">glDepthRange</a>



<a href="https://msdn.microsoft.com/6ebd467b-5a63-43e4-b3fd-242c704d7d13">glDrawArrays</a>



<a href="https://msdn.microsoft.com/e0e7e442-533d-4c41-addd-a215ce0b1c56">glEdgeFlagPointer</a>



<a href="https://msdn.microsoft.com/cd4590dd-ae41-47c9-9861-10d72318840f">glEnable</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/a170a84f-780a-42a5-a085-9ce355cf8825">glEvalCoord1</a>



<a href="https://msdn.microsoft.com/22cb0129-3cbe-4aa6-a3ac-b89576dfe71b">glEvalMesh1</a>



<a href="https://msdn.microsoft.com/0cc70e14-eb22-4d04-a6c1-3943933a558e">glEvalPoint1</a>



<a href="https://msdn.microsoft.com/019c2006-679a-4611-8156-f6665d3ef5b2">glFog</a>



<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a>



<a href="https://msdn.microsoft.com/b435d950-1f87-4041-93e4-f1f8786cabdb">glIndexPointer</a>



<a href="https://msdn.microsoft.com/18df5a6f-dc21-434d-a2e8-2c58597df037">glIsEnabled</a>



<a href="https://msdn.microsoft.com/004f0f53-4c72-48df-8231-6b39df464061">glLight</a>



<a href="https://msdn.microsoft.com/8214765c-5722-4df0-88ed-3a5ac039aac4">glLightModel</a>



<a href="https://msdn.microsoft.com/256d968c-9e72-4aec-9faf-afe70f1087a8">glLineStipple</a>



<a href="https://msdn.microsoft.com/13a69fd7-5eee-42ec-bd05-5bd3c838d4d7">glLineWidth</a>



<a href="https://msdn.microsoft.com/29edf9bd-f3b8-4de7-9afb-07714f4efd92">glLogicOp</a>



<a href="https://msdn.microsoft.com/47b0bd46-aa79-4146-8503-cddcc8b7b242">glMap1</a>



<a href="https://msdn.microsoft.com/8365a9bd-156b-4f57-8ceb-1edcbcea9eb4">glMap2</a>



<a href="https://msdn.microsoft.com/a3f55129-da54-48ca-a629-88fed936551e">glMaterial</a>



<a href="https://msdn.microsoft.com/e90bfed4-ab72-43d2-b7b5-37a9fd6ecb4c">glNormal</a>



<a href="https://msdn.microsoft.com/6ffb0522-87cc-4be1-a5b1-f6fd30e04b43">glNormalPointer</a>



<a href="https://msdn.microsoft.com/efa35fa8-721a-48e5-bf59-d33b9bbe7f73">glPointSize</a>



<a href="https://msdn.microsoft.com/d8781bae-e78c-40fb-9f33-c742c70ebda1">glPolygonMode</a>



<a href="https://msdn.microsoft.com/e066f9cf-36da-4a3b-a34f-2f8a6f5a0ae6">glPolygonStipple</a>



<a href="https://msdn.microsoft.com/c06a1d20-bf7b-4283-b0fe-8bd80bece4ce">glScissor</a>



<a href="https://msdn.microsoft.com/6c84415b-4d22-494b-90f2-6243d1406725">glStencilFunc</a>



<a href="https://msdn.microsoft.com/16809735-5624-49cf-bfa5-9908d008b234">glStencilOp</a>



<a href="https://msdn.microsoft.com/c3640a1b-ccc7-4f1a-94a5-a164f7377dbc">glTexCoordPointer</a>



<a href="https://msdn.microsoft.com/958c2932-c220-412c-a85e-eed613332dea">glTexGen</a>



<a href="https://msdn.microsoft.com/4f537b89-2ea2-4e2e-8c57-c372bf53f12c">glTexImage1D</a>



<a href="https://msdn.microsoft.com/e8b9c692-5239-47de-86eb-80c247c60e1d">glTexImage2D</a>
 

 

