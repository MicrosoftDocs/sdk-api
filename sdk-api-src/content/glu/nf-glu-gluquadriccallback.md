---
UID: NF:glu.gluQuadricCallback
title: gluQuadricCallback function
author: windows-driver-content
description: The gluQuadricCallback function defines a callback for a quadric object.
old-location: opengl\gluquadric.htm
old-project: OpenGL
ms.assetid: 1f1e9fe9-7239-419c-92b6-af2534850ac5
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GLU_ERROR, _ogl_gluQuadricCallback, glu/gluQuadricCallback, gluQuadricCallback, gluQuadricCallback function [OpenGL], opengl.gluquadric
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
-	gluQuadricCallback
product: Windows
targetos: Windows
req.lib: Glu32.lib
req.dll: Glu32.dll
req.irql: 
req.product: GDI+ 1.1
---

# gluQuadricCallback function


## -description


The <b>gluQuadricCallback</b> function defines a callback for a quadric object.


## -parameters




### -param qobj

The quadric object (created with <a href="https://msdn.microsoft.com/5a4289bf-b57a-4c74-b0e3-b7536671e4df">gluNewQuadric</a>).


### -param which

The callback being defined. The only valid value is GLU_ERROR.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GLU_ERROR"></a><a id="glu_error"></a><dl>
<dt><b>GLU_ERROR</b></dt>
</dl>
</td>
<td width="60%">
The <b>gluQuadricCallback</b> function is called when an error is encountered. Its single argument is of type <b>GLenum</b>, and it indicates the specific error that occurred. Character strings describing these errors can be retrieved with the <a href="https://msdn.microsoft.com/6d71a6d5-ac00-49f9-a56c-cfeeb88963eb">gluErrorString</a> call.

</td>
</tr>
</table>
 


### -param fn

The function to be called.


## -returns



This function does not return a value.




## -remarks



Use <b>gluQuadricCallback</b> to define a new callback to be used by a quadric object. If the specified callback is already defined, it is replaced. If <i>fn</i> is <b>NULL</b>, any existing callback is erased.




## -see-also




<a href="https://msdn.microsoft.com/6d71a6d5-ac00-49f9-a56c-cfeeb88963eb">gluErrorString</a>



<a href="https://msdn.microsoft.com/5a4289bf-b57a-4c74-b0e3-b7536671e4df">gluNewQuadric</a>
 

 

