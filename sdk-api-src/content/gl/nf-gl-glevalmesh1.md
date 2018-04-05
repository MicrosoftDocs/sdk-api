---
UID: NF:gl.glEvalMesh1
title: glEvalMesh1 function
author: windows-driver-content
description: Computes a one-dimensional grid of points or lines.
old-location: opengl\glevalmesh1.htm
old-project: OpenGL
ms.assetid: 176a4b81-f1a7-42fc-8ecd-bba77a0ec5b3
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: gl/glEvalMesh1, glEvalMesh1, glEvalMesh1 function [OpenGL], opengl.glevalmesh1
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
-	glEvalMesh1
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glEvalMesh1 function


## -description


Computes a one-dimensional grid of points or lines.


## -parameters




### -param mode

A value that specifies whether to compute a one-dimensional mesh of points or lines. The following symbolic constants are accepted: GL_POINT and GL_LINE. 


### -param i1

The first integer value for grid domain variable i.


### -param i2

The last integer value for grid domain variable i.


## -returns



This function does not return a value.




## -remarks



Use <a href="https://msdn.microsoft.com/87532b49-a506-44a7-be2f-b74c289f1a19">glMapGrid</a> and <a href="https://msdn.microsoft.com/22cb0129-3cbe-4aa6-a3ac-b89576dfe71b">glEvalMesh</a> together to efficiently generate and evaluate a series of evenly spaced map domain values. The <b>glEvalMesh</b> function steps through the integer domain of a one- or two-dimensional grid, whose range is the domain of the evaluation maps specified by <a href="https://msdn.microsoft.com/47b0bd46-aa79-4146-8503-cddcc8b7b242">glMap1</a> and <a href="https://msdn.microsoft.com/8365a9bd-156b-4f57-8ceb-1edcbcea9eb4">glMap2</a>. The mode parameter determines whether the resulting vertices are connected as points, lines, or filled polygons.



In the one-dimensional case, <b>glEvalMesh1</b>, the mesh is generated as if the following code fragment were executed:




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>(<i>type</i>);



for (i = i1; i &lt;= i2; i += 1)

 

{


<a href="https://msdn.microsoft.com/5e884f11-fb3f-4158-8041-6c71509bf7d5">glEvalCoord1</a>(iΔu + u₁)



}




<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>( );



where



Δu = (u₂ u₁) / n



and n, u₁, and u₂ are the arguments to the most recent <a href="https://msdn.microsoft.com/a0bc822e-dd98-4586-a322-2779e11f38ca">glMapGrid1</a> function. The <i>type</i> parameter is GL_POINTS if mode is GL_POINT, or GL_LINES if mode is GL_LINE. The one absolute numeric requirement is that if i = n, then the value computed from iΔu + u₁ is exactly u₂.






## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>
 

 

