---
UID: NF:gl.glColorMaterial
title: glColorMaterial function
author: windows-driver-content
description: The glColorMaterial function causes a material color to track the current color.
old-location: opengl\glcolormaterial.htm
old-project: OpenGL
ms.assetid: 6dbef2c2-f902-4f25-8a87-9e3d710dd807
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_glColorMaterial, gl/glColorMaterial, glColorMaterial, glColorMaterial function [OpenGL], opengl.glcolormaterial"
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
-	opengl32.dll
api_name:
-	glColorMaterial
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glColorMaterial function


## -description


The <b>glColorMaterial</b> function causes a material color to track the current color.


## -parameters




### -param face

Specifies whether front, back, or both front and back material parameters should track the current color. Accepted values are GL_FRONT, GL_BACK, and GL_FRONT_AND_BACK. The default value is GL_FRONT_AND_BACK.


### -param mode

Specifies which of several material parameters track the current color. Accepted values are GL_EMISSION, GL_AMBIENT, GL_DIFFUSE, GL_SPECULAR, and GL_AMBIENT_AND_DIFFUSE. The default value is GL_AMBIENT_AND_DIFFUSE.


## -returns



This function does not return a value.




## -remarks



The <b>glColorMaterial</b> function specifies which material parameters track the current color. When you enable GL_COLOR_MATERIAL, for each of the material or materials specified by <i>face</i>, the material parameter or parameters specified by <i>mode</i> track the current color at all times. Enable and disable GL_COLOR_MATERIAL with the functions <a href="https://msdn.microsoft.com/cd4590dd-ae41-47c9-9861-10d72318840f">glEnable</a> and <a href="https://msdn.microsoft.com/094f730e-5e2b-485e-8d9d-fee2902d3d5f">glDisable</a>, which you call with GL_COLOR_MATERIAL as their argument. By default, GL_COLOR_MATERIAL is disabled.

With <b>glColorMaterial</b>, you can change a subset of material parameters for each vertex using only the <a href="https://msdn.microsoft.com/916eb8b5-65c2-4523-bdb5-e609ad7a24a0">glColor</a> function, without calling <a href="https://msdn.microsoft.com/a3f55129-da54-48ca-a629-88fed936551e">glMaterial</a>. If you are going to specify only such a subset of parameters for each vertex, it is better to do so with <b>glColorMaterial</b> than with <b>glMaterial</b>.

The following functions retrieve information related to <b>glColorMaterial</b>:


<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a> with argument GL_COLOR_MATERIAL_PARAMETER

<b>glGet</b> with argument GL_COLOR_MATERIAL_FACE


<a href="https://msdn.microsoft.com/18df5a6f-dc21-434d-a2e8-2c58597df037">glIsEnabled</a> with argument GL_COLOR_MATERIAL




## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/916eb8b5-65c2-4523-bdb5-e609ad7a24a0">glColor</a>



<a href="https://msdn.microsoft.com/094f730e-5e2b-485e-8d9d-fee2902d3d5f">glDisable</a>



<a href="https://msdn.microsoft.com/cd4590dd-ae41-47c9-9861-10d72318840f">glEnable</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a>



<a href="https://msdn.microsoft.com/18df5a6f-dc21-434d-a2e8-2c58597df037">glIsEnabled</a>



<a href="https://msdn.microsoft.com/004f0f53-4c72-48df-8231-6b39df464061">glLight</a>



<a href="https://msdn.microsoft.com/8214765c-5722-4df0-88ed-3a5ac039aac4">glLightModel</a>



<a href="https://msdn.microsoft.com/a3f55129-da54-48ca-a629-88fed936551e">glMaterial</a>
 

 

