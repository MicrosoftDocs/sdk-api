---
UID: NF:gl.glIsEnabled
title: glIsEnabled function
author: windows-driver-content
description: The gllsEnabled function tests whether a capability is enabled.
old-location: opengl\glisenabled.htm
old-project: OpenGL
ms.assetid: 18df5a6f-dc21-434d-a2e8-2c58597df037
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GL_ALPHA_TEST, GL_AUTO_NORMAL, GL_BLEND, GL_CLIP_PLANE i, GL_COLOR_ARRAY, GL_COLOR_LOGIC_OP, GL_COLOR_MATERIAL, GL_CULL_FACE, GL_DEPTH_TEST, GL_DITHER, GL_FOG, GL_INDEX_ARRAY, GL_INDEX_LOGIC_OP, GL_LIGHT i, GL_LIGHTING, GL_LINE_SMOOTH, GL_LINE_STIPPLE, GL_MAP1_COLOR_4, GL_MAP1_INDEX, GL_MAP1_NORMAL, GL_MAP1_TEXTURE_COORD_1, GL_MAP1_TEXTURE_COORD_2, GL_MAP1_TEXTURE_COORD_3, GL_MAP1_TEXTURE_COORD_4, GL_MAP1_VERTEX_3, GL_MAP1_VERTEX_4, GL_MAP2_COLOR_4, GL_MAP2_INDEX, GL_MAP2_NORMAL, GL_MAP2_TEXTURE_COORD_1, GL_MAP2_TEXTURE_COORD_2, GL_MAP2_TEXTURE_COORD_3, GL_MAP2_TEXTURE_COORD_4, GL_MAP2_VERTEX_3, GL_MAP2_VERTEX_4, GL_NORMALIZE, GL_NORMAL_ARRAY, GL_POINT_SMOOTH, GL_POLYGON_OFFSET_FILL, GL_POLYGON_OFFSET_LINE, GL_POLYGON_OFFSET_POINT, GL_POLYGON_SMOOTH, GL_POLYGON_STIPPLE, GL_SCISSOR_TEST, GL_STENCIL_TEST, GL_TEXTURE_1D, GL_TEXTURE_2D, GL_TEXTURE_COORD_ARRAY, GL_TEXTURE_GEN_Q, GL_TEXTURE_GEN_R, GL_TEXTURE_GEN_S, GL_TEXTURE_GEN_T, GL_VERTEX_ARRAY, _ogl_glIsEnabled, gl/glIsEnabled, glIsEnabled, glIsEnabled function [OpenGL], opengl.glisenabled
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
-	glIsEnabled
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glIsEnabled function


## -description


The <b>gllsEnabled</b> function tests whether a capability is enabled.


## -parameters




### -param cap

A symbolic constant indicating an OpenGL capability. The following capabilities are accepted.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GL_ALPHA_TEST"></a><a id="gl_alpha_test"></a><dl>
<dt><b>GL_ALPHA_TEST</b></dt>
</dl>
</td>
<td width="60%">
See <a href="https://msdn.microsoft.com/6c0c06b5-1bad-4590-a262-f134f63f0936">glAlphaFunc</a>


</td>
</tr>
<tr>
<td width="40%"><a id="GL_AUTO_NORMAL"></a><a id="gl_auto_normal"></a><dl>
<dt><b>GL_AUTO_NORMAL</b></dt>
</dl>
</td>
<td width="60%">
See <a href="https://msdn.microsoft.com/a170a84f-780a-42a5-a085-9ce355cf8825">glEvalCoord</a>


</td>
</tr>
<tr>
<td width="40%"><a id="GL_BLEND"></a><a id="gl_blend"></a><dl>
<dt><b>GL_BLEND</b></dt>
</dl>
</td>
<td width="60%">
See <a href="https://msdn.microsoft.com/6756774b-5eef-419a-a653-0b251aed65a0">glBlendFunc</a>


</td>
</tr>
<tr>
<td width="40%"><a id="GL_CLIP_PLANE_i"></a><a id="gl_clip_plane_i"></a><a id="GL_CLIP_PLANE_I"></a><dl>
<dt><b>GL_CLIP_PLANE <i>i</i></b></dt>
</dl>
</td>
<td width="60%">
See <a href="https://msdn.microsoft.com/b70d2c30-7502-4399-8c08-5ec9a2a1919c">glClipPlane</a>


