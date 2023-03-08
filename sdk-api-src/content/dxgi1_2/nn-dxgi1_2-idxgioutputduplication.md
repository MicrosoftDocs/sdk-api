---
UID: NN:dxgi1_2.IDXGIOutputDuplication
title: IDXGIOutputDuplication (dxgi1_2.h)
description: The IDXGIOutputDuplication interface accesses and manipulates the duplicated desktop image.
helpviewer_keywords: ["IDXGIOutputDuplication","IDXGIOutputDuplication interface [DXGI]","IDXGIOutputDuplication interface [DXGI]","described","direct3ddxgi.idxgioutputduplication","dxgi1_2/IDXGIOutputDuplication"]
old-location: direct3ddxgi\idxgioutputduplication.htm
tech.root: direct3ddxgi
ms.assetid: 02C4EC3D-D97F-4CFC-ABF5-03B44CE6A658
ms.date: 12/05/2018
ms.keywords: IDXGIOutputDuplication, IDXGIOutputDuplication interface [DXGI], IDXGIOutputDuplication interface [DXGI],described, direct3ddxgi.idxgioutputduplication, dxgi1_2/IDXGIOutputDuplication
req.header: dxgi1_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dxgi.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDXGIOutputDuplication
 - dxgi1_2/IDXGIOutputDuplication
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dxgi.lib
 - Dxgi.dll
api_name:
 - IDXGIOutputDuplication
---

# IDXGIOutputDuplication interface


## -description

The <b>IDXGIOutputDuplication</b> interface accesses and manipulates the duplicated desktop image.

## -inheritance

The <b>IDXGIOutputDuplication</b> interface inherits from <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiobject">IDXGIObject</a>. <b>IDXGIOutputDuplication</b> also has these types of members:

## -remarks

A collaboration application can use <b>IDXGIOutputDuplication</b> to access the desktop image. <b>IDXGIOutputDuplication</b> is supported in Desktop Window Manager (DWM) on non-8bpp DirectX full-screen modes and non-8bpp OpenGL full-screen modes. 16-bit or 32-bit GDI non-DWM desktop modes are not supported.
        

An application can use <b>IDXGIOutputDuplication</b> on a separate thread to receive the desktop images and to feed them into their specific image-processing pipeline.  The application uses <b>IDXGIOutputDuplication</b> to perform the following operations:
          

<ol>
<li>Acquire the next desktop image.</li>
<li>Retrieve the information that describes the image.</li>
<li>Perform an operation on the image. This operation can be as simple as copying the image to a staging buffer so that the application can read the pixel data on the image. The application reads the pixel data  after the application calls <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgisurface-map">IDXGISurface::Map</a>. Alternatively, this operation can be more complex. For example, the application can run some pixel shaders on the updated regions of the image to encode those regions for transmission to a client.
          </li>
<li>After the application finishes  processing each desktop image, it releases the image, loops to step 1, and repeats the steps. The application repeats these steps until it is finished processing desktop images.</li>
</ol>
The following components of the operating system can generate the desktop image:

<ul>
<li>The DWM by composing the desktop image
          </li>
<li>A full-screen DirectX or OpenGL application</li>
<li>An application by switching to a separate desktop, for example, the secure desktop that is used to display the login screen</li>
</ul>
All current <b>IDXGIOutputDuplication</b> interfaces become invalid when the operating system switches to a different component that produces the desktop image or when a mode change occurs.  In these situations, the application must destroy its current <b>IDXGIOutputDuplication</b> interface and create a new <b>IDXGIOutputDuplication</b> interface.
        

Examples of situations in which <b>IDXGIOutputDuplication</b> becomes invalid are:
          

<ul>
<li>Desktop switch</li>
<li>Mode change</li>
<li>Switch from DWM on, DWM off, or other full-screen application
          </li>
</ul>
In these situations, the application must release the <b>IDXGIOutputDuplication</b> interface and must create a new <b>IDXGIOutputDuplication</b> interface for the new content.  If the application does not have the appropriate privilege to the new desktop image, its call to the <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutput1-duplicateoutput">IDXGIOutput1::DuplicateOutput</a> method fails.
        

While the application processes each desktop image, the operating system accumulates all the desktop image updates into a single update. For more information about desktop updates, see <a href="/windows/desktop/direct3ddxgi/desktop-dup-api">Updating the desktop image data</a>.
        

The desktop image is always in the <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT_B8G8R8A8_UNORM</a> format.
        

The <b>IDXGIOutputDuplication</b> interface does not exist for Windows Store apps.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiobject">IDXGIObject</a>
