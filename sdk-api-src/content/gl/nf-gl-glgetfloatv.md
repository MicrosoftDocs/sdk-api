---
UID: NF:gl.glGetFloatv
title: glGetFloatv function
author: windows-driver-content
description: The glGetFloatv function returns the value or values of a selected parameter.
old-location: opengl\glgetfloatv.htm
old-project: OpenGL
ms.assetid: 1701ae76-c60d-431d-8d37-a0a388a44bbc
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GL_ACCUM_ALPHA_BITS, GL_ACCUM_BLUE_BITS, GL_ACCUM_CLEAR_VALUE, GL_ACCUM_GREEN_BITS, GL_ACCUM_RED_BITS, GL_ALPHA_BIAS, GL_ALPHA_BITS, GL_ALPHA_SCALE, GL_ALPHA_TEST, GL_ALPHA_TEST_FUNC, GL_ALPHA_TEST_REF, GL_ATTRIB_STACK_DEPTH, GL_AUTO_NORMAL, GL_AUX_BUFFERS, GL_BLEND, GL_BLEND_DST, GL_BLEND_SRC, GL_BLUE_BIAS, GL_BLUE_BITS, GL_BLUE_SCALE, GL_CLIENT_ATTRIB_STACK_DEPTH, GL_CLIP_PLANEi, GL_COLOR_ARRAY, GL_COLOR_ARRAY_SIZE, GL_COLOR_ARRAY_STRIDE, GL_COLOR_ARRAY_TYPE, GL_COLOR_CLEAR_VALUE, GL_COLOR_LOGIC_OP, GL_COLOR_MATERIAL, GL_COLOR_MATERIAL_FACE, GL_COLOR_MATERIAL_PARAMETER, GL_COLOR_WRITEMASK, GL_CULL_FACE, GL_CULL_FACE_MODE, GL_CURRENT_COLOR, GL_CURRENT_INDEX, GL_CURRENT_NORMAL, GL_CURRENT_RASTER_COLOR, GL_CURRENT_RASTER_DISTANCE, GL_CURRENT_RASTER_INDEX, GL_CURRENT_RASTER_POSITION, GL_CURRENT_RASTER_POSITION_VALID, GL_CURRENT_RASTER_TEXTURE_COORDS, GL_CURRENT_TEXTURE_COORDS, GL_DEPTH_BIAS, GL_DEPTH_BITS, GL_DEPTH_CLEAR_VALUE, GL_DEPTH_FUNC, GL_DEPTH_RANGE, GL_DEPTH_SCALE, GL_DEPTH_TEST, GL_DEPTH_WRITEMASK, GL_DITHER, GL_DOUBLEBUFFER, GL_DRAW_BUFFER, GL_EDGE_FLAG, GL_EDGE_FLAG_ARRAY, GL_EDGE_FLAG_ARRAY_STRIDE, GL_FOG, GL_FOG_COLOR, GL_FOG_DENSITY, GL_FOG_END, GL_FOG_HINT, GL_FOG_INDEX, GL_FOG_MODE, GL_FOG_START, GL_FRONT_FACE, GL_GREEN_BIAS, GL_GREEN_BITS, GL_GREEN_SCALE, GL_INDEX_ARRAY, GL_INDEX_ARRAY_STRIDE, GL_INDEX_ARRAY_TYPE, GL_INDEX_BITS, GL_INDEX_CLEAR_VALUE, GL_INDEX_LOGIC_OP, GL_INDEX_MODE, GL_INDEX_OFFSET, GL_INDEX_SHIFT, GL_INDEX_WRITEMASK, GL_LIGHTING, GL_LIGHT_MODEL_AMBIENT, GL_LIGHT_MODEL_LOCAL_VIEWER, GL_LIGHT_MODEL_TWO_SIDE, GL_LIGHTi, GL_LINE_SMOOTH, GL_LINE_SMOOTH_HINT, GL_LINE_STIPPLE, GL_LINE_STIPPLE_PATTERN, GL_LINE_STIPPLE_REPEAT, GL_LINE_WIDTH, GL_LINE_WIDTH_GRANULARITY, GL_LINE_WIDTH_RANGE, GL_LIST_BASE, GL_LIST_INDEX, GL_LIST_MODE, GL_LOGIC_OP, GL_LOGIC_OP_MODE, GL_MAP1_COLOR_4, GL_MAP1_GRID_DOMAIN, GL_MAP1_GRID_SEGMENTS, GL_MAP1_INDEX, GL_MAP1_NORMAL, GL_MAP1_TEXTURE_COORD_1, GL_MAP1_TEXTURE_COORD_2, GL_MAP1_TEXTURE_COORD_3, GL_MAP1_TEXTURE_COORD_4, GL_MAP1_VERTEX_3, GL_MAP1_VERTEX_4, GL_MAP2_COLOR_4, GL_MAP2_GRID_DOMAIN, GL_MAP2_GRID_SEGMENTS, GL_MAP2_INDEX, GL_MAP2_NORMAL, GL_MAP2_TEXTURE_COORD_1, GL_MAP2_TEXTURE_COORD_2, GL_MAP2_TEXTURE_COORD_3, GL_MAP2_TEXTURE_COORD_4, GL_MAP2_VERTEX_3, GL_MAP2_VERTEX_4, GL_MAP_COLOR, GL_MAP_STENCIL, GL_MATRIX_MODE, GL_MAX_ATTRIB_STACK_DEPTH, GL_MAX_CLIENT_ATTRIB_STACK_DEPTH, GL_MAX_CLIP_PLANES, GL_MAX_EVAL_ORDER, GL_MAX_LIGHTS, GL_MAX_LIST_NESTING, GL_MAX_MODELVIEW_STACK_DEPTH, GL_MAX_NAME_STACK_DEPTH, GL_MAX_PIXEL_MAP_TABLE, GL_MAX_PROJECTION_STACK_DEPTH, GL_MAX_TEXTURE_SIZE, GL_MAX_TEXTURE_STACK_DEPTH, GL_MAX_VIEWPORT_DIMS, GL_MODELVIEW_MATRIX, GL_MODELVIEW_STACK_DEPTH, GL_NAME_STACK_DEPTH, GL_NORMALIZE, GL_NORMAL_ARRAY, GL_NORMAL_ARRAY_STRIDE, GL_NORMAL_ARRAY_TYPE, GL_PACK_ALIGNMENT, GL_PACK_LSB_FIRST, GL_PACK_ROW_LENGTH, GL_PACK_SKIP_PIXELS, GL_PACK_SKIP_ROWS, GL_PACK_SWAP_BYTES, GL_PERSPECTIVE_CORRECTION_HINT, GL_PIXEL_MAP_A_TO_A_SIZE, GL_PIXEL_MAP_B_TO_B_SIZE, GL_PIXEL_MAP_G_TO_G_SIZE, GL_PIXEL_MAP_I_TO_A_SIZE, GL_PIXEL_MAP_I_TO_B_SIZE, GL_PIXEL_MAP_I_TO_G_SIZE, GL_PIXEL_MAP_I_TO_I_SIZE, GL_PIXEL_MAP_I_TO_R_SIZE, GL_PIXEL_MAP_R_TO_R_SIZE, GL_PIXEL_MAP_S_TO_S_SIZE, GL_POINT_SIZE, GL_POINT_SIZE_GRANULARITY, GL_POINT_SIZE_RANGE, GL_POINT_SMOOTH, GL_POINT_SMOOTH_HINT, GL_POLYGON_MODE, GL_POLYGON_OFFSET_FACTOR, GL_POLYGON_OFFSET_FILL, GL_POLYGON_OFFSET_LINE, GL_POLYGON_OFFSET_POINT, GL_POLYGON_OFFSET_UNITS, GL_POLYGON_SMOOTH, GL_POLYGON_SMOOTH_HINT, GL_POLYGON_STIPPLE, GL_PROJECTION_MATRIX, GL_PROJECTION_STACK_DEPTH, GL_READ_BUFFER, GL_RED_BIAS, GL_RED_BITS, GL_RED_SCALE, GL_RENDER_MODE, GL_RGBA_MODE, GL_SCISSOR_BOX, GL_SCISSOR_TEST, GL_SHADE_MODEL, GL_STENCIL_BITS, GL_STENCIL_CLEAR_VALUE, GL_STENCIL_FAIL, GL_STENCIL_FUNC, GL_STENCIL_PASS_DEPTH_FAIL, GL_STENCIL_PASS_DEPTH_PASS, GL_STENCIL_REF, GL_STENCIL_TEST, GL_STENCIL_VALUE_MASK, GL_STENCIL_WRITEMASK, GL_STEREO, GL_SUBPIXEL_BITS, GL_TEXTURE_1D, GL_TEXTURE_2D, GL_TEXTURE_COORD_ARRAY, GL_TEXTURE_COORD_ARRAY_SIZE, GL_TEXTURE_COORD_ARRAY_STRIDE, GL_TEXTURE_COORD_ARRAY_TYPE, GL_TEXTURE_ENV_COLOR, GL_TEXTURE_ENV_MODE, GL_TEXTURE_GEN_Q, GL_TEXTURE_GEN_R, GL_TEXTURE_GEN_S, GL_TEXTURE_GEN_T, GL_TEXTURE_MATRIX, GL_TEXTURE_STACK_DEPTH, GL_UNPACK_ALIGNMENT, GL_UNPACK_LSB_FIRST, GL_UNPACK_ROW_LENGTH, GL_UNPACK_SKIP_PIXELS, GL_UNPACK_SKIP_ROWS, GL_UNPACK_SWAP_BYTES, GL_VERTEX_ARRAY, GL_VERTEX_ARRAY_SIZE, GL_VERTEX_ARRAY_STRIDE, GL_VERTEX_ARRAY_TYPE, GL_VIEWPORT, GL_ZOOM_X, GL_ZOOM_Y, gl/glGetFloatv, glGetFloatv, glGetFloatv function [OpenGL], opengl.glgetfloatv
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
-	glGetFloatv
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glGetFloatv function


## -description


The <b>glGetFloatv</b> function returns the value or values of a selected parameter.


## -parameters




### -param pname

