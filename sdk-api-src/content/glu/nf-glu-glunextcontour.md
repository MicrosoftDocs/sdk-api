---
UID: NF:glu.gluNextContour
title: gluNextContour function
author: windows-driver-content
description: The gluNextContour function marks the beginning of another contour.
old-location: opengl\glunextcontour.htm
old-project: OpenGL
ms.assetid: 622cd631-3426-4206-9e23-af2a74343da5
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GLU_CCW, GLU_CW, GLU_EXTERIOR, GLU_INTERIOR, GLU_UNKNOWN, _ogl_gluNextContour, glu/gluNextContour, gluNextContour, gluNextContour function [OpenGL], opengl.glunextcontour
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
-	gluNextContour
product: Windows
targetos: Windows
req.lib: Glu32.lib
req.dll: Glu32.dll
req.irql: 
req.product: GDI+ 1.1
---

# gluNextContour function


## -description


<p class="CCE_Message">[The <b>gluNextContour</b> function is obsolete and is provided for backward compatibility only. The <b>gluNextContour</b> function is mapped to <a href="https://msdn.microsoft.com/115db079-cbcb-48e1-8bab-0eb4814afb82">gluTessEndContour</a> followed by <a href="https://msdn.microsoft.com/4008ce9c-86e7-4b24-9bda-5915f469596a">gluTessBeginContour</a>.]

The <b>gluNextContour</b> function marks the beginning of another contour.


## -parameters




### -param tess

The tessellation object (created with <a href="https://msdn.microsoft.com/dfc9fce8-ecab-493b-85ee-6d7487814186">gluNewTess</a>).


### -param type

The type of the contour being defined. The following values are valid.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GLU_EXTERIOR"></a><a id="glu_exterior"></a><dl>
<dt><b>GLU_EXTERIOR</b></dt>
</dl>
</td>
<td width="60%">
An exterior contour defines an exterior boundary of the polygon.

</td>
</tr>
<tr>
<td width="40%"><a id="GLU_INTERIOR"></a><a id="glu_interior"></a><dl>
<dt><b>GLU_INTERIOR</b></dt>
</dl>
</td>
<td width="60%">
An interior contour defines an interior boundary of the polygon (such as a hole).

</td>
</tr>
<tr>
<td width="40%"><a id="GLU_UNKNOWN"></a><a id="glu_unknown"></a><dl>
<dt><b>GLU_UNKNOWN</b></dt>
</dl>
</td>
<td width="60%">
An unknown contour is analyzed by the library to determine whether it is interior or exterior.

</td>
</tr>
<tr>
<td width="40%"><a id="GLU_CCW__GLU_CW"></a><a id="glu_ccw__glu_cw"></a><dl>
<dt><b>GLU_CCW, GLU_CW</b></dt>
</dl>
</td>
<td width="60%">
The first GLU_CCW or GLU_CW contour defined is considered to be exterior. All other contours are considered to be exterior if they are oriented in the same direction (clockwise or counterclockwise) as the first contour, and interior if they are not.

If one contour is of type GLU_CCW or GLU_CW, then all contours must be of the same type (if they are not, then all GLU_CCW and GLU_CW contours will be changed to GLU_UNKNOWN). Note that there is no real difference between the GLU_CCW and GLU_CW contour types.

</td>
</tr>
</table>
 


## -returns



This function does not return a value.




## -remarks



Use the <b>gluNextContour</b> function to describe polygons with multiple contours. After you describe the first contour through a series of <a href="https://msdn.microsoft.com/9c555b32-5257-4eeb-9323-ccad59591097">gluTessVertex</a> calls, a <b>gluNextContour</b> call indicates that the previous contour is complete and that the next contour is about to begin. Perform another series of <b>gluTessVertex</b> calls to describe the new contour. Repeat this process until all contours have been described.

The <i>type</i> parameter defines what type of contour follows.

To define the type of the first contour, you can call <b>gluNextContour</b> before describing the first contour. If you do not call <b>gluNextContour</b> before the first contour, the first contour is marked GLU_EXTERIOR.
        


#### Examples

You can describe a quadrilateral with a triangular hole in it as follows:

<pre class="syntax" xml:space="preserve"><code>gluBeginPolygon(tess); 
    gluTessVertex(tess, v1, v1); 
    gluTessVertex(tess, v2, v2); 
    gluTessVertex(tess, v3, v3); 
    gluTessVertex(tess, v4, v4);  
gluNextContour(tess, GLU_INTERIOR); 
    gluTessVertex(tess, v5, v5); 
    gluTessVertex(tess, v6, v6); 
    gluTessVertex(tess, v7, v7);  
gluEndPolygon(tess);</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/dfc9fce8-ecab-493b-85ee-6d7487814186">gluNewTess</a>



<a href="https://msdn.microsoft.com/4008ce9c-86e7-4b24-9bda-5915f469596a">gluTessBeginContour</a>



<a href="https://msdn.microsoft.com/e4da731c-2082-4dbc-ae3a-8d6b30d50253">gluTessBeginPolygon</a>



<a href="https://msdn.microsoft.com/a9709919-d34c-42c4-82b8-6a503f2b39b0">gluTessCallback</a>



<a href="https://msdn.microsoft.com/115db079-cbcb-48e1-8bab-0eb4814afb82">gluTessEndContour</a>



<a href="https://msdn.microsoft.com/9c555b32-5257-4eeb-9323-ccad59591097">gluTessVertex</a>
 

 