</td>
</tr>
<tr>
<td width="40%"><a id="GL_COLOR_ARRAY"></a><a id="gl_color_array"></a><dl>
<dt><b>GL_COLOR_ARRAY</b></dt>
</dl>
</td>
<td width="60%">
See <a href="https://msdn.microsoft.com/4d9d05fb-691d-4b71-b079-c42dc7103055">glColorPointer</a>


</td>
</tr>
<tr>
<td width="40%"><a id="GL_COLOR_LOGIC_OP"></a><a id="gl_color_logic_op"></a><dl>
<dt><b>GL_COLOR_LOGIC_OP</b></dt>
</dl>
</td>
<td width="60%">
See <a href="https://msdn.microsoft.com/29edf9bd-f3b8-4de7-9afb-07714f4efd92">glLogicOp</a>


</td>
</tr>
<tr>
<td width="40%"><a id="GL_COLOR_MATERIAL"></a><a id="gl_color_material"></a><dl>
<dt><b>GL_COLOR_MATERIAL</b></dt>
</dl>
</td>
<td width="60%">
See <a href="https://msdn.microsoft.com/6dbef2c2-f902-4f25-8a87-9e3d710dd807">glColorMaterial</a>


</td>
</tr>
<tr>
<td width="40%"><a id="GL_CULL_FACE"></a><a id="gl_cull_face"></a><dl>
<dt><b>GL_CULL_FACE</b></dt>
</dl>
</td>
<td width="60%">
See <a href="https://msdn.microsoft.com/53bf05b5-a68b-4d96-b4e7-2878a0a86a13">glCullFace</a>


</td>
</tr>
<tr>
<td width="40%"><a id="GL_DEPTH_TEST"></a><a id="gl_depth_test"></a><dl>
<dt><b>GL_DEPTH_TEST</b></dt>
</dl>
</td>
<td width="60%">
See <a href="https://msdn.microsoft.com/6ab8774a-8887-4c1e-b567-4492c0a60cf2">glDepthFunc</a> and <a href="https://msdn.microsoft.com/44aed5e5-4bd2-4e7f-ad05-1cf4be5254a5">glDepthRange</a>


</td>
</tr>
<tr>
<td width="40%"><a id="GL_DITHER"></a><a id="gl_dither"></a><dl>
<dt><b>GL_DITHER</b></dt>
</dl>
</td>
<td width="60%">
See <a href="https://msdn.microsoft.com/cd4590dd-ae41-47c9-9861-10d72318840f">glEnable</a>


</td>
</tr>
<tr>
<td width="40%"><a id="GL_FOG"></a><a id="gl_fog"></a><dl>
<dt><b>GL_FOG</b></dt>
</dl>
</td>
<td width="60%">
See <a href="https://msdn.microsoft.com/019c2006-679a-4611-8156-f6665d3ef5b2">glFog</a>


</td>
</tr>
<tr>
<td width="40%"><a id="GL_INDEX_ARRAY"></a><a id="gl_index_array"></a><dl>
<dt><b>GL_INDEX_ARRAY</b></dt>
</dl>
</td>
<td width="60%">
See <a href="https://msdn.microsoft.com/b435d950-1f87-4041-93e4-f1f8786cabdb">glIndexPointer</a>


</td>
</tr>
<tr>
<td width="40%"><a id="GL_INDEX_LOGIC_OP"></a><a id="gl_index_logic_op"></a><dl>
<dt><b>GL_INDEX_LOGIC_OP</b></dt>
</dl>
</td>
<td width="60%">
See <a href="https://msdn.microsoft.com/29edf9bd-f3b8-4de7-9afb-07714f4efd92">glLogicOp</a>


</td>
</tr>
<tr>
<td width="40%"><a id="GL_LIGHT_i"></a><a id="gl_light_i"></a><a id="GL_LIGHT_I"></a><dl>
<dt><b>GL_LIGHT <i>i</i></b></dt>
</dl>
</td>
<td width="60%">
See <a href="https://msdn.microsoft.com/8214765c-5722-4df0-88ed-3a5ac039aac4">glLightModel</a> and <a href="https://msdn.microsoft.com/004f0f53-4c72-48df-8231-6b39df464061">glLight</a>