The parameter value to be returned. The following symbolic constants are accepted.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GL_ACCUM_ALPHA_BITS"></a><a id="gl_accum_alpha_bits"></a><dl>
<dt><b>GL_ACCUM_ALPHA_BITS</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the number of alpha bitplanes in the accumulation buffer.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_ACCUM_BLUE_BITS"></a><a id="gl_accum_blue_bits"></a><dl>
<dt><b>GL_ACCUM_BLUE_BITS</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the number of blue bitplanes in the accumulation buffer.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_ACCUM_CLEAR_VALUE"></a><a id="gl_accum_clear_value"></a><dl>
<dt><b>GL_ACCUM_CLEAR_VALUE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns four values: the red, green, blue, and alpha values used to clear the accumulation buffer. Integer values, if requested, are linearly mapped from the internal floating-point representation such that 1.0 returns the most positive representable integer value, and -1.0 returns the most negative representable integer value. See <a href="https://msdn.microsoft.com/77d8f340-be47-43f4-96fc-31025a4c8b4e">glClearAccum</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_ACCUM_GREEN_BITS"></a><a id="gl_accum_green_bits"></a><dl>
<dt><b>GL_ACCUM_GREEN_BITS</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the number of green bitplanes in the accumulation buffer.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_ACCUM_RED_BITS"></a><a id="gl_accum_red_bits"></a><dl>
<dt><b>GL_ACCUM_RED_BITS</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the number of red bitplanes in the accumulation buffer.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_ALPHA_BIAS"></a><a id="gl_alpha_bias"></a><dl>
<dt><b>GL_ALPHA_BIAS</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the alpha bias factor used during pixel transfers. See <a href="https://msdn.microsoft.com/c14349c0-ff50-441f-b9fd-8b0f5114fd8a">glPixelTransfer</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_ALPHA_BITS"></a><a id="gl_alpha_bits"></a><dl>
<dt><b>GL_ALPHA_BITS</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the number of alpha bitplanes in each color buffer.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_ALPHA_SCALE"></a><a id="gl_alpha_scale"></a><dl>
<dt><b>GL_ALPHA_SCALE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the alpha scale factor used during pixel transfers. See <a href="https://msdn.microsoft.com/c14349c0-ff50-441f-b9fd-8b0f5114fd8a">glPixelTransfer</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_ALPHA_TEST"></a><a id="gl_alpha_test"></a><dl>
<dt><b>GL_ALPHA_TEST</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether alpha testing of fragments is enabled. See <a href="https://msdn.microsoft.com/6c0c06b5-1bad-4590-a262-f134f63f0936">glAlphaFunc</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_ALPHA_TEST_FUNC"></a><a id="gl_alpha_test_func"></a><dl>
<dt><b>GL_ALPHA_TEST_FUNC</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the symbolic name of the alpha test function. See <a href="https://msdn.microsoft.com/6c0c06b5-1bad-4590-a262-f134f63f0936">glAlphaFunc</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_ALPHA_TEST_REF"></a><a id="gl_alpha_test_ref"></a><dl>
<dt><b>GL_ALPHA_TEST_REF</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the reference value for the alpha test. See <a href="https://msdn.microsoft.com/6c0c06b5-1bad-4590-a262-f134f63f0936">glAlphaFunc</a>. An integer value, if requested, is linearly mapped from the internal floating-point representation such that 1.0 returns the most positive representable integer value, and -1.0 returns the most negative representable integer value.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_ATTRIB_STACK_DEPTH"></a><a id="gl_attrib_stack_depth"></a><dl>
<dt><b>GL_ATTRIB_STACK_DEPTH</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the depth of the attribute stack. If the stack is empty, zero is returned. See <a href="https://msdn.microsoft.com/3c7b93cc-2112-4771-b422-a244821447e5">glPushAttrib</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_AUTO_NORMAL"></a><a id="gl_auto_normal"></a><dl>
<dt><b>GL_AUTO_NORMAL</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether 2-D map evaluation automatically generates surface normals. See <a href="https://msdn.microsoft.com/8365a9bd-156b-4f57-8ceb-1edcbcea9eb4">glMap2</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_AUX_BUFFERS"></a><a id="gl_aux_buffers"></a><dl>
<dt><b>GL_AUX_BUFFERS</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the number of auxiliary color buffers.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_BLEND"></a><a id="gl_blend"></a><dl>
<dt><b>GL_BLEND</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether blending is enabled. See <a href="https://msdn.microsoft.com/6756774b-5eef-419a-a653-0b251aed65a0">glBlendFunc</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_BLEND_DST"></a><a id="gl_blend_dst"></a><dl>
<dt><b>GL_BLEND_DST</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the symbolic constant identifying the destination blend function. See <a href="https://msdn.microsoft.com/6756774b-5eef-419a-a653-0b251aed65a0">glBlendFunc</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_BLEND_SRC"></a><a id="gl_blend_src"></a><dl>
<dt><b>GL_BLEND_SRC</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the symbolic constant identifying the source blend function. See <a href="https://msdn.microsoft.com/6756774b-5eef-419a-a653-0b251aed65a0">glBlendFunc</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_BLUE_BIAS"></a><a id="gl_blue_bias"></a><dl>
<dt><b>GL_BLUE_BIAS</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the blue bias factor used during pixel transfers. See <a href="https://msdn.microsoft.com/c14349c0-ff50-441f-b9fd-8b0f5114fd8a">glPixelTransfer</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_BLUE_BITS"></a><a id="gl_blue_bits"></a><dl>
<dt><b>GL_BLUE_BITS</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the number of blue bitplanes in each color buffer.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_BLUE_SCALE"></a><a id="gl_blue_scale"></a><dl>
<dt><b>GL_BLUE_SCALE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the blue scale factor used during pixel transfers. See <a href="https://msdn.microsoft.com/c14349c0-ff50-441f-b9fd-8b0f5114fd8a">glPixelTransfer</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_CLIENT_ATTRIB_STACK_DEPTH"></a><a id="gl_client_attrib_stack_depth"></a><dl>
<dt><b>GL_CLIENT_ATTRIB_STACK_DEPTH</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value indicating the depth of the attribute stack. The initial value is zero. See <a href="https://msdn.microsoft.com/69f28af6-1023-4546-95ff-169525c23b07">glPushClientAttrib</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_CLIP_PLANEi"></a><a id="gl_clip_planei"></a><a id="GL_CLIP_PLANEI"></a><dl>
<dt><b>GL_CLIP_PLANE<i>i</i></b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether the specified clipping plane is enabled. See <a href="https://msdn.microsoft.com/b70d2c30-7502-4399-8c08-5ec9a2a1919c">glClipPlane</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_COLOR_ARRAY"></a><a id="gl_color_array"></a><dl>
<dt><b>GL_COLOR_ARRAY</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether the specified color array is defined. See <a href="https://msdn.microsoft.com/4d9d05fb-691d-4b71-b079-c42dc7103055">glColorPointer</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_COLOR_ARRAY_SIZE"></a><a id="gl_color_array_size"></a><dl>
<dt><b>GL_COLOR_ARRAY_SIZE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value, the number of components per color in the color array. See <a href="https://msdn.microsoft.com/4d9d05fb-691d-4b71-b079-c42dc7103055">glColorPointer</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_COLOR_ARRAY_STRIDE"></a><a id="gl_color_array_stride"></a><dl>
<dt><b>GL_COLOR_ARRAY_STRIDE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value, the byte offset between consecutive colors in the color array. See <a href="https://msdn.microsoft.com/4d9d05fb-691d-4b71-b079-c42dc7103055">glColorPointer</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_COLOR_ARRAY_TYPE"></a><a id="gl_color_array_type"></a><dl>
<dt><b>GL_COLOR_ARRAY_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value, the data type of each component in the color array. See <a href="https://msdn.microsoft.com/4d9d05fb-691d-4b71-b079-c42dc7103055">glColorPointer</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_COLOR_CLEAR_VALUE"></a><a id="gl_color_clear_value"></a><dl>
<dt><b>GL_COLOR_CLEAR_VALUE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns four values: the red, green, blue, and alpha values used to clear the color buffers. Integer values, if requested, are linearly mapped from the internal floating-point representation such that 1.0 returns the most positive representable integer value, and -1.0 returns the most negative representable integer value. See <a href="https://msdn.microsoft.com/f938e3f4-9db3-4c24-97ae-531b6799224e">glClearColor</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_COLOR_LOGIC_OP"></a><a id="gl_color_logic_op"></a><dl>
<dt><b>GL_COLOR_LOGIC_OP</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether a fragment's RGBA color values are merged into the framebuffer using a logical operation. See <a href="https://msdn.microsoft.com/29edf9bd-f3b8-4de7-9afb-07714f4efd92">glLogicOp</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_COLOR_MATERIAL"></a><a id="gl_color_material"></a><dl>
<dt><b>GL_COLOR_MATERIAL</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether one or more material parameters are tracking the current color. See <a href="https://msdn.microsoft.com/6dbef2c2-f902-4f25-8a87-9e3d710dd807">glColorMaterial</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_COLOR_MATERIAL_FACE"></a><a id="gl_color_material_face"></a><dl>
<dt><b>GL_COLOR_MATERIAL_FACE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: a symbolic constant indicating which materials have a parameter that is tracking the current color. See <a href="https://msdn.microsoft.com/6dbef2c2-f902-4f25-8a87-9e3d710dd807">glColorMaterial</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_COLOR_MATERIAL_PARAMETER"></a><a id="gl_color_material_parameter"></a><dl>
<dt><b>GL_COLOR_MATERIAL_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: a symbolic constant indicating which material parameters are tracking the current color. See <a href="https://msdn.microsoft.com/6dbef2c2-f902-4f25-8a87-9e3d710dd807">glColorMaterial</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_COLOR_WRITEMASK"></a><a id="gl_color_writemask"></a><dl>
<dt><b>GL_COLOR_WRITEMASK</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns four Boolean values: the red, green, blue, and alpha write enables for the color buffers. See <a href="https://msdn.microsoft.com/23d7f94e-f290-423c-a841-f86caf94009d">glColorMask</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_CULL_FACE"></a><a id="gl_cull_face"></a><dl>
<dt><b>GL_CULL_FACE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether polygon culling is enabled. See <a href="https://msdn.microsoft.com/53bf05b5-a68b-4d96-b4e7-2878a0a86a13">glCullFace</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_CULL_FACE_MODE"></a><a id="gl_cull_face_mode"></a><dl>
<dt><b>GL_CULL_FACE_MODE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: a symbolic constant indicating which polygon faces are to be culled. See <a href="https://msdn.microsoft.com/53bf05b5-a68b-4d96-b4e7-2878a0a86a13">glCullFace</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_CURRENT_COLOR"></a><a id="gl_current_color"></a><dl>
<dt><b>GL_CURRENT_COLOR</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns four values: the red, green, blue, and alpha values of the current color. Integer values, if requested, are linearly mapped from the internal floating-point representation such that 1.0 returns the most positive representable integer value, and -1.0 returns the most negative representable integer value. See <a href="https://msdn.microsoft.com/916eb8b5-65c2-4523-bdb5-e609ad7a24a0">glColor</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_CURRENT_INDEX"></a><a id="gl_current_index"></a><dl>
<dt><b>GL_CURRENT_INDEX</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the current color index. See <a href="https://msdn.microsoft.com/239c2e5d-cd87-4c2e-8fa1-7c71a32d4350">glIndex</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_CURRENT_NORMAL"></a><a id="gl_current_normal"></a><dl>
<dt><b>GL_CURRENT_NORMAL</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns three values: the <i>x</i>, <i>y</i>, and <i>z</i> values of the current normal. Integer values, if requested, are linearly mapped from the internal floating-point representation such that 1.0 returns the most positive representable integer value, and -1.0 returns the most negative representable integer value. See <a href="https://msdn.microsoft.com/e90bfed4-ab72-43d2-b7b5-37a9fd6ecb4c">glNormal</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_CURRENT_RASTER_COLOR"></a><a id="gl_current_raster_color"></a><dl>
<dt><b>GL_CURRENT_RASTER_COLOR</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns four values: the red, green, blue, and alpha values of the current raster position. Integer values, if requested, are linearly mapped from the internal floating-point representation such that 1.0 returns the most positive representable integer value, and -1.0 returns the most negative representable integer value. See <a href="https://msdn.microsoft.com/2a661893-0818-441d-9399-0103560737c3">glRasterPos</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_CURRENT_RASTER_DISTANCE"></a><a id="gl_current_raster_distance"></a><dl>
<dt><b>GL_CURRENT_RASTER_DISTANCE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the distance from the eye to the current raster position. See <a href="https://msdn.microsoft.com/2a661893-0818-441d-9399-0103560737c3">glRasterPos</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_CURRENT_RASTER_INDEX"></a><a id="gl_current_raster_index"></a><dl>
<dt><b>GL_CURRENT_RASTER_INDEX</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the color index of the current raster position. See <a href="https://msdn.microsoft.com/2a661893-0818-441d-9399-0103560737c3">glRasterPos</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_CURRENT_RASTER_POSITION"></a><a id="gl_current_raster_position"></a><dl>
<dt><b>GL_CURRENT_RASTER_POSITION</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns four values: the <i>x</i>, <i>y</i>, <i>z</i>, and <i>w</i> components of the current raster position. The <i>x</i>, <i>y</i>, and <i>z</i> components are in window coordinates, and <i>w</i> is in clip coordinates. See <a href="https://msdn.microsoft.com/2a661893-0818-441d-9399-0103560737c3">glRasterPos</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_CURRENT_RASTER_POSITION_VALID"></a><a id="gl_current_raster_position_valid"></a><dl>
<dt><b>GL_CURRENT_RASTER_POSITION_VALID</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether the current raster position is valid. See <a href="https://msdn.microsoft.com/2a661893-0818-441d-9399-0103560737c3">glRasterPos</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_CURRENT_RASTER_TEXTURE_COORDS"></a><a id="gl_current_raster_texture_coords"></a><dl>
<dt><b>GL_CURRENT_RASTER_TEXTURE_COORDS</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns four values: the <i>s</i>, <i>t</i>, <i>r</i>, and <i>q</i> current raster texture coordinates. See <a href="https://msdn.microsoft.com/2a661893-0818-441d-9399-0103560737c3">glRasterPos</a> and <a href="https://msdn.microsoft.com/71eb39f1-e1ad-4b97-83e0-d2670f5a7545">glTexCoord</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_CURRENT_TEXTURE_COORDS"></a><a id="gl_current_texture_coords"></a><dl>
<dt><b>GL_CURRENT_TEXTURE_COORDS</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns four values: the <i>s</i>, <i>t</i>, <i>r</i>, and <i>q</i> current texture coordinates. See <a href="https://msdn.microsoft.com/71eb39f1-e1ad-4b97-83e0-d2670f5a7545">glTexCoord</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_DEPTH_BIAS"></a><a id="gl_depth_bias"></a><dl>
<dt><b>GL_DEPTH_BIAS</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the depth bias factor used during pixel transfers. See <a href="https://msdn.microsoft.com/c14349c0-ff50-441f-b9fd-8b0f5114fd8a">glPixelTransfer</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_DEPTH_BITS"></a><a id="gl_depth_bits"></a><dl>
<dt><b>GL_DEPTH_BITS</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the number of bitplanes in the depth buffer.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_DEPTH_CLEAR_VALUE"></a><a id="gl_depth_clear_value"></a><dl>
<dt><b>GL_DEPTH_CLEAR_VALUE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the value that is used to clear the depth buffer. Integer values, if requested, are linearly mapped from the internal floating-point representation such that 1.0 returns the most positive representable integer value, and -1.0 returns the most negative representable integer value. See <a href="https://msdn.microsoft.com/8e26ae78-edc1-4201-a0db-d5bc8ae6dc82">glClearDepth</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_DEPTH_FUNC"></a><a id="gl_depth_func"></a><dl>
<dt><b>GL_DEPTH_FUNC</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the symbolic constant that indicates the depth comparison function. See <a href="https://msdn.microsoft.com/6ab8774a-8887-4c1e-b567-4492c0a60cf2">glDepthFunc</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_DEPTH_RANGE"></a><a id="gl_depth_range"></a><dl>
<dt><b>GL_DEPTH_RANGE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns two values: the near and far mapping limits for the depth buffer. Integer values, if requested, are linearly mapped from the internal floating-point representation such that 1.0 returns the most positive representable integer value, and -1.0 returns the most negative representable integer value. See <a href="https://msdn.microsoft.com/44aed5e5-4bd2-4e7f-ad05-1cf4be5254a5">glDepthRange</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_DEPTH_SCALE"></a><a id="gl_depth_scale"></a><dl>
<dt><b>GL_DEPTH_SCALE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the depth scale factor used during pixel transfers. See <a href="https://msdn.microsoft.com/c14349c0-ff50-441f-b9fd-8b0f5114fd8a">glPixelTransfer</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_DEPTH_TEST"></a><a id="gl_depth_test"></a><dl>
<dt><b>GL_DEPTH_TEST</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether depth testing of fragments is enabled. See <a href="https://msdn.microsoft.com/6ab8774a-8887-4c1e-b567-4492c0a60cf2">glDepthFunc</a> and <a href="https://msdn.microsoft.com/44aed5e5-4bd2-4e7f-ad05-1cf4be5254a5">glDepthRange</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_DEPTH_WRITEMASK"></a><a id="gl_depth_writemask"></a><dl>
<dt><b>GL_DEPTH_WRITEMASK</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating if the depth buffer is enabled for writing. See <a href="https://msdn.microsoft.com/067b18e2-f21a-4dde-8fa6-dd975746e189">glDepthMask</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_DITHER"></a><a id="gl_dither"></a><dl>
<dt><b>GL_DITHER</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether dithering of fragment colors and indexes is enabled.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_DOUBLEBUFFER"></a><a id="gl_doublebuffer"></a><dl>
<dt><b>GL_DOUBLEBUFFER</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether double buffering is supported.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_DRAW_BUFFER"></a><a id="gl_draw_buffer"></a><dl>
<dt><b>GL_DRAW_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: a symbolic constant indicating which buffers are being drawn to. See <a href="https://msdn.microsoft.com/ea625699-303b-4e60-b9aa-771949a8d52d">glDrawBuffer</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_EDGE_FLAG"></a><a id="gl_edge_flag"></a><dl>
<dt><b>GL_EDGE_FLAG</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether the current edge flag is true or false. See <a href="https://msdn.microsoft.com/26e4e901-4d91-4d7c-ad07-b4480062a4cb">glEdgeFlag</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_EDGE_FLAG_ARRAY"></a><a id="gl_edge_flag_array"></a><dl>
<dt><b>GL_EDGE_FLAG_ARRAY</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether the edge flag array is enabled. See <a href="https://msdn.microsoft.com/e0e7e442-533d-4c41-addd-a215ce0b1c56">glEdgeFlagPointer</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_EDGE_FLAG_ARRAY_STRIDE"></a><a id="gl_edge_flag_array_stride"></a><dl>
<dt><b>GL_EDGE_FLAG_ARRAY_STRIDE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value, the byte offset between consecutive edge flags in the edge flag array. See <a href="https://msdn.microsoft.com/e0e7e442-533d-4c41-addd-a215ce0b1c56">glEdgeFlagPointer</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_FOG"></a><a id="gl_fog"></a><dl>
<dt><b>GL_FOG</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether fogging is enabled. See <a href="https://msdn.microsoft.com/019c2006-679a-4611-8156-f6665d3ef5b2">glFog</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_FOG_COLOR"></a><a id="gl_fog_color"></a><dl>
<dt><b>GL_FOG_COLOR</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns four values: the red, green, blue, and alpha components of the fog color. Integer values, if requested, are linearly mapped from the internal floating-point representation such that 1.0 returns the most positive representable integer value, and -1.0 returns the most negative representable integer value. See <a href="https://msdn.microsoft.com/019c2006-679a-4611-8156-f6665d3ef5b2">glFog</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_FOG_DENSITY"></a><a id="gl_fog_density"></a><dl>
<dt><b>GL_FOG_DENSITY</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the fog density parameter. See <a href="https://msdn.microsoft.com/019c2006-679a-4611-8156-f6665d3ef5b2">glFog</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_FOG_END"></a><a id="gl_fog_end"></a><dl>
<dt><b>GL_FOG_END</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the end factor for the linear fog equation. See <a href="https://msdn.microsoft.com/019c2006-679a-4611-8156-f6665d3ef5b2">glFog</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_FOG_HINT"></a><a id="gl_fog_hint"></a><dl>
<dt><b>GL_FOG_HINT</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: a symbolic constant indicating the mode of the fog hint. See <a href="https://msdn.microsoft.com/6d03e107-321a-45ee-9ce7-25fa9cab32d9">glHint</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_FOG_INDEX"></a><a id="gl_fog_index"></a><dl>
<dt><b>GL_FOG_INDEX</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the fog color index. See <a href="https://msdn.microsoft.com/019c2006-679a-4611-8156-f6665d3ef5b2">glFog</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_FOG_MODE"></a><a id="gl_fog_mode"></a><dl>
<dt><b>GL_FOG_MODE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: a symbolic constant indicating which fog equation is selected. See <a href="https://msdn.microsoft.com/019c2006-679a-4611-8156-f6665d3ef5b2">glFog</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_FOG_START"></a><a id="gl_fog_start"></a><dl>
<dt><b>GL_FOG_START</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the start factor for the linear fog equation. See <a href="https://msdn.microsoft.com/019c2006-679a-4611-8156-f6665d3ef5b2">glFog</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_FRONT_FACE"></a><a id="gl_front_face"></a><dl>
<dt><b>GL_FRONT_FACE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: a symbolic constant indicating whether clockwise or counterclockwise polygon winding is treated as front-facing. See <a href="https://msdn.microsoft.com/4087107c-99cd-4c26-92e3-8dc43633d51f">glFrontFace</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_GREEN_BIAS"></a><a id="gl_green_bias"></a><dl>
<dt><b>GL_GREEN_BIAS</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the green bias factor used during pixel transfers.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_GREEN_BITS"></a><a id="gl_green_bits"></a><dl>
<dt><b>GL_GREEN_BITS</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the number of green bitplanes in each color buffer.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_GREEN_SCALE"></a><a id="gl_green_scale"></a><dl>
<dt><b>GL_GREEN_SCALE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the green scale factor used during pixel transfers. See <a href="https://msdn.microsoft.com/c14349c0-ff50-441f-b9fd-8b0f5114fd8a">glPixelTransfer</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_INDEX_ARRAY"></a><a id="gl_index_array"></a><dl>
<dt><b>GL_INDEX_ARRAY</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether the color index array is enabled. See <a href="https://msdn.microsoft.com/b435d950-1f87-4041-93e4-f1f8786cabdb">glIndexPointer</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_INDEX_ARRAY_STRIDE"></a><a id="gl_index_array_stride"></a><dl>
<dt><b>GL_INDEX_ARRAY_STRIDE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value, the byte offset between consecutive color indexes in the color index array. See <a href="https://msdn.microsoft.com/b435d950-1f87-4041-93e4-f1f8786cabdb">glIndexPointer</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_INDEX_ARRAY_TYPE"></a><a id="gl_index_array_type"></a><dl>
<dt><b>GL_INDEX_ARRAY_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value, the data type of indexes in the color index array. The initial value is GL_FLOAT. See <a href="https://msdn.microsoft.com/b435d950-1f87-4041-93e4-f1f8786cabdb">glIndexPointer</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_INDEX_BITS"></a><a id="gl_index_bits"></a><dl>
<dt><b>GL_INDEX_BITS</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the number of bitplanes in each color-index buffer.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_INDEX_CLEAR_VALUE"></a><a id="gl_index_clear_value"></a><dl>
<dt><b>GL_INDEX_CLEAR_VALUE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the color index used to clear the color-index buffers. See <a href="https://msdn.microsoft.com/87983d93-c5a1-445f-8621-1c2952d93a0f">glClearIndex</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_INDEX_LOGIC_OP"></a><a id="gl_index_logic_op"></a><dl>
<dt><b>GL_INDEX_LOGIC_OP</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether a fragment's index values are merged into the framebuffer using a logical operation. See <a href="https://msdn.microsoft.com/29edf9bd-f3b8-4de7-9afb-07714f4efd92">glLogicOp</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_INDEX_MODE"></a><a id="gl_index_mode"></a><dl>
<dt><b>GL_INDEX_MODE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether OpenGL is in color-index mode (TRUE) or RGBA mode (FALSE).

