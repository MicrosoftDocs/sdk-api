---
UID: NF:glu.gluTessCallback
title: gluTessCallback function
author: windows-driver-content
description: The gluTessCallback function defines a callback for a tessellation object.
old-location: opengl\glutess.htm
old-project: OpenGL
ms.assetid: a9709919-d34c-42c4-82b8-6a503f2b39b0
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_gluTessCallback, glu/gluTessCallback, gluTessCallback, gluTessCallback function [OpenGL], opengl.glutess"
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
-	Glu32.dll
api_name:
-	gluTessCallback
product: Windows
targetos: Windows
req.lib: Glu32.lib
req.dll: Glu32.dll
req.irql: 
req.product: GDI+ 1.1
---

# gluTessCallback function


## -description


The <b>gluTessCallback</b> function defines a callback for a tessellation object.


## -parameters




### -param tess

The tessellation object (created with <a href="https://msdn.microsoft.com/dfc9fce8-ecab-493b-85ee-6d7487814186">gluNewTess</a>).


### -param which

The callback being defined. The following values are valid: GLU_TESS_BEGIN, GLU_TESS_BEGIN_DATA, GLU_TESS_EDGE_FLAG, GLU_TESS_EDGE_FLAG_DATA, GLU_TESS_VERTEX, GLU_TESS_VERTEX_DATA, GLU_TESS_END, GLU_TESS_END_DATA, GLU_TESS_COMBINE, GLU_TESS_COMBINE_DATA, GLU_TESS_ERROR, and GLU_TESS_ERROR_DATA.

For more information on these callbacks, see the following Remarks section.


### -param fn

The function to be called.


## -returns



This function does not return a value.




## -remarks



Use <b>gluTessCallback</b> to specify a callback to be used by a tessellation object. If the specified callback is already defined, then it is replaced. If <i>fn</i> is <b>NULL</b>, then the existing callback becomes undefined.

The tessellation object uses these callbacks to describe how a polygon that you specify is broken into triangles.

There are two versions of each callback, one with polygon data that you can define and one without. If both versions of a particular callback are specified, the callback with the polygon data you specify will be used. The <i>polygon_data</i> parameter of <a href="https://msdn.microsoft.com/3a04363a-c492-4fa5-b312-f2fa2a805782">gluTessBeginPolygon</a> is a copy of the pointer that was specified when <b>gluTessBeginPolygon</b> was called.

The following are valid callbacks:

<table>
<tr>
<th>Callback</th>
<th>Description</th>
</tr>
<tr>
<td>GLU_TESS_BEGIN</td>
<td>The GLU_TESS_BEGIN callback is invoked like <a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a> to indicate the start of a (triangle) primitive. The function takes a single argument of type <b>GLenum</b>. If you set the GLU_TESS_BOUNDARY_ONLY property to GL_FALSE, the argument is set to either GL_TRIANGLE_FAN, GL_TRIANGLE_STRIP, or GL_TRIANGLES. If you set the GLU_TESS_BOUNDARY_ONLY property to GL_TRUE, the argument is set to GL_LINE_LOOP. The function prototype for this callback is as follows: 
				<b>void</b> <b>begin</b> (<b>GLenum</b> <i>type</i>);

</td>
</tr>
<tr>
<td>GLU_TESS_BEGIN_DATA</td>
<td>GLU_TESS_BEGIN_DATA is the same as the GLU_TESS_BEGIN callback except that it takes an additional pointer argument. This pointer is identical to the opaque pointer provided when you call <a href="https://msdn.microsoft.com/3a04363a-c492-4fa5-b312-f2fa2a805782">gluTessBeginPolygon</a>. The function prototype for this callback is: 
				<b>void</b> <b>beginData</b> (<b>GLenum</b> <i>type</i>, <b>void</b> * <i>polygon_data</i>);

</td>
</tr>
<tr>
<td>GLU_TESS_EDGE_FLAG</td>
<td>The GLU_TESS_EDGE_FLAG callback is similar to <a href="https://msdn.microsoft.com/26e4e901-4d91-4d7c-ad07-b4480062a4cb">glEdgeFlag</a>. The function takes a single Boolean flag that indicates which edges lie on the polygon boundary. If the flag is GL_TRUE, then each vertex that follows begins an edge that lies on the polygon boundary; that is, an edge which separates an interior region from an exterior one. If the flag is GL_FALSE, then each vertex that follows begins an edge that lies in the polygon interior. The GLU_TESS_EDGE_FLAG callback (if defined) is invoked before the first vertex callback is made. 
				Because triangle fans and triangle strips do not support edge flags, the begin callback is not called with GL_TRIANGLE_FAN or GL_TRIANGLE_STRIP if an edge flag callback is provided. Instead, the fans and strips are converted to independent triangles. The function prototype for this callback is:

<b>void</b> <b>edgeFlag</b> (<b>GLboolean</b> <i>flag</i>);

</td>
</tr>
<tr>
<td>GLU_TESS_EDGE_FLAG_DATA</td>
<td>The GLU_TESS_EDGE_FLAG_DATA callback is the same as the GLU_TESS_EDGE_FLAG callback except that it takes an additional pointer argument. This pointer is identical to the opaque pointer provided when you call <a href="https://msdn.microsoft.com/3a04363a-c492-4fa5-b312-f2fa2a805782">gluTessBeginPolygon</a>. The function prototype for this callback is: <b>void</b> <b>edgeFlagData</b> (<b>GLboolean</b> <i>flag</i>, <b>void</b> * <i>polygon_data</i>);

</td>
</tr>
<tr>
<td>GLU_TESS_VERTEX</td>
<td>The GLU_TESS_VERTEX callback is invoked between the begin and end callbacks. It is similar to glVertex , and it defines the vertexes of the triangles created by the tessellation process. The function takes a pointer as its only argument. This pointer is identical to the opaque pointer that you provided when you defined the vertex (see <a href="https://msdn.microsoft.com/9c555b32-5257-4eeb-9323-ccad59591097">gluTessVertex</a>). The function prototype for this callback is: <b>void</b> <b>vertex</b> (<b>void</b> * <i>vertex_data</i>);

</td>
</tr>
<tr>
<td>GLU_TESS_VERTEX_DATA</td>
<td>The GLU_TESS_VERTEX_DATA is the same as the GLU_TESS_VERTEX callback except that it takes an additional pointer argument. This pointer is identical to the opaque pointer provided when you call <a href="https://msdn.microsoft.com/3a04363a-c492-4fa5-b312-f2fa2a805782">gluTessBeginPolygon</a>. The function prototype for this callback is: <b>void</b>  <b>vertexData</b> (void * <i>vertex_data</i>, <b>void</b> * <i>polygon_data</i>);

</td>
</tr>
<tr>
<td>GLU_TESS_END</td>
<td>The GLU_TESS_END callback serves the same purpose as <a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>. It indicates the end of a primitive, and it takes no arguments. The function prototype for this callback is: <b>void</b> <b>end</b> (<b>void</b>);

</td>
</tr>
<tr>
<td>GLU_TESS_END_DATA</td>
<td>The GLU_TESS_END_DATA callback is the same as the GLU_TESS_END callback except that it takes an additional pointer argument. This pointer is identical to the opaque pointer provided when you call <a href="https://msdn.microsoft.com/3a04363a-c492-4fa5-b312-f2fa2a805782">gluTessBeginPolygon</a>. The function prototype for this callback is: 
				<b>void</b> <b>endData</b> (<b>void</b> * <i>polygon_data</i>);

</td>
</tr>
<tr>
<td>GLU_TESS_COMBINE</td>
<td>Call the GLU_TESS_COMBINE callback to create a new vertex when the tessellation detects an intersection, or to merge features. The function takes four arguments: 
				An array of three elements, each of type Gldouble.

An array of four pointers.

An array of four elements, each of type GLfloat.

A pointer to a pointer.

The function prototype for this callback is: 

<b>void</b> <b>combine</b>(<b>GLdouble</b> <i>coords</i>[3], <b>void</b> * <i>vertex_data</i>[4], <b>GLfloat</b> <i>weight</i>[4], <b>void</b> **<i>outData</i>);

The vertex is defined as a linear combination of up to four existing vertexes, stored in vertex_data. The coefficients of the linear combination are given by weight; these weights always sum to 1.0. All vertex pointers are valid even when some of the weights are zero. The coords parameter gives the location of the new vertex.

Allocate another vertex, interpolate parameters using vertex_data and weight, and return the new vertex pointer in outData. This handle is supplied during rendering callbacks. Free the memory sometime after calling <a href="https://msdn.microsoft.com/c9ae2075-59d7-4c1a-b720-0aa05954525c">gluTessEndPolygon</a>.

For example, if the polygon lies in an arbitrary plane in three-dimensional space, and you associate a color with each vertex, the GLU_TESS_COMBINE callback might look like the following:

<pre xml:space="preserve"><code>void myCombine( GLdouble coords[3], VERTEX *d[4], 
                GLfloat w[4], VERTEX **dataOut ) 
{ 
    VERTEX *newVertex = new_vertex(); 
    newVertex-&gt;x = coords[0]; 
    newVertex-&gt;y = coords[1]; 
    newVertex-&gt;z = coords[2]; 
    newVertex-&gt;r = w[0]*d[0]-&gt;r + w[1]*d[1]-&gt;r + w[2]*d[2]-&gt;r + 
                   w[3]*d[3]-&gt;r; 
    newVertex-&gt;g = w[0]*d[0]-&gt;g + w[1]*d[1]-&gt;g + w[2]*d[2]-&gt;g + 
                   w[3]*d[3]-&gt;g; 
    newVertex-&gt;b = w[0]*d[0]-&gt;b + w[1]*d[1]-&gt;b + w[2]*d[2]-&gt;b + 
                   w[3]*d[3]-&gt;b; 
    newVertex-&gt;a = w[0]*d[0]-&gt;a + w[1]*d[1]-&gt;a + w[2]*d[2]-&gt;a + 
                   w[3]*d[3]-&gt;a; 
    *dataOut = newVertex; 
}</code></pre>
When the tessellation detects an intersection, the GLU_TESS_COMBINE or GLU_TESS_COMBINE_DATA callback (see below) must be defined, and must write a non-<b>NULL</b> pointer into dataOut. Otherwise the GLU_TESS_NEED_COMBINE_CALLBACK error occurs, and no output is generated. (This is the only error that can occur during tessellation and rendering.)

</td>
</tr>
<tr>
<td>GLU_TESS_COMBINE_DATA</td>
<td>The GLU_TESS_COMBINE_DATA callback is the same as the GLU_TESS_COMBINE callback except that it takes an additional pointer argument. This pointer is identical to the opaque pointer provided when you call <a href="https://msdn.microsoft.com/3a04363a-c492-4fa5-b312-f2fa2a805782">gluTessBeginPolygon</a>. The function prototype for this callback is: 
				<b>void</b> <b>combineData</b> (<b>GLdouble</b> <i>coords</i>[3], <b>void</b> *<i>vertex_data</i>[4], <b>GLfloat</b> <i>weight</i>[4], <b>void</b> **<i>outData</i>, <b>void</b> * <i>polygon_data</i>);

</td>
</tr>
<tr>
<td>GLU_TESS_ERROR</td>
<td>The GLU_TESS_ERROR callback is called when an error is encountered. The one argument is of type <b>GLenum</b>; it indicates the specific error that occurred and is set to one of the following: 
				GLU_TESS_MISSING_BEGIN_POLYGON

GLU_TESS_MISSING_END_POLYGON

GLU_TESS_MISSING_BEGIN_CONTOUR

GLU_TESS_MISSING_END_CONTOUR

GLU_TESS_COORD_TOO_LARGE

GLU_TESS_NEED_COMBINE_CALLBACK

Call gluErrorString to retrieve character strings describing these errors. The function prototype for this callback is as follows:

<b>void</b> <b>error</b> (<b>GLenum</b> <i>errno</i>);

The GLU library recovers from the first four errors by inserting the missing call or calls. GLU_TESS_COORD_TOO_LARGE indicates that some vertex coordinate exceeded the predefined constant GLU_TESS_MAX_COORD in absolute value, and that the value has been clamped. (Coordinate values must be small enough that two can be multiplied together without overflow.) GLU_TESS_NEED_COMBINE_CALLBACK indicates that the tessellation detected an intersection between two edges in the input data, and the GLU_TESS_COMBINE or GLU_TESS_COMBINE_DATA callback was not provided. No output will be generated.

</td>
</tr>
<tr>
<td>GLU_TESS_ERROR_DATA</td>
<td>The GLU_TESS_ERROR_DATA callback is the same as the GLU_TESS_ERROR callback, except that it takes an additional pointer argument. This pointer is identical to the opaque pointer provided when you call <a href="https://msdn.microsoft.com/3a04363a-c492-4fa5-b312-f2fa2a805782">gluTessBeginPolygon</a>. The function prototype for this callback is: 
				<b>void</b> <b>errorData</b> (<b>GLenum</b> <i>errno</i>, <b>void</b> * <i>polygon_data</i>);

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/26e4e901-4d91-4d7c-ad07-b4480062a4cb">glEdgeFlag</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/20253760-f9ec-4053-bcde-748178f3b359">glVertex</a>



<a href="https://msdn.microsoft.com/7e1540f7-5e7d-4a3b-8c94-5a6800b17411">gluDeleteTess</a>



<a href="https://msdn.microsoft.com/6d71a6d5-ac00-49f9-a56c-cfeeb88963eb">gluErrorString</a>



<a href="https://msdn.microsoft.com/dfc9fce8-ecab-493b-85ee-6d7487814186">gluNewTess</a>



<a href="https://msdn.microsoft.com/3a04363a-c492-4fa5-b312-f2fa2a805782">gluTessBeginPolygon</a>



<a href="https://msdn.microsoft.com/c9ae2075-59d7-4c1a-b720-0aa05954525c">gluTessEndPolygon</a>



<a href="https://msdn.microsoft.com/9c555b32-5257-4eeb-9323-ccad59591097">gluTessVertex</a>
 

 