</td>
</tr>
<tr>
<td width="40%"><a id="GL_LIGHTING"></a><a id="gl_lighting"></a><dl>
<dt><b>GL_LIGHTING</b></dt>
</dl>
</td>
<td width="60%">
See <a href="https://msdn.microsoft.com/a3f55129-da54-48ca-a629-88fed936551e">glMaterial</a>, <a href="https://msdn.microsoft.com/8214765c-5722-4df0-88ed-3a5ac039aac4">glLightModel</a>, and <a href="https://msdn.microsoft.com/004f0f53-4c72-48df-8231-6b39df464061">glLight</a>


</td>
</tr>
<tr>
<td width="40%"><a id="GL_LINE_SMOOTH"></a><a id="gl_line_smooth"></a><dl>
<dt><b>GL_LINE_SMOOTH</b></dt>
</dl>
</td>
<td width="60%">
See <a href="https://msdn.microsoft.com/13a69fd7-5eee-42ec-bd05-5bd3c838d4d7">glLineWidth</a>


</td>
</tr>
<tr>
<td width="40%"><a id="GL_LINE_STIPPLE"></a><a id="gl_line_stipple"></a><dl>
<dt><b>GL_LINE_STIPPLE</b></dt>
</dl>
</td>
<td width="60%">
See <a href="https://msdn.microsoft.com/256d968c-9e72-4aec-9faf-afe70f1087a8">glLineStipple</a>


</td>
</tr>
<tr>
<td width="40%"><a id="GL_MAP1_COLOR_4"></a><a id="gl_map1_color_4"></a><dl>
<dt><b>GL_MAP1_COLOR_4</b></dt>
</dl>
</td>
<td width="60%">
See <a href="https://msdn.microsoft.com/47b0bd46-aa79-4146-8503-cddcc8b7b242">glMap1</a>


</td>
</tr>
<tr>
<td width="40%"><a id="GL_MAP1_INDEX"></a><a id="gl_map1_index"></a><dl>
<dt><b>GL_MAP1_INDEX</b></dt>
</dl>
</td>
<td width="60%">
See <a href="https://msdn.microsoft.com/47b0bd46-aa79-4146-8503-cddcc8b7b242">glMap1</a>


</td>
</tr>
<tr>
<td width="40%"><a id="GL_MAP1_NORMAL"></a><a id="gl_map1_normal"></a><dl>
<dt><b>GL_MAP1_NORMAL</b></dt>
</dl>
</td>
<td width="60%">
See <a href="https://msdn.microsoft.com/47b0bd46-aa79-4146-8503-cddcc8b7b242">glMap1</a>


</td>
</tr>
<tr>
<td width="40%"><a id="GL_MAP1_TEXTURE_COORD_1"></a><a id="gl_map1_texture_coord_1"></a><dl>
<dt><b>GL_MAP1_TEXTURE_COORD_1</b></dt>
</dl>
</td>
<td width="60%">
See <a href="https://msdn.microsoft.com/47b0bd46-aa79-4146-8503-cddcc8b7b242">glMap1</a>


</td>
</tr>
<tr>
<td width="40%"><a id="GL_MAP1_TEXTURE_COORD_2"></a><a id="gl_map1_texture_coord_2"></a><dl>
<dt><b>GL_MAP1_TEXTURE_COORD_2</b></dt>
</dl>
</td>
<td width="60%">
See <a href="https://msdn.microsoft.com/47b0bd46-aa79-4146-8503-cddcc8b7b242">glMap1</a>


</td>
</tr>
<tr>
<td width="40%"><a id="GL_MAP1_TEXTURE_COORD_3"></a><a id="gl_map1_texture_coord_3"></a><dl>
<dt><b>GL_MAP1_TEXTURE_COORD_3</b></dt>
</dl>
</td>
<td width="60%">
See <a href="https://msdn.microsoft.com/47b0bd46-aa79-4146-8503-cddcc8b7b242">glMap1</a>