</td>
</tr>
<tr>
<td width="40%"><a id="GL_INDEX_OFFSET"></a><a id="gl_index_offset"></a><dl>
<dt><b>GL_INDEX_OFFSET</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the offset added to color and stencil indexes during pixel transfers. See <a href="https://msdn.microsoft.com/c14349c0-ff50-441f-b9fd-8b0f5114fd8a">glPixelTransfer</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_INDEX_SHIFT"></a><a id="gl_index_shift"></a><dl>
<dt><b>GL_INDEX_SHIFT</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the amount that color and stencil indexes are shifted during pixel transfers. See <a href="https://msdn.microsoft.com/c14349c0-ff50-441f-b9fd-8b0f5114fd8a">glPixelTransfer</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_INDEX_WRITEMASK"></a><a id="gl_index_writemask"></a><dl>
<dt><b>GL_INDEX_WRITEMASK</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: a mask indicating which bitplanes of each color-index buffer can be written. See <a href="https://msdn.microsoft.com/f4b5df36-390f-4254-95fb-98589750a11b">glIndexMask</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_LIGHTi"></a><a id="gl_lighti"></a><a id="GL_LIGHTI"></a><dl>
<dt><b>GL_LIGHT<i>i</i></b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether the specified light is enabled. See <a href="https://msdn.microsoft.com/004f0f53-4c72-48df-8231-6b39df464061">glLight</a> and <a href="https://msdn.microsoft.com/8214765c-5722-4df0-88ed-3a5ac039aac4">glLightModel</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_LIGHTING"></a><a id="gl_lighting"></a><dl>
<dt><b>GL_LIGHTING</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether lighting is enabled. See <a href="https://msdn.microsoft.com/8214765c-5722-4df0-88ed-3a5ac039aac4">glLightModel</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_LIGHT_MODEL_AMBIENT"></a><a id="gl_light_model_ambient"></a><dl>
<dt><b>GL_LIGHT_MODEL_AMBIENT</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns four values: the red, green, blue, and alpha components of the ambient intensity of the entire scene. Integer values, if requested, are linearly mapped from the internal floating-point representation such that 1.0 returns the most positive representable integer value, and -1.0 returns the most negative representable integer value. See <a href="https://msdn.microsoft.com/8214765c-5722-4df0-88ed-3a5ac039aac4">glLightModel</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_LIGHT_MODEL_LOCAL_VIEWER"></a><a id="gl_light_model_local_viewer"></a><dl>
<dt><b>GL_LIGHT_MODEL_LOCAL_VIEWER</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether specular reflection calculations treat the viewer as being local to the scene. See <a href="https://msdn.microsoft.com/8214765c-5722-4df0-88ed-3a5ac039aac4">glLightModel</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_LIGHT_MODEL_TWO_SIDE"></a><a id="gl_light_model_two_side"></a><dl>
<dt><b>GL_LIGHT_MODEL_TWO_SIDE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether separate materials are used to compute lighting for front-facing and back-facing polygons. See <a href="https://msdn.microsoft.com/8214765c-5722-4df0-88ed-3a5ac039aac4">glLightModel</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_LINE_SMOOTH"></a><a id="gl_line_smooth"></a><dl>
<dt><b>GL_LINE_SMOOTH</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether antialiasing of lines is enabled. See <a href="https://msdn.microsoft.com/13a69fd7-5eee-42ec-bd05-5bd3c838d4d7">glLineWidth</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_LINE_SMOOTH_HINT"></a><a id="gl_line_smooth_hint"></a><dl>
<dt><b>GL_LINE_SMOOTH_HINT</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: a symbolic constant indicating the mode of the line antialiasing hint. See <a href="https://msdn.microsoft.com/6d03e107-321a-45ee-9ce7-25fa9cab32d9">glHint</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_LINE_STIPPLE"></a><a id="gl_line_stipple"></a><dl>
<dt><b>GL_LINE_STIPPLE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether stippling of lines is enabled. See <a href="https://msdn.microsoft.com/256d968c-9e72-4aec-9faf-afe70f1087a8">glLineStipple</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_LINE_STIPPLE_PATTERN"></a><a id="gl_line_stipple_pattern"></a><dl>
<dt><b>GL_LINE_STIPPLE_PATTERN</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the 16-bit line stipple pattern. See <a href="https://msdn.microsoft.com/256d968c-9e72-4aec-9faf-afe70f1087a8">glLineStipple</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_LINE_STIPPLE_REPEAT"></a><a id="gl_line_stipple_repeat"></a><dl>
<dt><b>GL_LINE_STIPPLE_REPEAT</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the line stipple repeat factor. See <a href="https://msdn.microsoft.com/256d968c-9e72-4aec-9faf-afe70f1087a8">glLineStipple</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_LINE_WIDTH"></a><a id="gl_line_width"></a><dl>
<dt><b>GL_LINE_WIDTH</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the line width as specified with <a href="https://msdn.microsoft.com/13a69fd7-5eee-42ec-bd05-5bd3c838d4d7">glLineWidth</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_LINE_WIDTH_GRANULARITY"></a><a id="gl_line_width_granularity"></a><dl>
<dt><b>GL_LINE_WIDTH_GRANULARITY</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the width difference between adjacent supported widths for antialiased lines. See <a href="https://msdn.microsoft.com/13a69fd7-5eee-42ec-bd05-5bd3c838d4d7">glLineWidth</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_LINE_WIDTH_RANGE"></a><a id="gl_line_width_range"></a><dl>
<dt><b>GL_LINE_WIDTH_RANGE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns two values: the smallest and largest supported widths for antialiased lines. See <a href="https://msdn.microsoft.com/13a69fd7-5eee-42ec-bd05-5bd3c838d4d7">glLineWidth</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_LIST_BASE"></a><a id="gl_list_base"></a><dl>
<dt><b>GL_LIST_BASE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the base offset added to all names in arrays presented to <a href="https://msdn.microsoft.com/7c0a00df-91ee-44ad-9e02-97c1b078e87f">glCallLists</a>. See <a href="https://msdn.microsoft.com/df82f699-b2af-471a-83f3-5620857ba45d">glListBase</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_LIST_INDEX"></a><a id="gl_list_index"></a><dl>
<dt><b>GL_LIST_INDEX</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the name of the display list currently under construction. Zero is returned if no display list is currently under construction. See <a href="https://msdn.microsoft.com/9c6556d4-855f-4cba-94cc-27b5f1e4607a">glNewList</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_LIST_MODE"></a><a id="gl_list_mode"></a><dl>
<dt><b>GL_LIST_MODE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: a symbolic constant indicating the construction mode of the display list currently being constructed. See <a href="https://msdn.microsoft.com/9c6556d4-855f-4cba-94cc-27b5f1e4607a">glNewList</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_LOGIC_OP"></a><a id="gl_logic_op"></a><dl>
<dt><b>GL_LOGIC_OP</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether fragment indexes are merged into the framebuffer using a logical operation. See <a href="https://msdn.microsoft.com/29edf9bd-f3b8-4de7-9afb-07714f4efd92">glLogicOp</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_LOGIC_OP_MODE"></a><a id="gl_logic_op_mode"></a><dl>
<dt><b>GL_LOGIC_OP_MODE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: a symbolic constant indicating the selected logic operational mode. See <a href="https://msdn.microsoft.com/29edf9bd-f3b8-4de7-9afb-07714f4efd92">glLogicOp</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_MAP1_COLOR_4"></a><a id="gl_map1_color_4"></a><dl>
<dt><b>GL_MAP1_COLOR_4</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether 1-D evaluation generates colors. See <a href="https://msdn.microsoft.com/47b0bd46-aa79-4146-8503-cddcc8b7b242">glMap1</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_MAP1_GRID_DOMAIN"></a><a id="gl_map1_grid_domain"></a><dl>
<dt><b>GL_MAP1_GRID_DOMAIN</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns two values: the endpoints of the 1-D maps grid domain. See <a href="https://msdn.microsoft.com/87532b49-a506-44a7-be2f-b74c289f1a19">glMapGrid</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_MAP1_GRID_SEGMENTS"></a><a id="gl_map1_grid_segments"></a><dl>
<dt><b>GL_MAP1_GRID_SEGMENTS</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the number of partitions in the 1-D maps grid domain. See <a href="https://msdn.microsoft.com/87532b49-a506-44a7-be2f-b74c289f1a19">glMapGrid</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_MAP1_INDEX"></a><a id="gl_map1_index"></a><dl>
<dt><b>GL_MAP1_INDEX</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether 1-D evaluation generates color indexes. See <a href="https://msdn.microsoft.com/47b0bd46-aa79-4146-8503-cddcc8b7b242">glMap1</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_MAP1_NORMAL"></a><a id="gl_map1_normal"></a><dl>
<dt><b>GL_MAP1_NORMAL</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether 1-D evaluation generates normals. See <a href="https://msdn.microsoft.com/47b0bd46-aa79-4146-8503-cddcc8b7b242">glMap1</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_MAP1_TEXTURE_COORD_1"></a><a id="gl_map1_texture_coord_1"></a><dl>
<dt><b>GL_MAP1_TEXTURE_COORD_1</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether 1-D evaluation generates 1-D texture coordinates. See <a href="https://msdn.microsoft.com/47b0bd46-aa79-4146-8503-cddcc8b7b242">glMap1</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_MAP1_TEXTURE_COORD_2"></a><a id="gl_map1_texture_coord_2"></a><dl>
<dt><b>GL_MAP1_TEXTURE_COORD_2</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether 1-D evaluation generates 2-D texture coordinates. See <a href="https://msdn.microsoft.com/47b0bd46-aa79-4146-8503-cddcc8b7b242">glMap1</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_MAP1_TEXTURE_COORD_3"></a><a id="gl_map1_texture_coord_3"></a><dl>
<dt><b>GL_MAP1_TEXTURE_COORD_3</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether 1-D evaluation generates 3-D texture coordinates. See <a href="https://msdn.microsoft.com/47b0bd46-aa79-4146-8503-cddcc8b7b242">glMap1</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_MAP1_TEXTURE_COORD_4"></a><a id="gl_map1_texture_coord_4"></a><dl>
<dt><b>GL_MAP1_TEXTURE_COORD_4</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether 1-D evaluation generates 4-D texture coordinates. See <a href="https://msdn.microsoft.com/47b0bd46-aa79-4146-8503-cddcc8b7b242">glMap1</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_MAP1_VERTEX_3"></a><a id="gl_map1_vertex_3"></a><dl>
<dt><b>GL_MAP1_VERTEX_3</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether 1-D evaluation generates 3-D vertex coordinates. See <a href="https://msdn.microsoft.com/47b0bd46-aa79-4146-8503-cddcc8b7b242">glMap1</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_MAP1_VERTEX_4"></a><a id="gl_map1_vertex_4"></a><dl>
<dt><b>GL_MAP1_VERTEX_4</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether 1-D evaluation generates 4-D vertex coordinates. See <a href="https://msdn.microsoft.com/47b0bd46-aa79-4146-8503-cddcc8b7b242">glMap1</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_MAP2_COLOR_4"></a><a id="gl_map2_color_4"></a><dl>
<dt><b>GL_MAP2_COLOR_4</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether 2-D evaluation generates colors. See <a href="https://msdn.microsoft.com/8365a9bd-156b-4f57-8ceb-1edcbcea9eb4">glMap2</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_MAP2_GRID_DOMAIN"></a><a id="gl_map2_grid_domain"></a><dl>
<dt><b>GL_MAP2_GRID_DOMAIN</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns four values: the endpoints of the 2-D maps <i>i</i> and <i>j</i> grid domains. See <a href="https://msdn.microsoft.com/87532b49-a506-44a7-be2f-b74c289f1a19">glMapGrid</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_MAP2_GRID_SEGMENTS"></a><a id="gl_map2_grid_segments"></a><dl>
<dt><b>GL_MAP2_GRID_SEGMENTS</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns two values: the number of partitions in the 2-D maps <i>i</i> and <i>j</i> grid domains. See <a href="https://msdn.microsoft.com/87532b49-a506-44a7-be2f-b74c289f1a19">glMapGrid</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_MAP2_INDEX"></a><a id="gl_map2_index"></a><dl>
<dt><b>GL_MAP2_INDEX</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether 2-D evaluation generates color indexes. See <a href="https://msdn.microsoft.com/8365a9bd-156b-4f57-8ceb-1edcbcea9eb4">glMap2</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_MAP2_NORMAL"></a><a id="gl_map2_normal"></a><dl>
<dt><b>GL_MAP2_NORMAL</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether 2-D evaluation generates normals. See <a href="https://msdn.microsoft.com/8365a9bd-156b-4f57-8ceb-1edcbcea9eb4">glMap2</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_MAP2_TEXTURE_COORD_1"></a><a id="gl_map2_texture_coord_1"></a><dl>
<dt><b>GL_MAP2_TEXTURE_COORD_1</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether 2-D evaluation generates 1-D texture coordinates. See <a href="https://msdn.microsoft.com/8365a9bd-156b-4f57-8ceb-1edcbcea9eb4">glMap2</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_MAP2_TEXTURE_COORD_2"></a><a id="gl_map2_texture_coord_2"></a><dl>
<dt><b>GL_MAP2_TEXTURE_COORD_2</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether 2-D evaluation generates 2-D texture coordinates. See <a href="https://msdn.microsoft.com/8365a9bd-156b-4f57-8ceb-1edcbcea9eb4">glMap2</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_MAP2_TEXTURE_COORD_3"></a><a id="gl_map2_texture_coord_3"></a><dl>
<dt><b>GL_MAP2_TEXTURE_COORD_3</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether 2-D evaluation generates 3-D texture coordinates. See <a href="https://msdn.microsoft.com/8365a9bd-156b-4f57-8ceb-1edcbcea9eb4">glMap2</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_MAP2_TEXTURE_COORD_4"></a><a id="gl_map2_texture_coord_4"></a><dl>
<dt><b>GL_MAP2_TEXTURE_COORD_4</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether 2-D evaluation generates 4-D texture coordinates. See <a href="https://msdn.microsoft.com/8365a9bd-156b-4f57-8ceb-1edcbcea9eb4">glMap2</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_MAP2_VERTEX_3"></a><a id="gl_map2_vertex_3"></a><dl>
<dt><b>GL_MAP2_VERTEX_3</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether 2-D evaluation generates 3-D vertex coordinates. See <a href="https://msdn.microsoft.com/8365a9bd-156b-4f57-8ceb-1edcbcea9eb4">glMap2</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_MAP2_VERTEX_4"></a><a id="gl_map2_vertex_4"></a><dl>
<dt><b>GL_MAP2_VERTEX_4</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether 2-D evaluation generates 4-D vertex coordinates. See <a href="https://msdn.microsoft.com/8365a9bd-156b-4f57-8ceb-1edcbcea9eb4">glMap2</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_MAP_COLOR"></a><a id="gl_map_color"></a><dl>
<dt><b>GL_MAP_COLOR</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether colors and color indexes are to be replaced by table lookup during pixel transfers. See <a href="https://msdn.microsoft.com/c14349c0-ff50-441f-b9fd-8b0f5114fd8a">glPixelTransfer</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_MAP_STENCIL"></a><a id="gl_map_stencil"></a><dl>
<dt><b>GL_MAP_STENCIL</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether stencil indexes are to be replaced by table lookup during pixel transfers. See <a href="https://msdn.microsoft.com/c14349c0-ff50-441f-b9fd-8b0f5114fd8a">glPixelTransfer</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_MATRIX_MODE"></a><a id="gl_matrix_mode"></a><dl>
<dt><b>GL_MATRIX_MODE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: a symbolic constant indicating which matrix stack is currently the target of all matrix operations. See <a href="https://msdn.microsoft.com/f1006ea3-322a-42a9-b33c-6c7181985ef9">glMatrixMode</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_MAX_CLIENT_ATTRIB_STACK_DEPTH"></a><a id="gl_max_client_attrib_stack_depth"></a><dl>
<dt><b>GL_MAX_CLIENT_ATTRIB_STACK_DEPTH</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value indicating the maximum supported depth of the client attribute stack. See <a href="https://msdn.microsoft.com/69f28af6-1023-4546-95ff-169525c23b07">glPushClientAttrib</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_MAX_ATTRIB_STACK_DEPTH"></a><a id="gl_max_attrib_stack_depth"></a><dl>
<dt><b>GL_MAX_ATTRIB_STACK_DEPTH</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the maximum supported depth of the attribute stack. See <a href="https://msdn.microsoft.com/3c7b93cc-2112-4771-b422-a244821447e5">glPushAttrib</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_MAX_CLIP_PLANES"></a><a id="gl_max_clip_planes"></a><dl>
<dt><b>GL_MAX_CLIP_PLANES</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the maximum number of application-defined clipping planes. See <a href="https://msdn.microsoft.com/b70d2c30-7502-4399-8c08-5ec9a2a1919c">glClipPlane</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_MAX_EVAL_ORDER"></a><a id="gl_max_eval_order"></a><dl>
<dt><b>GL_MAX_EVAL_ORDER</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the maximum equation order supported by 1-D and 2-D evaluators. See <a href="https://msdn.microsoft.com/47b0bd46-aa79-4146-8503-cddcc8b7b242">glMap1</a> and <a href="https://msdn.microsoft.com/8365a9bd-156b-4f57-8ceb-1edcbcea9eb4">glMap2</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_MAX_LIGHTS"></a><a id="gl_max_lights"></a><dl>
<dt><b>GL_MAX_LIGHTS</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the maximum number of lights. See <a href="https://msdn.microsoft.com/004f0f53-4c72-48df-8231-6b39df464061">glLight</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_MAX_LIST_NESTING"></a><a id="gl_max_list_nesting"></a><dl>
<dt><b>GL_MAX_LIST_NESTING</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the maximum recursion depth allowed during display-list traversal. See <a href="https://msdn.microsoft.com/9373d32e-b11e-4a80-8713-da2c1d8d9368">glCallList</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_MAX_MODELVIEW_STACK_DEPTH"></a><a id="gl_max_modelview_stack_depth"></a><dl>
<dt><b>GL_MAX_MODELVIEW_STACK_DEPTH</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the maximum supported depth of the modelview matrix stack. See <a href="https://msdn.microsoft.com/97d8e644-50bb-4130-b6b7-d87df4468e73">glPushMatrix</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_MAX_NAME_STACK_DEPTH"></a><a id="gl_max_name_stack_depth"></a><dl>
<dt><b>GL_MAX_NAME_STACK_DEPTH</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the maximum supported depth of the selection name stack. See <a href="https://msdn.microsoft.com/e4319018-42c0-4567-b67f-31dbdbee9b13">glPushName</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_MAX_PIXEL_MAP_TABLE"></a><a id="gl_max_pixel_map_table"></a><dl>
<dt><b>GL_MAX_PIXEL_MAP_TABLE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the maximum supported size of a <a href="https://msdn.microsoft.com/79a84334-355c-46d3-990c-4d273e2d2207">glPixelMap</a> lookup table.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_MAX_PROJECTION_STACK_DEPTH"></a><a id="gl_max_projection_stack_depth"></a><dl>
<dt><b>GL_MAX_PROJECTION_STACK_DEPTH</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the maximum supported depth of the projection matrix stack. See <a href="https://msdn.microsoft.com/97d8e644-50bb-4130-b6b7-d87df4468e73">glPushMatrix</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_MAX_TEXTURE_SIZE"></a><a id="gl_max_texture_size"></a><dl>
<dt><b>GL_MAX_TEXTURE_SIZE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the maximum width or height of any texture image (without borders). See <a href="https://msdn.microsoft.com/4f537b89-2ea2-4e2e-8c57-c372bf53f12c">glTexImage1D</a> and <a href="https://msdn.microsoft.com/e8b9c692-5239-47de-86eb-80c247c60e1d">glTexImage2D</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_MAX_TEXTURE_STACK_DEPTH"></a><a id="gl_max_texture_stack_depth"></a><dl>
<dt><b>GL_MAX_TEXTURE_STACK_DEPTH</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the maximum supported depth of the texture matrix stack. See <a href="https://msdn.microsoft.com/97d8e644-50bb-4130-b6b7-d87df4468e73">glPushMatrix</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_MAX_VIEWPORT_DIMS"></a><a id="gl_max_viewport_dims"></a><dl>
<dt><b>GL_MAX_VIEWPORT_DIMS</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns two values: the maximum supported width and height of the viewport. See <a href="https://msdn.microsoft.com/11816b2f-ee18-42ef-a782-2e96699dd087">glViewport</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_MODELVIEW_MATRIX"></a><a id="gl_modelview_matrix"></a><dl>
<dt><b>GL_MODELVIEW_MATRIX</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns 16 values: the modelview matrix on the top of the modelview matrix stack. See <a href="https://msdn.microsoft.com/97d8e644-50bb-4130-b6b7-d87df4468e73">glPushMatrix</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_MODELVIEW_STACK_DEPTH"></a><a id="gl_modelview_stack_depth"></a><dl>
<dt><b>GL_MODELVIEW_STACK_DEPTH</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the number of matrices on the modelview matrix stack. See <a href="https://msdn.microsoft.com/97d8e644-50bb-4130-b6b7-d87df4468e73">glPushMatrix</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_NAME_STACK_DEPTH"></a><a id="gl_name_stack_depth"></a><dl>
<dt><b>GL_NAME_STACK_DEPTH</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the number of names on the selection name stack. See <a href="https://msdn.microsoft.com/e4319018-42c0-4567-b67f-31dbdbee9b13">glPushName</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_NORMAL_ARRAY"></a><a id="gl_normal_array"></a><dl>
<dt><b>GL_NORMAL_ARRAY</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value, indicating whether the normal array is enabled. See <a href="https://msdn.microsoft.com/6ffb0522-87cc-4be1-a5b1-f6fd30e04b43">glNormalPointer</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_NORMAL_ARRAY_STRIDE"></a><a id="gl_normal_array_stride"></a><dl>
<dt><b>GL_NORMAL_ARRAY_STRIDE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value, the byte offset between consecutive normals in the normal array. See <a href="https://msdn.microsoft.com/6ffb0522-87cc-4be1-a5b1-f6fd30e04b43">glNormalPointer</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_NORMAL_ARRAY_TYPE"></a><a id="gl_normal_array_type"></a><dl>
<dt><b>GL_NORMAL_ARRAY_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value, the data type of each coordinate in the normal array. See <a href="https://msdn.microsoft.com/6ffb0522-87cc-4be1-a5b1-f6fd30e04b43">glNormalPointer</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_NORMALIZE"></a><a id="gl_normalize"></a><dl>
<dt><b>GL_NORMALIZE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether normals are automatically scaled to unit length after they have been transformed to eye coordinates. See <a href="https://msdn.microsoft.com/e90bfed4-ab72-43d2-b7b5-37a9fd6ecb4c">glNormal</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_PACK_ALIGNMENT"></a><a id="gl_pack_alignment"></a><dl>
<dt><b>GL_PACK_ALIGNMENT</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the byte alignment used for writing pixel data to memory. See <a href="https://msdn.microsoft.com/c12255eb-8802-4602-b1fa-ab157201ae5c">glPixelStore</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_PACK_LSB_FIRST"></a><a id="gl_pack_lsb_first"></a><dl>
<dt><b>GL_PACK_LSB_FIRST</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether single-bit pixels being written to memory are written first to the least significant bit of each unsigned byte. See <a href="https://msdn.microsoft.com/c12255eb-8802-4602-b1fa-ab157201ae5c">glPixelStore</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_PACK_ROW_LENGTH"></a><a id="gl_pack_row_length"></a><dl>
<dt><b>GL_PACK_ROW_LENGTH</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the row length used for writing pixel data to memory. See <a href="https://msdn.microsoft.com/c12255eb-8802-4602-b1fa-ab157201ae5c">glPixelStore</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_PACK_SKIP_PIXELS"></a><a id="gl_pack_skip_pixels"></a><dl>
<dt><b>GL_PACK_SKIP_PIXELS</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the number of pixel locations skipped before the first pixel is written into memory. See <a href="https://msdn.microsoft.com/c12255eb-8802-4602-b1fa-ab157201ae5c">glPixelStore</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_PACK_SKIP_ROWS"></a><a id="gl_pack_skip_rows"></a><dl>
<dt><b>GL_PACK_SKIP_ROWS</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the number of rows of pixel locations skipped before the first pixel is written into memory. See <a href="https://msdn.microsoft.com/c12255eb-8802-4602-b1fa-ab157201ae5c">glPixelStore</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_PACK_SWAP_BYTES"></a><a id="gl_pack_swap_bytes"></a><dl>
<dt><b>GL_PACK_SWAP_BYTES</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether the bytes of 2-byte and 4-byte pixel indexes and components are swapped before being written to memory. See <a href="https://msdn.microsoft.com/c12255eb-8802-4602-b1fa-ab157201ae5c">glPixelStore</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_PERSPECTIVE_CORRECTION_HINT"></a><a id="gl_perspective_correction_hint"></a><dl>
<dt><b>GL_PERSPECTIVE_CORRECTION_HINT</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: a symbolic constant indicating the mode of the perspective correction hint. See <a href="https://msdn.microsoft.com/6d03e107-321a-45ee-9ce7-25fa9cab32d9">glHint</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_PIXEL_MAP_A_TO_A_SIZE"></a><a id="gl_pixel_map_a_to_a_size"></a><dl>
<dt><b>GL_PIXEL_MAP_A_TO_A_SIZE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the size of the alpha-to-alpha pixel-translation table. See <a href="https://msdn.microsoft.com/79a84334-355c-46d3-990c-4d273e2d2207">glPixelMap</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_PIXEL_MAP_B_TO_B_SIZE"></a><a id="gl_pixel_map_b_to_b_size"></a><dl>
<dt><b>GL_PIXEL_MAP_B_TO_B_SIZE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the size of the blue-to-blue pixel-translation table. See <a href="https://msdn.microsoft.com/79a84334-355c-46d3-990c-4d273e2d2207">glPixelMap</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_PIXEL_MAP_G_TO_G_SIZE"></a><a id="gl_pixel_map_g_to_g_size"></a><dl>
<dt><b>GL_PIXEL_MAP_G_TO_G_SIZE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the size of the green-to-green pixel-translation table. See <a href="https://msdn.microsoft.com/79a84334-355c-46d3-990c-4d273e2d2207">glPixelMap</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_PIXEL_MAP_I_TO_A_SIZE"></a><a id="gl_pixel_map_i_to_a_size"></a><dl>
<dt><b>GL_PIXEL_MAP_I_TO_A_SIZE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the size of the index-to-alpha pixel translation table. See <a href="https://msdn.microsoft.com/79a84334-355c-46d3-990c-4d273e2d2207">glPixelMap</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_PIXEL_MAP_I_TO_B_SIZE"></a><a id="gl_pixel_map_i_to_b_size"></a><dl>
<dt><b>GL_PIXEL_MAP_I_TO_B_SIZE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the size of the index-to-blue pixel translation table. See <a href="https://msdn.microsoft.com/79a84334-355c-46d3-990c-4d273e2d2207">glPixelMap</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_PIXEL_MAP_I_TO_G_SIZE"></a><a id="gl_pixel_map_i_to_g_size"></a><dl>
<dt><b>GL_PIXEL_MAP_I_TO_G_SIZE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the size of the index-to-green pixel-translation table. See <a href="https://msdn.microsoft.com/79a84334-355c-46d3-990c-4d273e2d2207">glPixelMap</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_PIXEL_MAP_I_TO_I_SIZE"></a><a id="gl_pixel_map_i_to_i_size"></a><dl>
<dt><b>GL_PIXEL_MAP_I_TO_I_SIZE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the size of the index-to-index pixel-translation table. See <a href="https://msdn.microsoft.com/79a84334-355c-46d3-990c-4d273e2d2207">glPixelMap</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_PIXEL_MAP_I_TO_R_SIZE"></a><a id="gl_pixel_map_i_to_r_size"></a><dl>
<dt><b>GL_PIXEL_MAP_I_TO_R_SIZE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the size of the index-to-red pixel-translation table. See <a href="https://msdn.microsoft.com/79a84334-355c-46d3-990c-4d273e2d2207">glPixelMap</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_PIXEL_MAP_R_TO_R_SIZE"></a><a id="gl_pixel_map_r_to_r_size"></a><dl>
<dt><b>GL_PIXEL_MAP_R_TO_R_SIZE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the size of the red-to-red pixel-translation table. See <a href="https://msdn.microsoft.com/79a84334-355c-46d3-990c-4d273e2d2207">glPixelMap</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_PIXEL_MAP_S_TO_S_SIZE"></a><a id="gl_pixel_map_s_to_s_size"></a><dl>
<dt><b>GL_PIXEL_MAP_S_TO_S_SIZE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the size of the stencil-to-stencil pixel translation table. See <a href="https://msdn.microsoft.com/79a84334-355c-46d3-990c-4d273e2d2207">glPixelMap</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_POINT_SIZE"></a><a id="gl_point_size"></a><dl>
<dt><b>GL_POINT_SIZE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the point size as specified by <a href="https://msdn.microsoft.com/efa35fa8-721a-48e5-bf59-d33b9bbe7f73">glPointSize</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_POINT_SIZE_GRANULARITY"></a><a id="gl_point_size_granularity"></a><dl>
<dt><b>GL_POINT_SIZE_GRANULARITY</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the size difference between adjacent supported sizes for antialiased points. See <a href="https://msdn.microsoft.com/efa35fa8-721a-48e5-bf59-d33b9bbe7f73">glPointSize</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_POINT_SIZE_RANGE"></a><a id="gl_point_size_range"></a><dl>
<dt><b>GL_POINT_SIZE_RANGE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns two values: the smallest and largest supported sizes for antialiased points. See <a href="https://msdn.microsoft.com/efa35fa8-721a-48e5-bf59-d33b9bbe7f73">glPointSize</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_POINT_SMOOTH"></a><a id="gl_point_smooth"></a><dl>
<dt><b>GL_POINT_SMOOTH</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether antialiasing of points is enabled. See <a href="https://msdn.microsoft.com/efa35fa8-721a-48e5-bf59-d33b9bbe7f73">glPointSize</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_POINT_SMOOTH_HINT"></a><a id="gl_point_smooth_hint"></a><dl>
<dt><b>GL_POINT_SMOOTH_HINT</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: a symbolic constant indicating the mode of the point antialiasing hint. See <a href="https://msdn.microsoft.com/6d03e107-321a-45ee-9ce7-25fa9cab32d9">glHint</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_POLYGON_MODE"></a><a id="gl_polygon_mode"></a><dl>
<dt><b>GL_POLYGON_MODE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns two values: symbolic constants indicating whether front-facing and back-facing polygons are rasterized as points, lines, or filled polygons. See <a href="https://msdn.microsoft.com/d8781bae-e78c-40fb-9f33-c742c70ebda1">glPolygonMode</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_POLYGON_OFFSET_FACTOR"></a><a id="gl_polygon_offset_factor"></a><dl>
<dt><b>GL_POLYGON_OFFSET_FACTOR</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value, the scaling factor used to determine the variable offset that is added to the depth value of each fragment generated when a polygon is rasterized. See <a href="https://msdn.microsoft.com/06bc1aba-1692-40f0-8535-2cb65b487490">glPolygonOffset</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_POLYGON_OFFSET_UNITS"></a><a id="gl_polygon_offset_units"></a><dl>
<dt><b>GL_POLYGON_OFFSET_UNITS</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value. This value is multiplied by an implementation-specific value and then added to the depth value of each fragment generated when a polygon is rasterized. See <a href="https://msdn.microsoft.com/06bc1aba-1692-40f0-8535-2cb65b487490">glPolygonOffset</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_POLYGON_OFFSET_FILL"></a><a id="gl_polygon_offset_fill"></a><dl>
<dt><b>GL_POLYGON_OFFSET_FILL</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether polygon offset is enabled for polygons in fill mode. See <a href="https://msdn.microsoft.com/06bc1aba-1692-40f0-8535-2cb65b487490">glPolygonOffset</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_POLYGON_OFFSET_LINE"></a><a id="gl_polygon_offset_line"></a><dl>
<dt><b>GL_POLYGON_OFFSET_LINE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether polygon offset is enabled for polygons in line mode. See <a href="https://msdn.microsoft.com/06bc1aba-1692-40f0-8535-2cb65b487490">glPolygonOffset</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_POLYGON_OFFSET_POINT"></a><a id="gl_polygon_offset_point"></a><dl>
<dt><b>GL_POLYGON_OFFSET_POINT</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether polygon offset is enabled for polygons in point mode. See <a href="https://msdn.microsoft.com/06bc1aba-1692-40f0-8535-2cb65b487490">glPolygonOffset</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_POLYGON_SMOOTH"></a><a id="gl_polygon_smooth"></a><dl>
<dt><b>GL_POLYGON_SMOOTH</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether antialiasing of polygons is enabled. See <a href="https://msdn.microsoft.com/d8781bae-e78c-40fb-9f33-c742c70ebda1">glPolygonMode</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_POLYGON_SMOOTH_HINT"></a><a id="gl_polygon_smooth_hint"></a><dl>
<dt><b>GL_POLYGON_SMOOTH_HINT</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: a symbolic constant indicating the mode of the polygon antialiasing hint. See <a href="https://msdn.microsoft.com/6d03e107-321a-45ee-9ce7-25fa9cab32d9">glHint</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_POLYGON_STIPPLE"></a><a id="gl_polygon_stipple"></a><dl>
<dt><b>GL_POLYGON_STIPPLE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether stippling of polygons is enabled. See <a href="https://msdn.microsoft.com/e066f9cf-36da-4a3b-a34f-2f8a6f5a0ae6">glPolygonStipple</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_PROJECTION_MATRIX"></a><a id="gl_projection_matrix"></a><dl>
<dt><b>GL_PROJECTION_MATRIX</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns 16 values: the projection matrix on the top of the projection matrix stack. See <a href="https://msdn.microsoft.com/97d8e644-50bb-4130-b6b7-d87df4468e73">glPushMatrix</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_PROJECTION_STACK_DEPTH"></a><a id="gl_projection_stack_depth"></a><dl>
<dt><b>GL_PROJECTION_STACK_DEPTH</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the number of matrices on the projection matrix stack. See <a href="https://msdn.microsoft.com/97d8e644-50bb-4130-b6b7-d87df4468e73">glPushMatrix</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_READ_BUFFER"></a><a id="gl_read_buffer"></a><dl>
<dt><b>GL_READ_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: a symbolic constant indicating which color buffer is selected for reading. See <a href="https://msdn.microsoft.com/41fbad5c-b8ca-456d-bbfc-b48c176e15b0">glReadPixels</a> and <a href="https://msdn.microsoft.com/3ddd69fe-74fc-4ac0-be8d-bcaa71ac0292">glAccum</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_RED_BIAS"></a><a id="gl_red_bias"></a><dl>
<dt><b>GL_RED_BIAS</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the red bias factor used during pixel transfers. See <a href="https://msdn.microsoft.com/c14349c0-ff50-441f-b9fd-8b0f5114fd8a">glPixelTransfer</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_RED_BITS"></a><a id="gl_red_bits"></a><dl>
<dt><b>GL_RED_BITS</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the number of red bitplanes in each color buffer.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_RED_SCALE"></a><a id="gl_red_scale"></a><dl>
<dt><b>GL_RED_SCALE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the red scale factor used during pixel transfers. See <a href="https://msdn.microsoft.com/c14349c0-ff50-441f-b9fd-8b0f5114fd8a">glPixelTransfer</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_RENDER_MODE"></a><a id="gl_render_mode"></a><dl>
<dt><b>GL_RENDER_MODE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: a symbolic constant indicating whether OpenGL is in render, select, or feedback mode. See <a href="https://msdn.microsoft.com/bcbc3bba-c552-425b-8284-6cadff0c9f56">glRenderMode</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_RGBA_MODE"></a><a id="gl_rgba_mode"></a><dl>
<dt><b>GL_RGBA_MODE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether OpenGL is in RGBA mode (TRUE) or color-index mode (FALSE). See <a href="https://msdn.microsoft.com/916eb8b5-65c2-4523-bdb5-e609ad7a24a0">glColor</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_SCISSOR_BOX"></a><a id="gl_scissor_box"></a><dl>
<dt><b>GL_SCISSOR_BOX</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns four values: the <i>x</i> and <i>y</i> window coordinates of the scissor box, followed by its width and height. See <a href="https://msdn.microsoft.com/c06a1d20-bf7b-4283-b0fe-8bd80bece4ce">glScissor</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_SCISSOR_TEST"></a><a id="gl_scissor_test"></a><dl>
<dt><b>GL_SCISSOR_TEST</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether scissoring is enabled. See <a href="https://msdn.microsoft.com/c06a1d20-bf7b-4283-b0fe-8bd80bece4ce">glScissor</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_SHADE_MODEL"></a><a id="gl_shade_model"></a><dl>
<dt><b>GL_SHADE_MODEL</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: a symbolic constant indicating whether the shading mode is flat or smooth. See <a href="https://msdn.microsoft.com/52985ad7-1d6c-48fc-8f1e-4eb2c0324c8e">glShadeModel</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_STENCIL_BITS"></a><a id="gl_stencil_bits"></a><dl>
<dt><b>GL_STENCIL_BITS</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the number of bitplanes in the stencil buffer.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_STENCIL_CLEAR_VALUE"></a><a id="gl_stencil_clear_value"></a><dl>
<dt><b>GL_STENCIL_CLEAR_VALUE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the index to which the stencil bitplanes are cleared. See <a href="https://msdn.microsoft.com/bbde8fa8-78f3-45bd-bac3-5d03839acc52">glClearStencil</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_STENCIL_FAIL"></a><a id="gl_stencil_fail"></a><dl>
<dt><b>GL_STENCIL_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: a symbolic constant indicating what action is taken when the stencil test fails. See <a href="https://msdn.microsoft.com/16809735-5624-49cf-bfa5-9908d008b234">glStencilOp</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_STENCIL_FUNC"></a><a id="gl_stencil_func"></a><dl>
<dt><b>GL_STENCIL_FUNC</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: a symbolic constant indicating what function is used to compare the stencil reference value with the stencil buffer value. See <a href="https://msdn.microsoft.com/6c84415b-4d22-494b-90f2-6243d1406725">glStencilFunc</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_STENCIL_PASS_DEPTH_FAIL"></a><a id="gl_stencil_pass_depth_fail"></a><dl>
<dt><b>GL_STENCIL_PASS_DEPTH_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: a symbolic constant indicating what action is taken when the stencil test passes, but the depth test fails. See <a href="https://msdn.microsoft.com/16809735-5624-49cf-bfa5-9908d008b234">glStencilOp</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_STENCIL_PASS_DEPTH_PASS"></a><a id="gl_stencil_pass_depth_pass"></a><dl>
<dt><b>GL_STENCIL_PASS_DEPTH_PASS</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: a symbolic constant indicating what action is taken when the stencil test passes and the depth test passes. See <a href="https://msdn.microsoft.com/16809735-5624-49cf-bfa5-9908d008b234">glStencilOp</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_STENCIL_REF"></a><a id="gl_stencil_ref"></a><dl>
<dt><b>GL_STENCIL_REF</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the reference value that is compared with the contents of the stencil buffer. See <a href="https://msdn.microsoft.com/6c84415b-4d22-494b-90f2-6243d1406725">glStencilFunc</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_STENCIL_TEST"></a><a id="gl_stencil_test"></a><dl>
<dt><b>GL_STENCIL_TEST</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether stencil testing of fragments is enabled. See <a href="https://msdn.microsoft.com/6c84415b-4d22-494b-90f2-6243d1406725">glStencilFunc</a> and <a href="https://msdn.microsoft.com/16809735-5624-49cf-bfa5-9908d008b234">glStencilOp</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_STENCIL_VALUE_MASK"></a><a id="gl_stencil_value_mask"></a><dl>
<dt><b>GL_STENCIL_VALUE_MASK</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the mask that is used to mask both the stencil reference value and the stencil buffer value before they are compared. See <a href="https://msdn.microsoft.com/6c84415b-4d22-494b-90f2-6243d1406725">glStencilFunc</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_STENCIL_WRITEMASK"></a><a id="gl_stencil_writemask"></a><dl>
<dt><b>GL_STENCIL_WRITEMASK</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the mask that controls writing of the stencil bitplanes. See <a href="https://msdn.microsoft.com/c586f9db-bad5-4f06-a194-a8d979842d0c">glStencilMask</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_STEREO"></a><a id="gl_stereo"></a><dl>
<dt><b>GL_STEREO</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether stereo buffers (left and right) are supported.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_SUBPIXEL_BITS"></a><a id="gl_subpixel_bits"></a><dl>
<dt><b>GL_SUBPIXEL_BITS</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: an estimate of the number of bits of subpixel resolution that are used to position rasterized geometry in window coordinates.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_TEXTURE_1D"></a><a id="gl_texture_1d"></a><dl>
<dt><b>GL_TEXTURE_1D</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether 1-D texture mapping is enabled. See <a href="https://msdn.microsoft.com/4f537b89-2ea2-4e2e-8c57-c372bf53f12c">glTexImage1D</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_TEXTURE_2D"></a><a id="gl_texture_2d"></a><dl>
<dt><b>GL_TEXTURE_2D</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether 2-D texture mapping is enabled. See <a href="https://msdn.microsoft.com/e8b9c692-5239-47de-86eb-80c247c60e1d">glTexImage2D</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_TEXTURE_COORD_ARRAY"></a><a id="gl_texture_coord_array"></a><dl>
<dt><b>GL_TEXTURE_COORD_ARRAY</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether the texture coordinate array is enabled. See <a href="https://msdn.microsoft.com/c3640a1b-ccc7-4f1a-94a5-a164f7377dbc">glTexCoordPointer</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_TEXTURE_COORD_ARRAY_SIZE"></a><a id="gl_texture_coord_array_size"></a><dl>
<dt><b>GL_TEXTURE_COORD_ARRAY_SIZE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value, the number of coordinates per element in the texture coordinate array. See <a href="https://msdn.microsoft.com/c3640a1b-ccc7-4f1a-94a5-a164f7377dbc">glTexCoordPointer</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_TEXTURE_COORD_ARRAY_STRIDE"></a><a id="gl_texture_coord_array_stride"></a><dl>
<dt><b>GL_TEXTURE_COORD_ARRAY_STRIDE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value, the byte offset between consecutive elements in the texture coordinate array. See <a href="https://msdn.microsoft.com/c3640a1b-ccc7-4f1a-94a5-a164f7377dbc">glTexCoordPointer</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_TEXTURE_COORD_ARRAY_TYPE"></a><a id="gl_texture_coord_array_type"></a><dl>
<dt><b>GL_TEXTURE_COORD_ARRAY_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter params returns one value, the data type of the coordinates in the texture coordinate array. See <a href="https://msdn.microsoft.com/c3640a1b-ccc7-4f1a-94a5-a164f7377dbc">glTexCoordPointer</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_TEXTURE_ENV_COLOR"></a><a id="gl_texture_env_color"></a><dl>
<dt><b>GL_TEXTURE_ENV_COLOR</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns four values: the red, green, blue, and alpha values of the texture environment color. Integer values, if requested, are linearly mapped from the internal floating-point representation such that 1.0 returns the most positive representable integer value, and 1.0 returns the most negative representable integer value. See <a href="https://msdn.microsoft.com/7a130cbe-e34b-4381-b6f2-53e2b9234067">glTexEnv</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_TEXTURE_ENV_MODE"></a><a id="gl_texture_env_mode"></a><dl>
<dt><b>GL_TEXTURE_ENV_MODE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: a symbolic constant indicating which texture environment function is currently selected. See <a href="https://msdn.microsoft.com/7a130cbe-e34b-4381-b6f2-53e2b9234067">glTexEnv</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_TEXTURE_GEN_Q"></a><a id="gl_texture_gen_q"></a><dl>
<dt><b>GL_TEXTURE_GEN_Q</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether automatic generation of the Q texture coordinate is enabled. See <a href="https://msdn.microsoft.com/958c2932-c220-412c-a85e-eed613332dea">glTexGen</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_TEXTURE_GEN_R"></a><a id="gl_texture_gen_r"></a><dl>
<dt><b>GL_TEXTURE_GEN_R</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether automatic generation of the R texture coordinate is enabled. See <a href="https://msdn.microsoft.com/958c2932-c220-412c-a85e-eed613332dea">glTexGen</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_TEXTURE_GEN_S"></a><a id="gl_texture_gen_s"></a><dl>
<dt><b>GL_TEXTURE_GEN_S</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether automatic generation of the S texture coordinate is enabled. See <a href="https://msdn.microsoft.com/958c2932-c220-412c-a85e-eed613332dea">glTexGen</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_TEXTURE_GEN_T"></a><a id="gl_texture_gen_t"></a><dl>
<dt><b>GL_TEXTURE_GEN_T</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether automatic generation of the T texture coordinate is enabled. See <a href="https://msdn.microsoft.com/958c2932-c220-412c-a85e-eed613332dea">glTexGen</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_TEXTURE_MATRIX"></a><a id="gl_texture_matrix"></a><dl>
<dt><b>GL_TEXTURE_MATRIX</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns 16 values: the texture matrix on the top of the texture matrix stack. See <a href="https://msdn.microsoft.com/97d8e644-50bb-4130-b6b7-d87df4468e73">glPushMatrix</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_TEXTURE_STACK_DEPTH"></a><a id="gl_texture_stack_depth"></a><dl>
<dt><b>GL_TEXTURE_STACK_DEPTH</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the number of matrices on the texture matrix stack. See <a href="https://msdn.microsoft.com/97d8e644-50bb-4130-b6b7-d87df4468e73">glPushMatrix</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_UNPACK_ALIGNMENT"></a><a id="gl_unpack_alignment"></a><dl>
<dt><b>GL_UNPACK_ALIGNMENT</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the byte alignment used for reading pixel data from memory. See <a href="https://msdn.microsoft.com/c12255eb-8802-4602-b1fa-ab157201ae5c">glPixelStore</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_UNPACK_LSB_FIRST"></a><a id="gl_unpack_lsb_first"></a><dl>
<dt><b>GL_UNPACK_LSB_FIRST</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether single-bit pixels being read from memory are read first from the least significant bit of each unsigned byte. See <a href="https://msdn.microsoft.com/c12255eb-8802-4602-b1fa-ab157201ae5c">glPixelStore</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_UNPACK_ROW_LENGTH"></a><a id="gl_unpack_row_length"></a><dl>
<dt><b>GL_UNPACK_ROW_LENGTH</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the row length used for reading pixel data from memory. See <a href="https://msdn.microsoft.com/c12255eb-8802-4602-b1fa-ab157201ae5c">glPixelStore</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_UNPACK_SKIP_PIXELS"></a><a id="gl_unpack_skip_pixels"></a><dl>
<dt><b>GL_UNPACK_SKIP_PIXELS</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the number of pixel locations skipped before the first pixel is read from memory. See <a href="https://msdn.microsoft.com/c12255eb-8802-4602-b1fa-ab157201ae5c">glPixelStore</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_UNPACK_SKIP_ROWS"></a><a id="gl_unpack_skip_rows"></a><dl>
<dt><b>GL_UNPACK_SKIP_ROWS</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the number of rows of pixel locations skipped before the first pixel is read from memory. See <a href="https://msdn.microsoft.com/c12255eb-8802-4602-b1fa-ab157201ae5c">glPixelStore</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_UNPACK_SWAP_BYTES"></a><a id="gl_unpack_swap_bytes"></a><dl>
<dt><b>GL_UNPACK_SWAP_BYTES</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether the bytes of 2-byte and 4-byte pixel indexes and components are swapped after being read from memory. See <a href="https://msdn.microsoft.com/c12255eb-8802-4602-b1fa-ab157201ae5c">glPixelStore</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_VERTEX_ARRAY"></a><a id="gl_vertex_array"></a><dl>
<dt><b>GL_VERTEX_ARRAY</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns a single Boolean value indicating whether the vertex array is enabled. See <a href="https://msdn.microsoft.com/e5f97fdc-9448-4389-8533-3855a3213feb">glVertexPointer</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_VERTEX_ARRAY_SIZE"></a><a id="gl_vertex_array_size"></a><dl>
<dt><b>GL_VERTEX_ARRAY_SIZE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value, the number of coordinates per vertex in the vertex array. See <a href="https://msdn.microsoft.com/e5f97fdc-9448-4389-8533-3855a3213feb">glVertexPointer</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_VERTEX_ARRAY_STRIDE"></a><a id="gl_vertex_array_stride"></a><dl>
<dt><b>GL_VERTEX_ARRAY_STRIDE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value, the byte offset between consecutive vertexes in the vertex array. See <a href="https://msdn.microsoft.com/e5f97fdc-9448-4389-8533-3855a3213feb">glVertexPointer</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_VERTEX_ARRAY_TYPE"></a><a id="gl_vertex_array_type"></a><dl>
<dt><b>GL_VERTEX_ARRAY_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value, the data type of each coordinate in the vertex array. See <a href="https://msdn.microsoft.com/e5f97fdc-9448-4389-8533-3855a3213feb">glVertexPointer</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_VIEWPORT"></a><a id="gl_viewport"></a><dl>
<dt><b>GL_VIEWPORT</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns four values: the <i>x</i> and <i>y</i> window coordinates of the viewport, followed by its width and height. See <a href="https://msdn.microsoft.com/11816b2f-ee18-42ef-a782-2e96699dd087">glViewport</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_ZOOM_X"></a><a id="gl_zoom_x"></a><dl>
<dt><b>GL_ZOOM_X</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the <i>x</i> pixel zoom factor. See <a href="https://msdn.microsoft.com/57ead7d8-0502-46b4-9f66-dbb3cb75b0f9">glPixelZoom</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_ZOOM_Y"></a><a id="gl_zoom_y"></a><dl>
<dt><b>GL_ZOOM_Y</b></dt>
</dl>
</td>
<td width="60%">
The <i>params</i> parameter returns one value: the <i>y</i> pixel zoom factor. See <a href="https://msdn.microsoft.com/57ead7d8-0502-46b4-9f66-dbb3cb75b0f9">glPixelZoom</a>.

