---
UID: NF:d2d1.ID2D1RenderTarget.SetDpi
title: ID2D1RenderTarget::SetDpi (d2d1.h)
description: Sets the dots per inch (DPI) of the render target.
helpviewer_keywords: ["ID2D1RenderTarget interface [Direct2D]","SetDpi method","ID2D1RenderTarget.SetDpi","ID2D1RenderTarget::SetDpi","SetDpi","SetDpi method [Direct2D]","SetDpi method [Direct2D]","ID2D1RenderTarget interface","d2d1/ID2D1RenderTarget::SetDpi","direct2d.ID2D1RenderTarget_SetDpi"]
old-location: direct2d\ID2D1RenderTarget_SetDpi.htm
tech.root: Direct2D
ms.assetid: 603a838b-4abc-4adf-93a9-ec8535d42ed6
ms.date: 12/05/2018
ms.keywords: ID2D1RenderTarget interface [Direct2D],SetDpi method, ID2D1RenderTarget.SetDpi, ID2D1RenderTarget::SetDpi, SetDpi, SetDpi method [Direct2D], SetDpi method [Direct2D],ID2D1RenderTarget interface, d2d1/ID2D1RenderTarget::SetDpi, direct2d.ID2D1RenderTarget_SetDpi
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1RenderTarget::SetDpi
 - d2d1/ID2D1RenderTarget::SetDpi
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1RenderTarget.SetDpi
---

# ID2D1RenderTarget::SetDpi


## -description

Sets the dots per inch (DPI) of the render target.

## -parameters

### -param dpiX

Type: <b>FLOAT</b>

A value greater than or equal to zero that specifies the horizontal DPI of the render target.

### -param dpiY

Type: <b>FLOAT</b>

A value greater than or equal to zero that specifies the vertical DPI of the render target.

## -remarks

This method specifies the mapping from pixel space to device-independent space  for the render target.  If both <i>dpiX</i> and <i>dpiY</i> are 0, the factory-read system DPI is chosen. If one parameter is zero and the other unspecified, the DPI is not changed.

For <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget">ID2D1HwndRenderTarget</a>, the DPI defaults to the most recently factory-read system DPI. The default value for all other render targets is 96 DPI.

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>

