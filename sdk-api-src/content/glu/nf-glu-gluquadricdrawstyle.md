---
UID: NF:glu.gluQuadricDrawStyle
title: gluQuadricDrawStyle function
author: windows-driver-content
description: The gluQuadricDrawStyle function specifies the draw style desired for quadrics.
old-location: opengl\gluquadricdrawstyle.htm
old-project: OpenGL
ms.assetid: 30f6da40-9306-46bb-a815-f51722e57e18
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GLU_FILL, GLU_LINE, GLU_POINT, GLU_SILHOUETTE, _ogl_gluQuadricDrawStyle, glu/gluQuadricDrawStyle, gluQuadricDrawStyle, gluQuadricDrawStyle function [OpenGL], opengl.gluquadricdrawstyle
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
-	gluQuadricDrawStyle
product: Windows
targetos: Windows
req.lib: Glu32.lib
req.dll: Glu32.dll
req.irql: 
req.product: GDI+ 1.1
---

# gluQuadricDrawStyle function


## -description


The <b>gluQuadricDrawStyle</b> function specifies the draw style desired for quadrics.


## -parameters




### -param quadObject

The quadric object (created with <a href="https://msdn.microsoft.com/5a4289bf-b57a-4c74-b0e3-b7536671e4df">gluNewQuadric</a>).


### -param drawStyle

The desired draw style. The following values are valid.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GLU_FILL"></a><a id="glu_fill"></a><dl>
<dt><b>GLU_FILL</b></dt>
</dl>
</td>
<td width="60%">
Quadrics are rendered with polygon primitives. The polygons are drawn in a counterclockwise fashion with respect to their normals (as defined with <a href="https://msdn.microsoft.com/4e3fc6d3-5a39-455b-bd24-8eb497333096">gluQuadricOrientation</a>).

</td>
</tr>
<tr>
<td width="40%"><a id="GLU_LINE"></a><a id="glu_line"></a><dl>
<dt><b>GLU_LINE</b></dt>
</dl>
</td>
<td width="60%">
Quadrics are rendered as a set of lines.

</td>
</tr>
<tr>
<td width="40%"><a id="GLU_SILHOUETTE"></a><a id="glu_silhouette"></a><dl>
<dt><b>GLU_SILHOUETTE</b></dt>
</dl>
</td>
<td width="60%">
Quadrics are rendered as a set of lines, except that edges separating coplanar faces will not be drawn.

</td>
</tr>
<tr>
<td width="40%"><a id="GLU_POINT"></a><a id="glu_point"></a><dl>
<dt><b>GLU_POINT</b></dt>
</dl>
</td>
<td width="60%">
Quadrics are rendered as a set of points.

</td>
</tr>
</table>
 


## -returns



This function does not return a value.




## -remarks



The <b>gluQuadricDrawStyle</b> function specifies the draw style for quadrics rendered with <b>quadObject</b>.




## -see-also




<a href="https://msdn.microsoft.com/5a4289bf-b57a-4c74-b0e3-b7536671e4df">gluNewQuadric</a>



<a href="https://msdn.microsoft.com/945759ec-ed4a-480f-8243-49fc785867c1">gluQuadricNormals</a>



<a href="https://msdn.microsoft.com/4e3fc6d3-5a39-455b-bd24-8eb497333096">gluQuadricOrientation</a>



<a href="https://msdn.microsoft.com/11681497-f099-4856-a0ac-6a44abd3e1a1">gluQuadricTexture</a>
 

 

