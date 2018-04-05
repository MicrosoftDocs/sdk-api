---
UID: NF:gl.glGetMapdv
title: glGetMapdv function
author: windows-driver-content
description: The glGetMapdv, glGetMapfv, and glGetMapiv functions return evaluator parameters.
old-location: opengl\glgetmapdv.htm
old-project: OpenGL
ms.assetid: 3b4fc03b-ada4-4f4a-a234-fa6439f2e5c8
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GL_COEFF, GL_DOMAIN, GL_ORDER, gl/glGetMapdv, glGetMapdv, glGetMapdv function [OpenGL], opengl.glgetmapdv
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
-	glGetMapdv
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glGetMapdv function


## -description


The <b>glGetMapdv</b>, <a href="https://msdn.microsoft.com/dc93e468-7b76-4b5d-a46c-63920ed05568">glGetMapfv</a>, and <a href="https://msdn.microsoft.com/bc055451-7c20-4a8a-96dd-55c877700714">glGetMapiv</a> functions return evaluator parameters.


## -parameters




### -param target

The symbolic name of a map. The following are accepted values: GL_MAP1_COLOR_4, GL_MAP1_INDEX, GL_MAP1_NORMAL, GL_MAP1_TEXTURE_COORD_1, GL_MAP1_TEXTURE_COORD_2, GL_MAP1_TEXTURE_COORD_3, GL_MAP1_TEXTURE_COORD_4, GL_MAP1_VERTEX_3, GL_MAP1_VERTEX_4, GL_MAP2_COLOR_4, GL_MAP2_INDEX, GL_MAP2_NORMAL, GL_MAP2_TEXTURE_COORD_1, GL_MAP2_TEXTURE_COORD_2, GL_MAP2_TEXTURE_COORD_3, GL_MAP2_TEXTURE_COORD_4, GL_MAP2_VERTEX_3, and GL_MAP2_VERTEX_4.


### -param query

Specifies which parameter to return. The following symbolic names are accepted.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GL_COEFF"></a><a id="gl_coeff"></a><dl>
<dt><b>GL_COEFF</b></dt>
</dl>
</td>
<td width="60%">
The <i>v</i> parameter returns the control points for the evaluator function. One-dimensional evaluators return <i>order</i> control points, and two-dimensional evaluators return <i>uorder</i> <i>x</i> <i>vorder</i> control points. Each control point consists of one, two, three, or four integer, single-precision floating-point, or double-precision floating-point values, depending on the type of the evaluator. Two-dimensional control points are returned in row-major order, incrementing the <i>uorder</i> index quickly, and the <i>vorder</i> index after each row. Integer values, when requested, are computed by rounding the internal floating-point values to the nearest integer values.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_ORDER"></a><a id="gl_order"></a><dl>
<dt><b>GL_ORDER</b></dt>
</dl>
</td>
<td width="60%">
The <i>v</i> parameter returns the order of the evaluator function. One-dimensional evaluators return a single value, <i>order</i>. Two-dimensional evaluators return two values, <i>uorder</i> and <i>vorder</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_DOMAIN"></a><a id="gl_domain"></a><dl>
<dt><b>GL_DOMAIN</b></dt>
</dl>
</td>
<td width="60%">
The <i>v</i> parameter returns the linear <i>u</i> and <i>v</i> mapping parameters. One-dimensional evaluators return two values, <i>u</i> 1 and <i>u</i> 2, as specified by <a href="https://msdn.microsoft.com/47b0bd46-aa79-4146-8503-cddcc8b7b242">glMap1</a>. Two-dimensional evaluators return four values (<i>u1</i>, <i>u2</i>, <i>v1</i>, and <i>v2</i>) as specified by <a href="https://msdn.microsoft.com/8365a9bd-156b-4f57-8ceb-1edcbcea9eb4">glMap2</a>. Integer values, when requested, are computed by rounding the internal floating-point values to the nearest integer values.

</td>
</tr>
</table>
 


### -param v

Returns the requested data.


## -returns



This function does not return a value.




## -remarks



The <b>glGetMap</b> function returns evaluator parameters. (The <b>glMap1</b> and <b>glMap2</b> functions define evaluators.) The <i>target</i> parameter specifies a map, <i>query</i> selects a specific parameter, and <i>v</i> points to storage where the values will be returned.

The acceptable values for the <i>target</i> parameter are described in <a href="https://msdn.microsoft.com/47b0bd46-aa79-4146-8503-cddcc8b7b242">glMap1</a> and <a href="https://msdn.microsoft.com/8365a9bd-156b-4f57-8ceb-1edcbcea9eb4">glMap2</a>.

If an error is generated, no change is made to the contents of <i>v</i>.




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/a170a84f-780a-42a5-a085-9ce355cf8825">glEvalCoord</a>



<a href="https://msdn.microsoft.com/47b0bd46-aa79-4146-8503-cddcc8b7b242">glMap1</a>



<a href="https://msdn.microsoft.com/8365a9bd-156b-4f57-8ceb-1edcbcea9eb4">glMap2</a>
 

 