</td>
</tr>
</table>
 


### -param params

Returns the value or values of the specified parameter.


## -returns



This function does not return a value.




## -remarks



This function returns values for simple state variables in OpenGL. The <i>pname</i> parameter is a symbolic constant indicating the state variable to be returned, and <i>params</i> is a pointer to an array of the indicated type in which to place the returned data.

Type conversion is performed if <i>params</i> has a different type from the state variable value being requested. If you call <a href="https://msdn.microsoft.com/dda38a63-9cf6-46f4-9b7a-52ee4fe2a5e1">glGetBooleanv</a>, a floating-point or integer value is converted to GL_FALSE if and only if it is zero. Otherwise, it is converted to GL_TRUE.

If you call <a href="https://msdn.microsoft.com/16b04af6-5da3-439f-8d4f-bc8ab1fcb2c5">glGetIntegerv</a>, Boolean values are returned as GL_TRUE or GL_FALSE, and most floating-point values are rounded to the nearest integer value. Floating-point colors and normals, however, are returned with a linear mapping that maps 1.0 to the most positive representable integer value and 1.0 to the most negative representable integer value.

If you call <b>glGetFloatv</b> or <a href="https://msdn.microsoft.com/9d99e653-7997-4e38-82d2-e7b1525208fe">glGetDoublev</a>, Boolean values are returned as GL_TRUE or GL_FALSE, and integer values are converted to floating-point values.

