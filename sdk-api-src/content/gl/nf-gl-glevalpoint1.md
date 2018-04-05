---
UID: NF:gl.glEvalPoint1
title: glEvalPoint1 function
author: windows-driver-content
description: The glEvalPoint1 and glEvalPoint2 functions generate and evaluate a single point in a mesh.
old-location: opengl\glevalpoint1.htm
old-project: OpenGL
ms.assetid: 5ef1d2f0-d77b-4bb8-a0d4-45c1a6a91c18
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: gl/glEvalPoint1, glEvalPoint1, glEvalPoint1 function [OpenGL], opengl.glevalpoint1
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
-	glEvalPoint1
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glEvalPoint1 function


## -description


The <a href="https://msdn.microsoft.com/0cc70e14-eb22-4d04-a6c1-3943933a558e">glEvalPoint1</a> and <b>glEvalPoint2</b> functions generate and evaluate a single point in a mesh.


## -parameters




### -param i

The integer value for grid domain variable <i>i</i>.


## -returns



This function does not return a value.




## -remarks



The <a href="https://msdn.microsoft.com/87532b49-a506-44a7-be2f-b74c289f1a19">glMapGrid</a> and <a href="https://msdn.microsoft.com/22cb0129-3cbe-4aa6-a3ac-b89576dfe71b">glEvalMesh</a> functions are used in tandem to efficiently generate and evaluate a series of evenly spaced map domain values. You can use <b>glEvalPoint</b> to evaluate a single grid point in the same gridspace that is traversed by <b>glEvalMesh</b>. Calling <a href="https://msdn.microsoft.com/0cc70e14-eb22-4d04-a6c1-3943933a558e">glEvalPoint1</a> is equivalent to calling

<b>glEvalCoord1</b> (<i>i</i> Δ<i>u</i> +<i>u</i>₁ );

where

Δ<i>u</i> = (<i>u</i>₂ <i>u</i>₁ )/<i>n</i>

and <i>n</i>, <i>u</i>₁ , and <i>u</i>₂ are the arguments to the most recent <b>glMapGrid1</b> function. The one absolute numeric requirement is that if <i>i</i> = <i>n</i>, then the value computed from (<i>i</i> Δ<i>u</i> + <i></i>u₁ ) is exactly <i>u</i>₂ .

In the two-dimensional case, <b>glEvalPoint2</b>, let

Δ<i>u</i> = (<i>u</i>₂ <i>u</i>₁ )/<i>n</i>

Δ<i>v</i> = (<i>v</i>₂ <i>v</i>₁ )/<i>m</i>

where <i>n</i>, <i>u</i>₁ , <i>u</i>₂ , <i>m</i>, <i>v</i>₁ , and <i>v</i>₂  are the arguments to the most recent <b>glMapGrid2</b> function. Then the <b>glEvalPoint2</b> function is equivalent to calling

<b>glEvalCoord2</b> (<i>i</i> Δ<i>u</i> + <i>u</i>₁ , <i>j</i> Δ<i>v</i> + <i>v</i>₁ );

The only absolute numeric requirements are that if <i>i</i>=<i>n</i>, then the value computed from (<i>i</i> Δ<i>u</i> + <i>u</i>₁ ) is exactly <i></i>u₂ , and if <i>j</i> = <i>m</i>, then the value computed from (<i>j</i> Δ<i>v</i> + <i>v</i>₁  ) is exactly <i>v</i>₂ .

The following functions retrieve information relating to <a href="https://msdn.microsoft.com/0cc70e14-eb22-4d04-a6c1-3943933a558e">glEvalPoint1</a> and <b>glEvalPoint2</b>:


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_MAP1_GRID_DOMAIN

<b>glGet</b> with argument GL_MAP2_GRID_DOMAIN

<b>glGet</b> with argument GL_MAP1_GRID_SEGMENTS

<b>glGet</b> with argument GL_MAP2_GRID_SEGMENTS




## -see-also




<a href="https://msdn.microsoft.com/a170a84f-780a-42a5-a085-9ce355cf8825">glEvalCoord</a>



<a href="https://msdn.microsoft.com/22cb0129-3cbe-4aa6-a3ac-b89576dfe71b">glEvalMesh</a>



<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a>



<a href="https://msdn.microsoft.com/47b0bd46-aa79-4146-8503-cddcc8b7b242">glMap1</a>



<a href="https://msdn.microsoft.com/8365a9bd-156b-4f57-8ceb-1edcbcea9eb4">glMap2</a>



<a href="https://msdn.microsoft.com/87532b49-a506-44a7-be2f-b74c289f1a19">glMapGrid</a>
 

 

