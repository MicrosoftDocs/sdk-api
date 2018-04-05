---
UID: NF:glu.gluGetString
title: gluGetString function
author: windows-driver-content
description: The gluGetString function gets a string that describes the GLU version number or supported GLU extension calls.
old-location: opengl\glugetstring.htm
old-project: OpenGL
ms.assetid: e6d9ce03-3218-4145-8bb5-3989afe62436
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "_ogl_gluGetString, glu/gluGetString, gluGetString, gluGetString function [OpenGL], opengl.glugetstring"
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
-	gluGetString
product: Windows
targetos: Windows
req.lib: Glu32.lib
req.dll: Glu32.dll
req.irql: 
req.product: GDI+ 1.1
---

# gluGetString function


## -description


The <b>gluGetString</b> function gets a string that describes the GLU version number or supported GLU extension calls.


## -parameters




### -param name

Either the version number of GLU (GLU_VERSION) or available vendor-specific extension calls (GLU_EXTENSIONS).


## -remarks



The <b>gluGetString</b> function returns a pointer to a static, null-terminated string. When <i>name</i> is GLU_VERSION, the returned string is a value that represents the version number of GLU. The format of the version number is as follows:

<pre class="syntax" xml:space="preserve"><code>&lt;version number&gt;&lt;space&gt;&lt;vendor-specific information&gt; 
(for example, "1.2.11 Microsoft Windows")</code></pre>
The version number has the form "major_number.minor_number" or "major_number.minor_number.release_number". The vendor-specific information is optional, and the format and contents depend on the implementation.

When <i>name</i> is GLU_EXTENSIONS, the returned string contains a list of names of supported GLU extensions that are separated by spaces. The format of the returned list of names is as follows:

<pre class="syntax" xml:space="preserve"><code>&lt;extension_name&gt;&lt;space&gt;&lt;extension_name&gt;&lt;space&gt; . . .
(for example, "GLU_NURBS GL_TESSELATION")</code></pre>
The extension names cannot contain any spaces.

The <b>gluGetString</b> function is valid for GLU version 1.1 or later.