You can query many of the Boolean parameters more easily with <a href="https://msdn.microsoft.com/18df5a6f-dc21-434d-a2e8-2c58597df037">glIsEnabled</a>.




## -see-also




<a href="https://msdn.microsoft.com/3ddd69fe-74fc-4ac0-be8d-bcaa71ac0292">glAccum</a>



<a href="https://msdn.microsoft.com/6c0c06b5-1bad-4590-a262-f134f63f0936">glAlphaFunc</a>



<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/6756774b-5eef-419a-a653-0b251aed65a0">glBlendFunc</a>



<a href="https://msdn.microsoft.com/9373d32e-b11e-4a80-8713-da2c1d8d9368">glCallList</a>



<a href="https://msdn.microsoft.com/77d8f340-be47-43f4-96fc-31025a4c8b4e">glClearAccum</a>



<a href="https://msdn.microsoft.com/f938e3f4-9db3-4c24-97ae-531b6799224e">glClearColor</a>



<a href="https://msdn.microsoft.com/8e26ae78-edc1-4201-a0db-d5bc8ae6dc82">glClearDepth</a>



<a href="https://msdn.microsoft.com/87983d93-c5a1-445f-8621-1c2952d93a0f">glClearIndex</a>



<a href="https://msdn.microsoft.com/bbde8fa8-78f3-45bd-bac3-5d03839acc52">glClearStencil</a>