</td>
</tr>
<tr>
<td width="40%"><a id="GL_MAP1_TEXTURE_COORD_4"></a><a id="gl_map1_texture_coord_4"></a><dl>
<dt><b>GL_MAP1_TEXTURE_COORD_4</b></dt>
</dl>
</td>
<td width="60%">
See <a href="https://msdn.microsoft.com/47b0bd46-aa79-4146-8503-cddcc8b7b242">glMap1</a>


</td>
</tr>
<tr>
<td width="40%"><a id="GL_MAP1_VERTEX_3"></a><a id="gl_map1_vertex_3"></a><dl>
<dt><b>GL_MAP1_VERTEX_3</b></dt>
</dl>
</td>
<td width="60%">
See <a href="https://msdn.microsoft.com/47b0bd46-aa79-4146-8503-cddcc8b7b242">glMap1</a>


</td>
</tr>
<tr>
<td width="40%"><a id="GL_MAP1_VERTEX_4"></a><a id="gl_map1_vertex_4"></a><dl>
<dt><b>GL_MAP1_VERTEX_4</b></dt>
</dl>
</td>
<td width="60%">
See <a href="https://msdn.microsoft.com/47b0bd46-aa79-4146-8503-cddcc8b7b242">glMap1</a>


</td>
</tr>
<tr>
<td width="40%"><a id="GL_MAP2_COLOR_4"></a><a id="gl_map2_color_4"></a><dl>
<dt><b>GL_MAP2_COLOR_4</b></dt>
</dl>
</td>
<td width="60%">
See <a href="https://msdn.microsoft.com/8365a9bd-156b-4f57-8ceb-1edcbcea9eb4">glMap2</a>


</td>
</tr>
<tr>
<td width="40%"><a id="GL_MAP2_INDEX"></a><a id="gl_map2_index"></a><dl>
<dt><b>GL_MAP2_INDEX</b></dt>
</dl>
</td>
<td width="60%">
See <a href="https://msdn.microsoft.com/8365a9bd-156b-4f57-8ceb-1edcbcea9eb4">glMap2</a>


</td>
</tr>
<tr>
<td width="40%"><a id="GL_MAP2_NORMAL"></a><a id="gl_map2_normal"></a><dl>
<dt><b>GL_MAP2_NORMAL</b></dt>
</dl>
</td>
<td width="60%">
See <a href="https://msdn.microsoft.com/8365a9bd-156b-4f57-8ceb-1edcbcea9eb4">glMap2</a>


</td>
</tr>
<tr>
<td width="40%"><a id="GL_MAP2_TEXTURE_COORD_1"></a><a id="gl_map2_texture_coord_1"></a><dl>
<dt><b>GL_MAP2_TEXTURE_COORD_1</b></dt>
</dl>
</td>
<td width="60%">
See <a href="https://msdn.microsoft.com/8365a9bd-156b-4f57-8ceb-1edcbcea9eb4">glMap2</a>


</td>
</tr>
<tr>
<td width="40%"><a id="GL_MAP2_TEXTURE_COORD_2"></a><a id="gl_map2_texture_coord_2"></a><dl>
<dt><b>GL_MAP2_TEXTURE_COORD_2</b></dt>
</dl>
</td>
<td width="60%">
See <a href="https://msdn.microsoft.com/8365a9bd-156b-4f57-8ceb-1edcbcea9eb4">glMap2</a>


</td>
</tr>
<tr>
<td width="40%"><a id="GL_MAP2_TEXTURE_COORD_3"></a><a id="gl_map2_texture_coord_3"></a><dl>
<dt><b>GL_MAP2_TEXTURE_COORD_3</b></dt>
</dl>
</td>
<td width="60%">
See <a href="https://msdn.microsoft.com/8365a9bd-156b-4f57-8ceb-1edcbcea9eb4">glMap2</a>


</td>
</tr>
<tr>
<td width="40%"><a id="GL_MAP2_TEXTURE_COORD_4"></a><a id="gl_map2_texture_coord_4"></a><dl>
<dt><b>GL_MAP2_TEXTURE_COORD_4</b></dt>
</dl>
</td>
<td width="60%">
See <a href="https://msdn.microsoft.com/8365a9bd-156b-4f57-8ceb-1edcbcea9eb4">glMap2</a>


