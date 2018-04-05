---
UID: NF:gl.glEvalMesh2
title: glEvalMesh2 function
author: windows-driver-content
description: Computes a two-dimensional grid of points or lines.
old-location: opengl\glevalmesh2.htm
old-project: OpenGL
ms.assetid: 21e94388-903e-4b9d-8e54-9c914d0ce372
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: gl/glEvalMesh2, glEvalMesh2, glEvalMesh2 function [OpenGL], opengl.glevalmesh2
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
-	glEvalMesh2
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glEvalMesh2 function


## -description


Computes a two-dimensional grid of points or lines.


## -parameters




### -param mode

A value that specifies whether to compute a two-dimensional mesh of points, lines, or polygons. The following symbolic constants are accepted: GL_POINT, GL_LINE, and GL_FILL.


### -param i1

The first integer value for grid domain variable i.


### -param i2

The last integer value for grid domain variable i.


### -param j1

The first integer value for grid domain variable j.


### -param j2

The last integer value for grid domain variable j.


## -returns



This function does not return a value.




## -remarks



Use <a href="https://msdn.microsoft.com/87532b49-a506-44a7-be2f-b74c289f1a19">glMapGrid</a> and <a href="https://msdn.microsoft.com/22cb0129-3cbe-4aa6-a3ac-b89576dfe71b">glEvalMesh</a> in tandem to efficiently generate and evaluate a series of evenly spaced map domain values. The <b>glEvalMesh</b> function steps through the integer domain of a one- or two-dimensional grid, whose range is the domain of the evaluation maps specified by <a href="https://msdn.microsoft.com/47b0bd46-aa79-4146-8503-cddcc8b7b242">glMap1</a> and <a href="https://msdn.microsoft.com/8365a9bd-156b-4f57-8ceb-1edcbcea9eb4">glMap2</a>. The mode parameter determines whether the resulting vertices are connected as points, lines, or filled polygons.



In the two-dimensional case, <b>glEvalMesh2</b>, let 



Δ u = (u₂ u₁)/n



Δ v = (v₂ v₁)/m,



where n, u₁, u₂, m, v₁, and v₂ are the arguments to the most recent <a href="https://msdn.microsoft.com/87532b49-a506-44a7-be2f-b74c289f1a19">glMapGrid2</a> function. Then, if <i>mode</i> is GL_FILL, <b>glEvalMesh2</b> is equivalent to:



for (j = j1; j &lt; j2; j += 1)

 

{




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>(GL_QUAD_STRIP);



for (i = i1; i &lt;= i2; i += 1)

 

{


<a href="https://msdn.microsoft.com/95963abc-841a-4154-92d5-5ae3e6de0f97">glEvalCoord2</a>(iΔ u + u1 ( ) , j Δ v + v1);


<a href="https://msdn.microsoft.com/95963abc-841a-4154-92d5-5ae3e6de0f97">glEvalCoord2</a>(iΔ u + u1 ( ) , (j+1) Δ v + v1);



}




<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>( ); 

}



If <i>mode</i> is GL_LINE, then a call to <b>glEvalMesh2</b> is equivalent to:



for (j = j1; j &lt;= j2; j += 1) 



{




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>(GL_LINE_STRIP);



for (i = i1; i &lt;= i2; i += 1)



{


<a href="https://msdn.microsoft.com/95963abc-841a-4154-92d5-5ae3e6de0f97">glEvalCoord2</a>(iΔ u + u1, jΔ v + v1);



}


<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>( );



}



for (i = i1; i &lt;= i2; i += 1) 



{


<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>(GL_LINE_STRIP);



for (j = j1; j &lt;= j1; j += 1)



{




<a href="https://msdn.microsoft.com/95963abc-841a-4154-92d5-5ae3e6de0f97">glEvalCoord2</a>(iΔ u + u1, jΔ v + v1);



}



glEnd( );



}



And finally, if <i>mode</i> is GL_POINT, then a call to <b>glEvalMesh2</b> is equivalent to:


<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>(GL_POINTS);

 

for (j = j1; j &lt;= j2; j += 1)

 

{



for (i = i1; i &lt;= i2; i += 1)

 

{




<a href="https://msdn.microsoft.com/95963abc-841a-4154-92d5-5ae3e6de0f97">glEvalCoord2</a>(iΔ u + u1, jΔ v + v1);



}

 

} 




<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>( );



In all three cases, the only absolute numeric requirements are that if i = n, then the value computed from iΔ u + u₁ is exactly u₂, and if j = m, then the value computed from jΔ v + v₁ is exactly v₂.

The following functions retrieve information relating to <b>glEvalMesh</b>:




<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_MAP1_GRID_DOMAIN


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_MAP2_GRID_DOMAIN


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_MAP1_GRID_SEGMENTS


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_MAP2_GRID_SEGMENTS





