---
UID: NF:gl.glRasterPos2d
title: glRasterPos2d function
author: windows-driver-content
description: Specifies the raster position for pixel operations.
old-location: opengl\glrasterpos2d.htm
old-project: OpenGL
ms.assetid: 3aad4085-8957-433c-8822-765df6278af8
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: gl/glRasterPos2d, glRasterPos2d, glRasterPos2d function [OpenGL], opengl.glrasterpos2d
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
-	glRasterPos2d
product: Windows
targetos: Windows
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
req.product: GDI+ 1.1
---

# glRasterPos2d function


## -description


Specifies the raster position for pixel operations.


## -parameters




### -param x

Specifies the x-coordinate for the current raster position.


### -param y

Specifies the y-coordinate for the current raster position.


## -returns



This function does not return a value.




## -remarks



OpenGL maintains a 3-D position in window coordinates. This position, called the raster position, is maintained with subpixel accuracy. It is used to position pixel and bitmap write operations. See <a href="https://msdn.microsoft.com/3cd8e41b-016b-4610-833a-048b5e50ae7c">glBitmap</a>, <a href="https://msdn.microsoft.com/c4eda64f-a75e-4e6d-984d-af49414b94d8">glDrawPixels</a>, and <a href="https://msdn.microsoft.com/c4055928-7b8b-4d0f-94f3-e3b9c0503308">glCopyPixels</a>.

 

The current raster position consists of three window coordinates (<i>x, y, z</i>), a clip coordinate <i>w</i> value, an eye coordinate distance, a valid bit, and associated color data and texture coordinates. The <i>w</i> coordinate is a clip coordinate, because <i>w</i> is not projected to window coordinates. The <a href="https://msdn.microsoft.com/2a661893-0818-441d-9399-0103560737c3">glRasterPos4</a> function specifies object coordinates <i>x, y, z</i>, and <i>w</i> explicitly. The glRasterPos3 function specifies object coordinates <i>x, y,</i> and <i>z</i> explicitly, while <i>w</i> is implicitly set to one. The glRasterPos2 function uses the argument values for <i>x</i> and <i>y</i> while implicitly setting <i>z</i> and <i>w</i> to zero and one.



The object coordinates presented by <a href="https://msdn.microsoft.com/2a661893-0818-441d-9399-0103560737c3">glRasterPos</a> are treated just like those of a <a href="https://msdn.microsoft.com/20253760-f9ec-4053-bcde-748178f3b359">glVertex</a> command. They are transformed by the current modelview and projection matrices and passed to the clipping stage. If the vertex is not culled, then it is projected and scaled to window coordinates, which become the new current raster position, and the GL_CURRENT_RASTER_POSITION_VALID flag is set. If the vertex is culled, then the valid bit is cleared and the current raster position and associated color and texture coordinates are undefined.



The current raster position also includes some associated color data and texture coordinates. If lighting is enabled, then GL_CURRENT_RASTER_COLOR, in RGBA mode, or the GL_CURRENT_RASTER_INDEX, in color-index mode, is set to the color produced by the lighting calculation (see <a href="https://msdn.microsoft.com/004f0f53-4c72-48df-8231-6b39df464061">glLight</a>, <a href="https://msdn.microsoft.com/8214765c-5722-4df0-88ed-3a5ac039aac4">glLightModel</a>, and <a href="https://msdn.microsoft.com/52985ad7-1d6c-48fc-8f1e-4eb2c0324c8e">glShadeModel</a>). If lighting is disabled, current color (in RGBA mode, state variable GL_CURRENT_COLOR) or color index (in color-index mode, state variable GL_CURRENT_INDEX) is used to update the current raster color.



Likewise, GL_CURRENT_RASTER_TEXTURE_COORDS is updated as a function of GL_CURRENT_TEXTURE_COORDS, based on the texture matrix and the texture generation functions (see <a href="https://msdn.microsoft.com/958c2932-c220-412c-a85e-eed613332dea">glTexGen</a>). Finally, the distance from the origin of the eye coordinate system to the vertex, as transformed by only the modelview matrix, replaces GL_CURRENT_RASTER_DISTANCE.



Initially, the current raster position is (0,0,0,1), the current raster distance is 0, the valid bit is set, the associated RGBA color is (1,1,1,1), the associated color index is 1, and the associated texture coordinates are (0, 0, 0, 1). In RGBA mode, GL_CURRENT_RASTER_INDEX is always 1; in color-index mode, the current raster RGBA color always maintains its initial value.



<div class="alert"><b>Note</b>  The raster position is modified both by <a href="https://msdn.microsoft.com/2a661893-0818-441d-9399-0103560737c3">glRasterPos</a> and by <a href="https://msdn.microsoft.com/3cd8e41b-016b-4610-833a-048b5e50ae7c">glBitmap</a>. </div>
<div> </div>
<div class="alert"><b>Note</b>  When the raster position coordinates are invalid, drawing commands that are based on the raster position are ignored (that is, they do not result in changes to the OpenGL state).

</div>
<div> </div>
 

The following functions retrieve information related to <a href="https://msdn.microsoft.com/2a661893-0818-441d-9399-0103560737c3">glRasterPos</a>:



<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a>
<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a>
<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a>
<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a>
<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a>
<a href="https://msdn.microsoft.com/7f5d0084-443a-44f8-98fb-0003627212de">glGet</a>



## -see-also




<a href="https://msdn.microsoft.com/8e8e98f8-89e8-40f5-89c1-492c9e3bbd74">glBegin</a>



<a href="https://msdn.microsoft.com/3cd8e41b-016b-4610-833a-048b5e50ae7c">glBitmap</a>



<a href="https://msdn.microsoft.com/c4055928-7b8b-4d0f-94f3-e3b9c0503308">glCopyPixels</a>



<a href="https://msdn.microsoft.com/c4eda64f-a75e-4e6d-984d-af49414b94d8">glDrawPixels</a>



<a href="https://msdn.microsoft.com/040f8573-683c-4a8a-ae51-66abb0541ac4">glEnd</a>



<a href="https://msdn.microsoft.com/004f0f53-4c72-48df-8231-6b39df464061">glLight</a>



<a href="https://msdn.microsoft.com/8214765c-5722-4df0-88ed-3a5ac039aac4">glLightModel</a>



<a href="https://msdn.microsoft.com/52985ad7-1d6c-48fc-8f1e-4eb2c0324c8e">glShadeModel</a>



<a href="https://msdn.microsoft.com/71eb39f1-e1ad-4b97-83e0-d2670f5a7545">glTexCoord</a>



<a href="https://msdn.microsoft.com/958c2932-c220-412c-a85e-eed613332dea">glTexGen</a>



<a href="https://msdn.microsoft.com/20253760-f9ec-4053-bcde-748178f3b359">glVertex</a>
 

 