<a href="https://msdn.microsoft.com/b70d2c30-7502-4399-8c08-5ec9a2a1919c">glClipPlane</a>



<a href="https://msdn.microsoft.com/916eb8b5-65c2-4523-bdb5-e609ad7a24a0">glColor</a>



<a href="https://msdn.microsoft.com/23d7f94e-f290-423c-a841-f86caf94009d">glColorMask</a>



<a href="https://msdn.microsoft.com/6dbef2c2-f902-4f25-8a87-9e3d710dd807">glColorMaterial</a>



<a href="https://msdn.microsoft.com/53bf05b5-a68b-4d96-b4e7-2878a0a86a13">glCullFace</a>



<a href="https://msdn.microsoft.com/6ab8774a-8887-4c1e-b567-4492c0a60cf2">glDepthFunc</a>



<a href="https://msdn.microsoft.com/067b18e2-f21a-4dde-8fa6-dd975746e189">glDepthMask</a>



<a href="https://msdn.microsoft.com/44aed5e5-4bd2-4e7f-ad05-1cf4be5254a5">glDepthRange</a>



<a href="https://msdn.microsoft.com/ea625699-303b-4e60-b9aa-771949a8d52d">glDrawBuffer</a>



<a href="https://msdn.microsoft.com/26e4e901-4d91-4d7c-ad07-b4480062a4cb">glEdgeFlag</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/019c2006-679a-4611-8156-f6665d3ef5b2">glFog</a>



