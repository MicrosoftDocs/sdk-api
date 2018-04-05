---
UID: NF:glu.gluQuadricNormals
title: gluQuadricNormals function
author: windows-driver-content
description: The gluQuadricNormals function specifies what kind of normals are to be used for quadrics.
old-location: opengl\gluquadricnormals.htm
old-project: OpenGL
ms.assetid: 945759ec-ed4a-480f-8243-49fc785867c1
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GLU_FLAT, GLU_NONE, GLU_SMOOTH, _ogl_gluQuadricNormals, glu/gluQuadricNormals, gluQuadricNormals, gluQuadricNormals function [OpenGL], opengl.gluquadricnormals
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
-	gluQuadricNormals
product: Windows
targetos: Windows
req.lib: Glu32.lib
req.dll: Glu32.dll
req.irql: 
req.product: GDI+ 1.1
---

# gluQuadricNormals function


## -description


The <b>gluQuadricNormals</b> function specifies what kind of normals are to be used for quadrics.


## -parameters




### -param quadObject

The quadric object (created with <a href="https://msdn.microsoft.com/5a4289bf-b57a-4c74-b0e3-b7536671e4df">gluNewQuadric</a>).


### -param normals

The desired type of normals. The following values are valid.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GLU_NONE"></a><a id="glu_none"></a><dl>
<dt><b>GLU_NONE</b></dt>
</dl>
</td>
<td width="60%">
No normals are generated.

</td>
</tr>
<tr>
<td width="40%"><a id="GLU_FLAT"></a><a id="glu_flat"></a><dl>
<dt><b>GLU_FLAT</b></dt>
</dl>
</td>
<td width="60%">
One normal is generated for every facet of a quadric.

</td>
</tr>
<tr>
<td width="40%"><a id="GLU_SMOOTH"></a><a id="glu_smooth"></a><dl>
<dt><b>GLU_SMOOTH</b></dt>
</dl>
</td>
<td width="60%">
One normal is generated for every vertex of a quadric. This is the default value.

</td>
</tr>
</table>
 


## -returns



This function does not return a value.




## -remarks



The <b>gluQuadricNormals</b> function specifies what kind of normals are to be used for quadrics rendered with <b>quadObject</b>.




## -see-also




<a href="https://msdn.microsoft.com/5a4289bf-b57a-4c74-b0e3-b7536671e4df">gluNewQuadric</a>



<a href="https://msdn.microsoft.com/30f6da40-9306-46bb-a815-f51722e57e18">gluQuadricDrawStyle</a>



<a href="https://msdn.microsoft.com/4e3fc6d3-5a39-455b-bd24-8eb497333096">gluQuadricOrientation</a>



<a href="https://msdn.microsoft.com/11681497-f099-4856-a0ac-6a44abd3e1a1">gluQuadricTexture</a>
 

 

