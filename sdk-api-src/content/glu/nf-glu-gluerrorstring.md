---
UID: NF:glu.gluErrorString
title: gluErrorString function
author: windows-driver-content
description: The gluErrorString function produces an error string from an OpenGL or GLU error code. The error string is ANSI only.
old-location: opengl\gluerrorstring.htm
old-project: OpenGL
ms.assetid: 6d71a6d5-ac00-49f9-a56c-cfeeb88963eb
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_gluErrorString, glu/gluErrorString, gluErrorString, gluErrorString function [OpenGL], opengl.gluerrorstring"
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
-	gluErrorString
product: Windows
targetos: Windows
req.lib: Glu32.lib
req.dll: Glu32.dll
req.irql: 
req.product: GDI+ 1.1
---

# gluErrorString function


## -description


The <b>gluErrorString</b> function produces an error string from an OpenGL or GLU error code. The error string is ANSI only.


## -parameters




### -param errCode

An OpenGL or GLU error code.


## -remarks



The <b>gluErrorString</b> function produces an error string from an OpenGL or GLU error code. The string is in an ISO Latin 1 format. For example, <b>gluErrorString</b>(GL_OUT_OF_MEMORY) returns the string "out of memory".

The standard GLU error codes are GLU_INVALID_ENUM, GLU_INVALID_VALUE, and GLU_OUT_OF_MEMORY. Certain other GLU functions can return specialized error codes through callbacks. For the list of OpenGL error codes, see <a href="https://msdn.microsoft.com/18f0368f-054f-4b84-8397-3f9ee4aa07fa">glGetError</a>.

The <b>gluErrorString</b> function produces error strings in ANSI only. Whenever possible, use <b>gluErrorStringWIN</b>, which allows ANSI or Unicode error strings. This makes it easier to localize your program for use with another language.




## -see-also




<a href="https://msdn.microsoft.com/18f0368f-054f-4b84-8397-3f9ee4aa07fa">glGetError</a>



<a href="https://msdn.microsoft.com/1e9afc00-57c6-459e-a9fc-463f45df2084">gluNurbsCallback</a>



<a href="https://msdn.microsoft.com/1f1e9fe9-7239-419c-92b6-af2534850ac5">gluQuadricCallback</a>



<a href="https://msdn.microsoft.com/a9709919-d34c-42c4-82b8-6a503f2b39b0">gluTessCallback</a>
 

 