<a href="https://msdn.microsoft.com/4087107c-99cd-4c26-92e3-8dc43633d51f">glFrontFace</a>



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



<a href="https://msdn.microsoft.com/6d03e107-321a-45ee-9ce7-25fa9cab32d9">glHint</a>



<a href="https://msdn.microsoft.com/239c2e5d-cd87-4c2e-8fa1-7c71a32d4350">glIndex</a>



<a href="https://msdn.microsoft.com/f4b5df36-390f-4254-95fb-98589750a11b">glIndexMask</a>



<a href="https://msdn.microsoft.com/18df5a6f-dc21-434d-a2e8-2c58597df037">glIsEnabled</a>



<a href="https://msdn.microsoft.com/004f0f53-4c72-48df-8231-6b39df464061">glLight</a>



<a href="https://msdn.microsoft.com/8214765c-5722-4df0-88ed-3a5ac039aac4">glLightModel</a>



<a href="https://msdn.microsoft.com/256d968c-9e72-4aec-9faf-afe70f1087a8">glLineStipple</a>



<a href="https://msdn.microsoft.com/13a69fd7-5eee-42ec-bd05-5bd3c838d4d7">glLineWidth</a>



<a href="https://msdn.microsoft.com/df82f699-b2af-471a-83f3-5620857ba45d">glListBase</a>



