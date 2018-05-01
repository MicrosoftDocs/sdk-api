---
UID: NF:mfapi.MFCreateDXGISurfaceBuffer
title: MFCreateDXGISurfaceBuffer function
author: windows-driver-content
description: Creates a media buffer to manage a Microsoft DirectX Graphics Infrastructure (DXGI) surface.
old-location: mf\mfcreatedxgisurfacebuffer.htm
old-project: medfound
ms.assetid: 5D859F36-A82B-488B-A2F6-C697A1AA86BC
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: MFCreateDXGISurfaceBuffer, MFCreateDXGISurfaceBuffer function [Media Foundation], mf.mfcreatedxgisurfacebuffer, mfapi/MFCreateDXGISurfaceBuffer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_CUSTOM_DECODE_UNIT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	mfplat.dll
api_name:
-	MFCreateDXGISurfaceBuffer
product: Windows
targetos: Windows
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
req.product: GDI+ 1.1
---

# MFCreateDXGISurfaceBuffer function


## -description


Creates a media buffer to manage a Microsoft DirectX Graphics Infrastructure (DXGI) surface.


## -parameters




### -param riid [in]


            Identifies the type of DXGI surface. This value must be <b>IID_ID3D11Texture2D</b>.
          


### -param punkSurface [in]


            A pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface of the DXGI surface.
          


### -param uSubresourceIndex [in]

The zero-based index of a subresource of the surface. The media buffer object is associated with this subresource.


### -param fBottomUpWhenLinear [in]


            If <b>TRUE</b>, the buffer's <a href="https://msdn.microsoft.com/32601f2e-ab91-4a65-bcf4-8e063e90fbb0">IMF2DBuffer::ContiguousCopyTo</a> method copies the buffer into a bottom-up format. The bottom-up format is compatible with GDI for uncompressed RGB images. If this parameter is <b>FALSE</b>, the <b>ContiguousCopyTo</b> method copies the buffer into a top-down format, which is compatible with Direct3D.
          

For more information about top-down versus bottom-up images, see <a href="https://msdn.microsoft.com/13cd1106-48b3-4522-ac09-8efbaab5c31d">Image Stride</a>.


### -param ppBuffer [out]


            Receives a pointer to the <a href="https://msdn.microsoft.com/3ccc7089-d0d0-4eb1-b763-0d4e348af685">IMFMediaBuffer</a> interface. The caller must release the buffer.
          


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The returned buffer object supports the following interfaces:

<ul>
<li>
<a href="https://msdn.microsoft.com/80eb23db-a7c0-4dbe-97d8-0dc07a34d8f7">IMF2DBuffer</a>
</li>
<li>
<a href="https://msdn.microsoft.com/BFA73B1A-F8A7-4100-9DBD-234CCA06F9F5">IMF2DBuffer2</a>
</li>
<li>
<a href="https://msdn.microsoft.com/796D7755-275D-4A0B-A34F-5D34DCEC8AC7">IMFDXGIBuffer</a>
</li>
<li>
<a href="https://msdn.microsoft.com/3ccc7089-d0d0-4eb1-b763-0d4e348af685">IMFMediaBuffer</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

