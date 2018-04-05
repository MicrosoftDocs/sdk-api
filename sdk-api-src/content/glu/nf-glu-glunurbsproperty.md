---
UID: NF:glu.gluNurbsProperty
title: gluNurbsProperty function
author: windows-driver-content
description: The gluNurbsProperty function sets a Non-Uniform Rational B-Spline (NURBS) property.
old-location: opengl\glunurbsproperty.htm
old-project: OpenGL
ms.assetid: c8c3b0c3-11b8-4123-91b6-75fed78932ce
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GLU_AUTO_LOAD_MATRIX, GLU_CULLING, GLU_DISPLAY_MODE, GLU_DOMAIN_DISTANCE, GLU_PARAMETRIC_ERROR, GLU_PARAMETRIC_TOLERANCE, GLU_PATH_LENGTH, GLU_SAMPLING_METHOD, GLU_SAMPLING_TOLERANCE, GLU_U_STEP, GLU_V_STEP, _ogl_gluNurbsProperty, glu/gluNurbsProperty, gluNurbsProperty, gluNurbsProperty function [OpenGL], opengl.glunurbsproperty
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: glu.h
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
-	glu32.dll
api_name:
-	gluNurbsProperty
product: Windows
targetos: Windows
req.lib: Glu32.lib
req.dll: Glu32.dll
req.irql: 
req.product: GDI+ 1.1
---

# gluNurbsProperty function


## -description


The <b>gluNurbsProperty</b> function sets a Non-Uniform Rational B-Spline (<a href="https://msdn.microsoft.com/0b55659d-9fa2-47fc-ae15-0c296bd94dcb">NURBS</a>) property.


## -parameters




### -param nobj

The NURBS object (created with <a href="https://msdn.microsoft.com/f47badb0-6b75-4bfd-9771-516668d9e255">gluNewNurbsRenderer</a>).


### -param property

The property to be set. The following values are valid:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GLU_SAMPLING_TOLERANCE"></a><a id="glu_sampling_tolerance"></a><dl>
<dt><b>GLU_SAMPLING_TOLERANCE</b></dt>
</dl>
</td>
<td width="60%">
Specifies the maximum length, in pixels, to use when the sampling method is set to GLU_PATH_LENGTH. The default value is 50.0 pixels.

</td>
</tr>
<tr>
<td width="40%"><a id="GLU_DISPLAY_MODE"></a><a id="glu_display_mode"></a><dl>
<dt><b>GLU_DISPLAY_MODE</b></dt>
</dl>
</td>
<td width="60%">
The <i>value</i> parameter defines how a NURBS surface is to be rendered. You can set <i>value</i> to GLU_FILL, GLU_OUTLINE_POLYGON, or GLU_OUTLINE_PATCH. 

GLU_FILL. The surface is rendered as a set of polygons. This is the default value. 

GLU_OUTLINE_POLYGON. The NURBS library draws only the outlines of the polygons created by tessellation. 

GLU_OUTLINE_PATCH. Only the outlines of patches and trim curves defined by the user are drawn.

</td>
</tr>
<tr>
<td width="40%"><a id="GLU_CULLING"></a><a id="glu_culling"></a><dl>
<dt><b>GLU_CULLING</b></dt>
</dl>
</td>
<td width="60%">
The <i>value</i> parameter is a Boolean value. When value is set to GL_TRUE, NURBS curves whose control points lie outside the current viewport are discarded prior to tessellation. The default is GL_FALSE (because a NURBS curve cannot fall entirely within the convex hull of its control points).

</td>
</tr>
<tr>
<td width="40%"><a id="GLU_AUTO_LOAD_MATRIX"></a><a id="glu_auto_load_matrix"></a><dl>
<dt><b>GLU_AUTO_LOAD_MATRIX</b></dt>
</dl>
</td>
<td width="60%">
The <i>value</i> parameter is a Boolean value. When set to GL_TRUE, the NURBS code downloads the projection matrix, modelview matrix, and viewport from the OpenGL server to compute sampling and culling matrices for each NURBS curve that is rendered. Sampling and culling matrices are required to determine the tessellation of a NURBS surface into line segments or polygons and to cull a NURBS surface if it lies outside of the viewport. 

If this mode is set to GL_FALSE, you must provide a projection matrix, modelview matrix, and viewport for the NURBS renderer to use to construct sampling and culling matrices. You can do this with the <a href="https://msdn.microsoft.com/7fdbc4e2-a037-4f07-bb03-e51feea42775">gluLoadSamplingMatrices</a> function.

The default for this mode is GL_TRUE. Changing this mode from GL_TRUE to GL_FALSE does not affect the sampling and culling matrices until you call <a href="https://msdn.microsoft.com/7fdbc4e2-a037-4f07-bb03-e51feea42775">gluLoadSamplingMatrices</a>. 

The following property parameters are supported in GLU version 1.1 or later and are not valid for GLU version 1.0: GLU_PARAMETRIC_TOLERANCE, GLU_SAMPLING_METHOD, GLU_U_STEP, and GLU_V_STEP.

