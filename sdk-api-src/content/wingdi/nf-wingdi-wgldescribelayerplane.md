---
UID: NF:wingdi.wglDescribeLayerPlane
title: wglDescribeLayerPlane function (wingdi.h)
description: The wglDescribeLayerPlane function obtains information about the layer planes of a given pixel format.
helpviewer_keywords: ["_ogl_wglDescribeLayerPlane","opengl.wgldescribelayerplane","wglDescribeLayerPlane","wglDescribeLayerPlane function [OpenGL]","wingdi/wglDescribeLayerPlane"]
old-location: opengl\wgldescribelayerplane.htm
tech.root: OpenGL
ms.assetid: a80d257e-7053-4328-8298-80ed72513837
ms.date: 12/05/2018
ms.keywords: _ogl_wglDescribeLayerPlane, opengl.wgldescribelayerplane, wglDescribeLayerPlane, wglDescribeLayerPlane function [OpenGL], wingdi/wglDescribeLayerPlane
req.header: wingdi.h
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
req.lib: Opengl32.lib
req.dll: Opengl32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - wglDescribeLayerPlane
 - wingdi/wglDescribeLayerPlane
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - opengl32.dll
api_name:
 - wglDescribeLayerPlane
---

# wglDescribeLayerPlane function


## -description

The <b>wglDescribeLayerPlane</b> function obtains information about the layer planes of a given pixel format.

## -parameters

### -param unnamedParam1

Specifies the device context of a window whose layer planes are to be described.

### -param unnamedParam2

Specifies which layer planes of a pixel format are being described.

### -param unnamedParam3

Specifies the overlay or underlay plane. Positive values of <i>iLayerPlane</i> identify overlay planes, where 1 is the first overlay plane over the main plane, 2 is the second overlay plane over the first overlay plane, and so on. Negative values identify underlay planes, where 1 is the first underlay plane under the main plane, 2 is the second underlay plane under the first underlay plane, and so on. The number of overlay and underlay planes is given in the <b>bReserved</b> member of the <a href="/windows/desktop/api/wingdi/ns-wingdi-pixelformatdescriptor">PIXELFORMATDESCRIPTOR</a> structure.

### -param unnamedParam4

Specifies the size, in bytes, of the structure pointed to by <i>plpd</i>. The <b>wglDescribeLayerPlane</b> function stores layer plane data in a <a href="/windows/desktop/api/wingdi/ns-wingdi-layerplanedescriptor">LAYERPLANEDESCRIPTOR</a> structure, and stores no more than <i>nBytes</i> of data. Set the value of <i>nBytes</i> to the size of <b>LAYERPLANEDESCRIPTOR</b>.

### -param unnamedParam5

Points to a <b>LAYERPLANEDESCRIPTOR</b> structure. The <b>wglDescribeLayerPlane</b> function sets the value of the structure's data members. The function stores the number of bytes of data copied to the structure in the <b>nSize</b> member.

## -returns

If the function succeeds, the return value is <b>TRUE</b>. In addition, the <b>wglDescribeLayerPlane</b> function sets the members of the <b>LAYERPLANEDESCRIPTOR</b> structure pointed to by <i>plpd</i> according to the specified layer plane (<i>iLayerPlane</i> ) of the specified pixel format (<i>iPixelFormat</i> ).

If the function fails, the return value is <b>FALSE</b>.

## -remarks

The numbering of planes (<i>iLayerPlane</i> ) determines their order. Higher-numbered planes overlay lower-numbered planes.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-describepixelformat">DescribePixelFormat</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-layerplanedescriptor">LAYERPLANEDESCRIPTOR</a>



<a href="/windows/desktop/OpenGL/opengl-on-windows-nt--windows-2000--and-windows-95-98">OpenGL on Windows</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-pixelformatdescriptor">PIXELFORMATDESCRIPTOR</a>



<a href="/windows/desktop/OpenGL/wgl-functions">WGL Functions</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-wglcreatelayercontext">wglCreateLayerContext</a>