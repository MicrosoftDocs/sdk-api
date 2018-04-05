---
UID: NF:glu.gluTessProperty
title: gluTessProperty function
author: windows-driver-content
description: The gluTessProperty function sets the property of a tessellation object.
old-location: opengl\glutessproperty.htm
old-project: OpenGL
ms.assetid: 1306b9ef-4f1e-4684-99ea-464bae1d0a61
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GLU_TESS_BOUNDARY_ONLY, GLU_TESS_TOLERANCE, GLU_TESS_WINDING_RULE, _ogl_gluTessProperty, glu/gluTessProperty, gluTessProperty, gluTessProperty function [OpenGL], opengl.glutessproperty
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
-	gluTessProperty
product: Windows
targetos: Windows
req.lib: Glu32.lib
req.dll: Glu32.dll
req.irql: 
req.product: GDI+ 1.1
---

# gluTessProperty function


## -description


The <b>gluTessProperty</b> function sets the property of a tessellation object.


## -parameters




### -param tess

The tessellation object (created with <a href="https://msdn.microsoft.com/dfc9fce8-ecab-493b-85ee-6d7487814186">gluNewTess</a>).


### -param which

The property value to set. The following values are valid: GLU_TESS_WINDING_RULE, GLU_TESS_BOUNDARY_ONLY, and GLU_TESS_TOLERANCE.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GLU_TESS_WINDING_RULE"></a><a id="glu_tess_winding_rule"></a><dl>
<dt><b>GLU_TESS_WINDING_RULE</b></dt>
</dl>
</td>
<td width="60%">
Determines which parts of the polygon are on the interior. The value parameter may be set to one of the following: GLU_TESS_WINDING_ODD, GLU_TESS_WINDING_NONZERO, GLU_TESS_WINDING_POSITIVE, GLU_TESS_WINDING_NEGATIVE, or GLU_TESS_WINDING_ABS_GEQ_TWO. 
		  

To understand how the winding rule works, first consider that the input contours partition the plane into regions. The winding rule determines which of these regions are inside the polygon.

For a single-contour C, the winding number of a point x is simply the signed number of revolutions we make around x as we travel once around C (where counterclockwise is positive). When there are several contours, the individual winding numbers are summed. This procedure associates a signed integer value with each point x in the plane. Note that the winding number is the same for all points in a single region.

The winding rule classifies a region as "inside" if its winding number belongs to the chosen category (odd, nonzero, positive, negative, or absolute value of at least two). The previous GLU tessellator (prior to GLU 1.2) used the "odd" rule. The "nonzero" rule (GLU_TESS_WINDING_NONZERO) is another common way to define the interior. The other three rules (GLU_TESS_WINDING_POSITIVE, GLU_TESS_WINDING_NEGATIVE, GLU_TESS_WINDING_ABS_GEQ_TWO) are useful for polygon CSG operations.

</td>
</tr>
<tr>
<td width="40%"><a id="GLU_TESS_BOUNDARY_ONLY"></a><a id="glu_tess_boundary_only"></a><dl>
<dt><b>GLU_TESS_BOUNDARY_ONLY</b></dt>
</dl>
</td>
<td width="60%">
Specifies a Boolean value (set value to GL_TRUE or GL_FALSE). When you set value to GL_TRUE, a set of closed contours separating the polygon interior and exterior is returned instead of a tessellation. Exterior contours are oriented counterclockwise with respect to the normal; interior contours are oriented clockwise. The GLU_TESS_BEGIN and GLU_TESS_BEGIN_DATA callbacks use the type GL_LINE_LOOP for each contour.

</td>
</tr>
<tr>
<td width="40%"><a id="GLU_TESS_TOLERANCE"></a><a id="glu_tess_tolerance"></a><dl>
<dt><b>GLU_TESS_TOLERANCE</b></dt>
</dl>
</td>
<td width="60%">
Specifies a tolerance for merging features to reduce the size of the output. For example, two vertexes that are very close to each other might be replaced by a single vertex. The tolerance is multiplied by the largest coordinate magnitude of any input vertex; this specifies the maximum distance that any feature can move as the result of a single merge operation. If a single feature takes part in several merge operations, the total distance moved can be larger. 
		  

Feature merging is completely optional; the tolerance is only a hint. The implementation is free to merge in some cases and not in others, or to never merge features at all. The default tolerance is zero.

The current implementation merges vertexes only if they are exactly coincident, regardless of the current tolerance. A vertex is spliced into an edge only if the implementation is unable to distinguish which side of the edge the vertex lies on. Two edges are merged only when both endpoints are identical.

</td>
</tr>
</table>
 


### -param value

The value of the indicated property.


## -returns



This function does not return a value.




## -remarks



The <b>gluTessProperty</b> function controls properties stored in a tessellation object. These properties affect the way the polygons are interpreted and rendered. 




## -see-also




<a href="https://msdn.microsoft.com/6aa565d8-2257-4259-a959-b7d806a7ed96">gluGetTessProperty</a>



<a href="https://msdn.microsoft.com/dfc9fce8-ecab-493b-85ee-6d7487814186">gluNewTess</a>
 

 

