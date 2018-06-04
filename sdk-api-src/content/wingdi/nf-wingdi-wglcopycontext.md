---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# wglCopyContext function


## -description


The <b>wglCopyContext</b> function copies selected groups of rendering states from one OpenGL rendering context to another.


## -parameters




### -param

TBD




#### - hglrcDst

Specifies the destination OpenGL rendering context to which state information is to be copied.


#### - hglrcSrc

Specifies the source OpenGL rendering context whose state information is to be copied.


#### - mask

Specifies which groups of the <i>hglrcSrc</i> rendering state are to be copied to <i>hglrcDst</i>. It contains the bitwise-OR of the same symbolic names that are passed to the <b>glPushAttrib</b> function. You can use GL_ALL_ATTRIB_BITS to copy all the rendering state information.


## -returns



If the function succeeds, the return value is <b>TRUE</b>. If the function fails, the return value is <b>FALSE</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Using the <b>wglCopyContext</b> function, you can synchronize the rendering state of two rendering contexts. You can only copy the rendering state between two rendering contexts within the same process. The rendering contexts must be from the same OpenGL implementation. For example, you can always copy a rendering state between two rendering contexts with identical pixel format in the same process.

You can copy the same state information available only with the <b>glPushAttrib</b> function. You cannot copy some state information, such as pixel pack/unpack state, render mode state, select state, and feedback state. When you call <b>wglCopyContext</b>, make sure that the destination rendering context, <i>hglrcDst</i>, is not current to any thread.




## -see-also




<a href="https://msdn.microsoft.com/589a86f1-598d-4175-97fc-27ca0b254935">OpenGL on Windows</a>



<a href="https://msdn.microsoft.com/52053370-d88b-4faf-bdcd-4663c6d5270d">WGL Functions</a>



<a href="https://msdn.microsoft.com/3c7b93cc-2112-4771-b422-a244821447e5">glPushAttrib</a>



<a href="https://msdn.microsoft.com/fa9ed944-f917-4fdf-a52a-10a7ade8f2ca">wglCreateContext</a>



<a href="https://msdn.microsoft.com/81050b48-7385-4ef3-acc5-82d5c893b2e8">wglCreateLayerContext</a>



<a href="https://msdn.microsoft.com/587ea116-c70b-41ca-bf9b-a0c666f4e948">wglShareLists</a>
 

 

