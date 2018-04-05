---
UID: NF:glu.gluQuadricTexture
title: gluQuadricTexture function
author: windows-driver-content
description: The gluQuadricTexture function specifies whether quadrics are to be textured.
old-location: opengl\gluquadrictexture.htm
old-project: OpenGL
ms.assetid: 11681497-f099-4856-a0ac-6a44abd3e1a1
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GL_FALSE, GL_TRUE, _ogl_gluQuadricTexture, glu/gluQuadricTexture, gluQuadricTexture, gluQuadricTexture function [OpenGL], opengl.gluquadrictexture
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
-	gluQuadricTexture
product: Windows
targetos: Windows
req.lib: Glu32.lib
req.dll: Glu32.dll
req.irql: 
req.product: GDI+ 1.1
---

# gluQuadricTexture function


## -description


The <b>gluQuadricTexture</b> function specifies whether quadrics are to be textured.


## -parameters




### -param quadObject

The quadric object (created with <a href="https://msdn.microsoft.com/5a4289bf-b57a-4c74-b0e3-b7536671e4df">gluNewQuadric</a>).


### -param textureCoords

A flag indicating whether texture coordinates are to be generated. The following values are valid.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GL_TRUE"></a><a id="gl_true"></a><dl>
<dt><b>GL_TRUE</b></dt>
</dl>
</td>
<td width="60%">
Generate texture coordinates.

</td>
</tr>
<tr>
<td width="40%"><a id="GL_FALSE"></a><a id="gl_false"></a><dl>
<dt><b>GL_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Do not generate texture coordinates. This is the default value.

</td>
</tr>
</table>
 


## -returns



This function does not return a value.




## -remarks



The <b>gluQuadricTexture</b> function specifies whether texture coordinates are to be generated for quadrics rendered with <b>quadObject</b>.

The manner in which texture coordinates are generated depends upon the specific quadric rendered.




## -see-also




<a href="https://msdn.microsoft.com/5a4289bf-b57a-4c74-b0e3-b7536671e4df">gluNewQuadric</a>



<a href="https://msdn.microsoft.com/30f6da40-9306-46bb-a815-f51722e57e18">gluQuadricDrawStyle</a>



<a href="https://msdn.microsoft.com/945759ec-ed4a-480f-8243-49fc785867c1">gluQuadricNormals</a>
 

 