<a href="https://msdn.microsoft.com/29edf9bd-f3b8-4de7-9afb-07714f4efd92">glLogicOp</a>



<a href="https://msdn.microsoft.com/47b0bd46-aa79-4146-8503-cddcc8b7b242">glMap1</a>



<a href="https://msdn.microsoft.com/8365a9bd-156b-4f57-8ceb-1edcbcea9eb4">glMap2</a>



<a href="https://msdn.microsoft.com/87532b49-a506-44a7-be2f-b74c289f1a19">glMapGrid</a>



<a href="https://msdn.microsoft.com/f1006ea3-322a-42a9-b33c-6c7181985ef9">glMatrixMode</a>



<a href="https://msdn.microsoft.com/9c6556d4-855f-4cba-94cc-27b5f1e4607a">glNewList</a>



<a href="https://msdn.microsoft.com/e90bfed4-ab72-43d2-b7b5-37a9fd6ecb4c">glNormal</a>



<a href="https://msdn.microsoft.com/79a84334-355c-46d3-990c-4d273e2d2207">glPixelMap</a>



<a href="https://msdn.microsoft.com/c12255eb-8802-4602-b1fa-ab157201ae5c">glPixelStore</a>



<a href="https://msdn.microsoft.com/c14349c0-ff50-441f-b9fd-8b0f5114fd8a">glPixelTransfer</a>



<a href="https://msdn.microsoft.com/57ead7d8-0502-46b4-9f66-dbb3cb75b0f9">glPixelZoom</a>



<a href="https://msdn.microsoft.com/efa35fa8-721a-48e5-bf59-d33b9bbe7f73">glPointSize</a>



<a href="https://msdn.microsoft.com/d8781bae-e78c-40fb-9f33-c742c70ebda1">glPolygonMode</a>



<a href="https://msdn.microsoft.com/e066f9cf-36da-4a3b-a34f-2f8a6f5a0ae6">glPolygonStipple</a>



<a href="https://msdn.microsoft.com/3c7b93cc-2112-4771-b422-a244821447e5">glPushAttrib</a>



<a href="https://msdn.microsoft.com/97d8e644-50bb-4130-b6b7-d87df4468e73">glPushMatrix</a>



<a href="https://msdn.microsoft.com/e4319018-42c0-4567-b67f-31dbdbee9b13">glPushName</a>



<a href="https://msdn.microsoft.com/2a661893-0818-441d-9399-0103560737c3">glRasterPos</a>



<a href="https://msdn.microsoft.com/41fbad5c-b8ca-456d-bbfc-b48c176e15b0">glReadPixels</a>



<a href="https://msdn.microsoft.com/c06a1d20-bf7b-4283-b0fe-8bd80bece4ce">glScissor</a>



<a href="https://msdn.microsoft.com/52985ad7-1d6c-48fc-8f1e-4eb2c0324c8e">glShadeModel</a>



<a href="https://msdn.microsoft.com/6c84415b-4d22-494b-90f2-6243d1406725">glStencilFunc</a>



<a href="https://msdn.microsoft.com/c586f9db-bad5-4f06-a194-a8d979842d0c">glStencilMask</a>



<a href="https://msdn.microsoft.com/16809735-5624-49cf-bfa5-9908d008b234">glStencilOp</a>



<a href="https://msdn.microsoft.com/71eb39f1-e1ad-4b97-83e0-d2670f5a7545">glTexCoord</a>



<a href="https://msdn.microsoft.com/7a130cbe-e34b-4381-b6f2-53e2b9234067">glTexEnv</a>



<a href="https://msdn.microsoft.com/958c2932-c220-412c-a85e-eed613332dea">glTexGen</a>



<a href="https://msdn.microsoft.com/4f537b89-2ea2-4e2e-8c57-c372bf53f12c">glTexImage1D</a>



<a href="https://msdn.microsoft.com/e8b9c692-5239-47de-86eb-80c247c60e1d">glTexImage2D</a>



<a href="https://msdn.microsoft.com/11816b2f-ee18-42ef-a782-2e96699dd087">glViewport</a>
 

 