The following value parameters are supported in GLU version 1.1 or later and are not valid for GLU version 1.0: GLU_PATH_LENGTH, GLU_PARAMETRIC_ERROR, and GLU_DOMAIN_DISTANCE.

</td>
</tr>
<tr>
<td width="40%"><a id="GLU_PARAMETRIC_TOLERANCE"></a><a id="glu_parametric_tolerance"></a><dl>
<dt><b>GLU_PARAMETRIC_TOLERANCE</b></dt>
</dl>
</td>
<td width="60%">
Specifies the maximum distance, in pixels, to use when the sampling method is set to GLU_PARAMETRIC_ERROR. The default value is 0.5.

</td>
</tr>
<tr>
<td width="40%"><a id="GLU_SAMPLING_METHOD"></a><a id="glu_sampling_method"></a><dl>
<dt><b>GLU_SAMPLING_METHOD</b></dt>
</dl>
</td>
<td width="60%">
Specifies how to tessallate a NURBS surface. GLU_SAMPLING_METHOD can have one of the following three values. 

GLU_PATH_LENGTH. The default value. Specifies that surfaces rendered with the maximum length, in pixels, of the edges of the tessellation polygons are no greater than the value specified by GLU_SAMPLING_TOLERANCE. 

GLU_PARAMETRIC_ERROR. Specifies that in rendering the surface, the value of GLU_PARAMETRIC_TOLERANCE specifies the maximum distance, in pixels, between the tessellation polygons and the surfaces they approximate. 

GLU_DOMAIN_DISTANCE. Specifies, in parametric coordinates, how many sample points per unit length to take in the <i>u</i> and <i>v</i> dimensions.

</td>
</tr>
<tr>
<td width="40%"><a id="GLU_U_STEP"></a><a id="glu_u_step"></a><dl>
<dt><b>GLU_U_STEP</b></dt>
</dl>
</td>
<td width="60%">
Specifies the number of sample points per unit length taken along the <i>u</i> dimension in parametric coordinates. The value of GLU_U_STEP is used when GLU_SAMPLING_METHOD is set to GLU_DOMAIN_DISTANCE. The default value is 100.

</td>
</tr>
<tr>
<td width="40%"><a id="GLU_V_STEP"></a><a id="glu_v_step"></a><dl>
<dt><b>GLU_V_STEP</b></dt>
</dl>
</td>
<td width="60%">
Specifies the number of sample points per unit length taken along the <i>v</i> dimension in parametric coordinates. The value of GLU_V_STEP is used when GLU_SAMPLING_METHOD is set to GLU_DOMAIN_DISTANCE. The default value is 100.

</td>
</tr>
</table>
 


### -param value

The value to which to set the indicated property. The <i>value</i> parameter can be a numeric value or one of the following three values: GLU_PATH_LENGTH, GLU_PARAMETRIC_ERROR, or GLU_DOMAIN_DISTANCE. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GLU_PATH_LENGTH"></a><a id="glu_path_length"></a><dl>
<dt><b>GLU_PATH_LENGTH</b></dt>
</dl>
</td>
<td width="60%">
The default value. Specifies that surfaces rendered with the maximum length, in pixels, of the edges of the tessellation polygons are no greater than the value specified by GLU_SAMPLING_TOLERANCE.

</td>
</tr>
<tr>
<td width="40%"><a id="GLU_PARAMETRIC_ERROR"></a><a id="glu_parametric_error"></a><dl>
<dt><b>GLU_PARAMETRIC_ERROR</b></dt>
</dl>
</td>
<td width="60%">
Specifies that in rendering the surface, the value of GLU_PARAMETRIC_TOLERANCE specifies the maximum distance, in pixels, between the tessellation polygons and the surfaces they approximate.

</td>
</tr>
<tr>
<td width="40%"><a id="GLU_DOMAIN_DISTANCE"></a><a id="glu_domain_distance"></a><dl>
<dt><b>GLU_DOMAIN_DISTANCE</b></dt>
</dl>
</td>
<td width="60%">
Specifies, in parametric coordinates, how many sample points per unit length to take in the <i>u</i> and <i>v</i> dimensions.

</td>
</tr>
</table>
 


## -returns



This function does not return a value.




## -remarks



Use <b>gluNurbsProperty</b> to control properties stored in a NURBS object. These properties affect the way a NURBS curve is rendered.

<table></table>
 




## -see-also




<a href="https://msdn.microsoft.com/7dbc75a0-d04e-4794-b3dd-a602addf9dfa">gluGetNurbsProperty</a>



<a href="https://msdn.microsoft.com/e6d9ce03-3218-4145-8bb5-3989afe62436">gluGetString</a>



<a href="https://msdn.microsoft.com/7fdbc4e2-a037-4f07-bb03-e51feea42775">gluLoadSamplingMatrices</a>



<a href="https://msdn.microsoft.com/f47badb0-6b75-4bfd-9771-516668d9e255">gluNewNurbsRenderer</a>
 

 

