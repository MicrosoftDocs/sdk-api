---
UID: NF:glu.gluQuadricOrientation
title: gluQuadricOrientation function
author: windows-driver-content
description: The gluQuadricOrientation function specifies inside or outside orientation for quadrics.
old-location: opengl\gluquadricorientation.htm
old-project: OpenGL
ms.assetid: 4e3fc6d3-5a39-455b-bd24-8eb497333096
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GLU_INSIDE, GLU_OUTSIDE, _ogl_gluQuadricOrientation, glu/gluQuadricOrientation, gluQuadricOrientation, gluQuadricOrientation function [OpenGL], opengl.gluquadricorientation
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
-	gluQuadricOrientation
product: Windows
targetos: Windows
req.lib: Glu32.lib
req.dll: Glu32.dll
req.irql: 
req.product: GDI+ 1.1
---

# gluQuadricOrientation function


## -description


The <b>gluQuadricOrientation</b> function specifies inside or outside orientation for quadrics.


## -parameters




### -param quadObject

The quadric object (created with <a href="https://msdn.microsoft.com/5a4289bf-b57a-4c74-b0e3-b7536671e4df">gluNewQuadric</a>).


### -param orientation

The desired orientation. The following values are valid.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GLU_OUTSIDE"></a><a id="glu_outside"></a><dl>
<dt><b>GLU_OUTSIDE</b></dt>
</dl>
</td>
<td width="60%">
Draw quadrics with normals pointing outward. This is the default value.

</td>
</tr>
<tr>
<td width="40%"><a id="GLU_INSIDE"></a><a id="glu_inside"></a><dl>
<dt><b>GLU_INSIDE</b></dt>
</dl>
</td>
<td width="60%">
Draw quadrics with normals pointing inward.

</td>
</tr>
</table>
 


## -returns



This function does not return a value.




## -remarks



The <b>gluQuadricOrientation</b> function specifies what kind of orientation is desired for quadrics rendered with <b>quadObject</b>. The interpretation of outward and inward depends on the quadric being drawn.




## -see-also




<a href="https://msdn.microsoft.com/5a4289bf-b57a-4c74-b0e3-b7536671e4df">gluNewQuadric</a>



<a href="https://msdn.microsoft.com/30f6da40-9306-46bb-a815-f51722e57e18">gluQuadricDrawStyle</a>



<a href="https://msdn.microsoft.com/945759ec-ed4a-480f-8243-49fc785867c1">gluQuadricNormals</a>



<a href="https://msdn.microsoft.com/11681497-f099-4856-a0ac-6a44abd3e1a1">gluQuadricTexture</a>
 

 

