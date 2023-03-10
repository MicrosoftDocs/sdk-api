---
UID: NF:wingdi.SetWorldTransform
title: SetWorldTransform function (wingdi.h)
description: The SetWorldTransform function sets a two-dimensional linear transformation between world space and page space for the specified device context. This transformation can be used to scale, rotate, shear, or translate graphics output.
helpviewer_keywords: ["SetWorldTransform","SetWorldTransform function [Windows GDI]","_win32_SetWorldTransform","gdi.setworldtransform","wingdi/SetWorldTransform"]
old-location: gdi\setworldtransform.htm
tech.root: gdi
ms.assetid: d103a4dd-949e-4f18-ac90-bb0e51011233
ms.date: 12/05/2018
ms.keywords: SetWorldTransform, SetWorldTransform function [Windows GDI], _win32_SetWorldTransform, gdi.setworldtransform, wingdi/SetWorldTransform
req.header: wingdi.h
req.include-header: Windows.h
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
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetWorldTransform
 - wingdi/SetWorldTransform
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Draw-l1-1-0.dll
 - Ext-MS-Win-GDI-Draw-l1-1-1.dll
 - ext-ms-win-gdi-draw-l1-1-2.dll
 - Ext-MS-Win-GDI-Draw-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - SetWorldTransform
---

## -description

The <b>SetWorldTransform</b> function sets a two-dimensional linear transformation between world space and page space for the specified device context. This transformation can be used to scale, rotate, shear, or translate graphics output.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param lpxf [in]

A pointer to an <a href="/windows/desktop/api/wingdi/ns-wingdi-xform">XFORM</a> structure that contains the transformation data.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

Below is the transformation matrix (note that the digits in the element notation are 1-based column number followed by 1-based row number, rather than the reverse).


``` syntax
| eM11 eM21 eDx |
| eM12 eM22 eDy |
| 0    0    1   |

```


So for any coordinates (x, y) in world space, the transformed coordinates in page space (x', y') can be determined in the way shown below.


``` syntax
| x' |   | eM11 eM21 eDx |   | x |   
| y' | = | eM12 eM22 eDy | . | y |
| 1  |   | 0    0    1   |   | 1 |

x' = x * eM11 + y * eM21 + eDx
y' = x * eM12 + y * eM22 + eDy

```


This function uses logical units.

The world transformation is usually used to scale or rotate logical images in a device-independent way.

The default world transformation is the identity matrix with zero offset.

The <b>SetWorldTransform</b> function will fail unless the graphics mode for the given device context has been set to GM_ADVANCED by previously calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-setgraphicsmode">SetGraphicsMode</a> function. Likewise, it will not be possible to reset the graphics mode for the device context to the default GM_COMPATIBLE mode, unless the world transformation has first been reset to the default identity transformation by calling <b>SetWorldTransform</b> or <a href="/windows/desktop/api/wingdi/nf-wingdi-modifyworldtransform">ModifyWorldTransform</a>.

#### Examples

For an example, see <a href="/windows/desktop/gdi/using-coordinate-spaces-and-transformations">Using Coordinate Spaces and Transformations</a>.

## -see-also

<a href="/windows/desktop/gdi/coordinate-space-and-transformation-functions">Coordinate Space and Transformation Functions</a>

<a href="/windows/desktop/gdi/coordinate-spaces-and-transformations">Coordinate Spaces and Transformations Overview</a>

<a href="/windows/desktop/api/wingdi/nf-wingdi-getworldtransform">GetWorldTransform</a>

<a href="/windows/desktop/api/wingdi/nf-wingdi-modifyworldtransform">ModifyWorldTransform</a>

<a href="/windows/desktop/api/wingdi/nf-wingdi-setgraphicsmode">SetGraphicsMode</a>

<a href="/windows/desktop/api/wingdi/nf-wingdi-setmapmode">SetMapMode</a>

<a href="/windows/desktop/api/wingdi/nf-wingdi-setviewportextex">SetViewportExtEx</a>

<a href="/windows/desktop/api/wingdi/nf-wingdi-setviewportorgex">SetViewportOrgEx</a>

<a href="/windows/desktop/api/wingdi/nf-wingdi-setwindowextex">SetWindowExtEx</a>

<a href="/windows/desktop/api/wingdi/nf-wingdi-setwindoworgex">SetWindowOrgEx</a>

<a href="/windows/desktop/api/wingdi/ns-wingdi-xform">XFORM</a>