</td>
</tr>
<tr>
<td width="40%"><a id="GL_MAP2_VERTEX_3"></a><a id="gl_map2_vertex_3"></a><dl>
<dt><b>GL_MAP2_VERTEX_3</b></dt>
</dl>
</td>
<td width="60%">
See <a href="https://msdn.microsoft.com/8365a9bd-156b-4f57-8ceb-1edcbcea9eb4">glMap2</a>


</td>
</tr>
<tr>
<td width="40%"><a id="GL_MAP2_VERTEX_4"></a><a id="gl_map2_vertex_4"></a><dl>
<dt><b>GL_MAP2_VERTEX_4</b></dt>
</dl>
</td>
<td width="60%">
See <a href="https://msdn.microsoft.com/8365a9bd-156b-4f57-8ceb-1edcbcea9eb4">glMap2</a>


</td>
</tr>
<tr>
<td width="40%"><a id="GL_NORMAL_ARRAY"></a><a id="gl_normal_array"></a><dl>
<dt><b>GL_NORMAL_ARRAY</b></dt>
</dl>
</td>
<td width="60%">
See <a href="https://msdn.microsoft.com/6ffb0522-87cc-4be1-a5b1-f6fd30e04b43">glNormalPointer</a>


</td>
</tr>
<tr>
<td width="40%"><a id="GL_NORMALIZE"></a><a id="gl_normalize"></a><dl>
<dt><b>GL_NORMALIZE</b></dt>
</dl>
</td>
<td width="60%">
See <a href="https://msdn.microsoft.com/e90bfed4-ab72-43d2-b7b5-37a9fd6ecb4c">glNormal</a>


</td>
</tr>
<tr>
<td width="40%"><a id="GL_POINT_SMOOTH"></a><a id="gl_point_smooth"></a><dl>
<dt><b>GL_POINT_SMOOTH</b></dt>
</dl>
</td>
<td width="60%">
See <a href="https://msdn.microsoft.com/efa35fa8-721a-48e5-bf59-d33b9bbe7f73">glPointSize</a>


</td>
</tr>
<tr>
<td width="40%"><a id="GL_POLYGON_OFFSET_FILL"></a><a id="gl_polygon_offset_fill"></a><dl>
<dt><b>GL_POLYGON_OFFSET_FILL</b></dt>
</dl>
</td>
<td width="60%">
See <a href="https://msdn.microsoft.com/06bc1aba-1692-40f0-8535-2cb65b487490">glPolygonOffset</a>


</td>
</tr>
<tr>
<td width="40%"><a id="GL_POLYGON_OFFSET_LINE"></a><a id="gl_polygon_offset_line"></a><dl>
<dt><b>GL_POLYGON_OFFSET_LINE</b></dt>
</dl>
</td>
<td width="60%">
See <a href="https://msdn.microsoft.com/06bc1aba-1692-40f0-8535-2cb65b487490">glPolygonOffset</a>


</td>
</tr>
<tr>
<td width="40%"><a id="GL_POLYGON_OFFSET_POINT"></a><a id="gl_polygon_offset_point"></a><dl>
<dt><b>GL_POLYGON_OFFSET_POINT</b></dt>
</dl>
</td>
<td width="60%">
See <a href="https://msdn.microsoft.com/06bc1aba-1692-40f0-8535-2cb65b487490">glPolygonOffset</a>


</td>
</tr>
<tr>
<td width="40%"><a id="GL_POLYGON_SMOOTH"></a><a id="gl_polygon_smooth"></a><dl>
<dt><b>GL_POLYGON_SMOOTH</b></dt>
</dl>
</td>
<td width="60%">
See <a href="https://msdn.microsoft.com/d8781bae-e78c-40fb-9f33-c742c70ebda1">glPolygonMode</a>


</td>
</tr>
<tr>
<td width="40%"><a id="GL_POLYGON_STIPPLE"></a><a id="gl_polygon_stipple"></a><dl>
<dt><b>GL_POLYGON_STIPPLE</b></dt>
</dl>
</td>
<td width="60%">
See <a href="https://msdn.microsoft.com/e066f9cf-36da-4a3b-a34f-2f8a6f5a0ae6">glPolygonStipple</a>


</td>
</tr>
<tr>
<td width="40%"><a id="GL_SCISSOR_TEST"></a><a id="gl_scissor_test"></a><dl>
<dt><b>GL_SCISSOR_TEST</b></dt>
</dl>
</td>
<td width="60%">
See <a href="https://msdn.microsoft.com/c06a1d20-bf7b-4283-b0fe-8bd80bece4ce">glScissor</a>


</td>
</tr>
<tr>
<td width="40%"><a id="GL_STENCIL_TEST"></a><a id="gl_stencil_test"></a><dl>
<dt><b>GL_STENCIL_TEST</b></dt>
</dl>
</td>
<td width="60%">
See <a href="https://msdn.microsoft.com/6c84415b-4d22-494b-90f2-6243d1406725">glStencilFunc</a> and <a href="https://msdn.microsoft.com/16809735-5624-49cf-bfa5-9908d008b234">glStencilOp</a>


</td>
</tr>
<tr>
<td width="40%"><a id="GL_TEXTURE_1D"></a><a id="gl_texture_1d"></a><dl>
<dt><b>GL_TEXTURE_1D</b></dt>
</dl>
</td>
<td width="60%">
See <a href="https://msdn.microsoft.com/4f537b89-2ea2-4e2e-8c57-c372bf53f12c">glTexImage1D</a>


</td>
</tr>
<tr>
<td width="40%"><a id="GL_TEXTURE_2D"></a><a id="gl_texture_2d"></a><dl>
<dt><b>GL_TEXTURE_2D</b></dt>
</dl>
</td>
<td width="60%">
See <a href="https://msdn.microsoft.com/e8b9c692-5239-47de-86eb-80c247c60e1d">glTexImage2D</a>


</td>
</tr>
<tr>
<td width="40%"><a id="GL_TEXTURE_COORD_ARRAY"></a><a id="gl_texture_coord_array"></a><dl>
<dt><b>GL_TEXTURE_COORD_ARRAY</b></dt>
</dl>
</td>
<td width="60%">
See <a href="https://msdn.microsoft.com/c3640a1b-ccc7-4f1a-94a5-a164f7377dbc">glTexCoordPointer</a>


</td>
</tr>
<tr>
<td width="40%"><a id="GL_TEXTURE_GEN_Q"></a><a id="gl_texture_gen_q"></a><dl>
<dt><b>GL_TEXTURE_GEN_Q</b></dt>
</dl>
</td>
<td width="60%">
See <a href="https://msdn.microsoft.com/958c2932-c220-412c-a85e-eed613332dea">glTexGen</a>


</td>
</tr>
<tr>
<td width="40%"><a id="GL_TEXTURE_GEN_R"></a><a id="gl_texture_gen_r"></a><dl>
<dt><b>GL_TEXTURE_GEN_R</b></dt>
</dl>
</td>
<td width="60%">
See <a href="https://msdn.microsoft.com/958c2932-c220-412c-a85e-eed613332dea">glTexGen</a>


</td>
</tr>
<tr>
<td width="40%"><a id="GL_TEXTURE_GEN_S"></a><a id="gl_texture_gen_s"></a><dl>
<dt><b>GL_TEXTURE_GEN_S</b></dt>
</dl>
</td>
<td width="60%">
See <a href="https://msdn.microsoft.com/958c2932-c220-412c-a85e-eed613332dea">glTexGen</a>


</td>
</tr>
<tr>
<td width="40%"><a id="GL_TEXTURE_GEN_T"></a><a id="gl_texture_gen_t"></a><dl>
<dt><b>GL_TEXTURE_GEN_T</b></dt>
</dl>
</td>
<td width="60%">
See <a href="https://msdn.microsoft.com/958c2932-c220-412c-a85e-eed613332dea">glTexGen</a>


</td>
</tr>
<tr>
<td width="40%"><a id="GL_VERTEX_ARRAY"></a><a id="gl_vertex_array"></a><dl>
<dt><b>GL_VERTEX_ARRAY</b></dt>
</dl>
</td>
<td width="60%">
See <a href="https://msdn.microsoft.com/e5f97fdc-9448-4389-8533-3855a3213feb">glVertexPointer</a>


</td>
</tr>
</table>
 


## -remarks



The <b>gllsEnabled</b> function returns GL_TRUE if <i>cap</i> is an enabled capability and returns GL_FALSE otherwise.




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/cd4590dd-ae41-47c9-9861-10d72318840f">glEnable</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>
 

 

