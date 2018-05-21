---
UID: NF:dxgi1_2.IDXGIOutput1.GetDisplaySurfaceData1
title: IDXGIOutput1::GetDisplaySurfaceData1
author: windows-driver-content
description: Copies the display surface (front buffer) to a user-provided resource.
old-location: direct3ddxgi\idxgioutput1_getdisplaysurfacedata1.htm
old-project: direct3ddxgi
ms.assetid: 120BC7CD-A4B2-4688-9A11-0BD59761B5F1
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: GetDisplaySurfaceData1, GetDisplaySurfaceData1 method [DXGI], GetDisplaySurfaceData1 method [DXGI],IDXGIOutput1 interface, IDXGIOutput1 interface [DXGI],GetDisplaySurfaceData1 method, IDXGIOutput1.GetDisplaySurfaceData1, IDXGIOutput1::GetDisplaySurfaceData1, direct3ddxgi.idxgioutput1_getdisplaysurfacedata1, dxgi1_2/IDXGIOutput1::GetDisplaySurfaceData1
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dxgi1_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DXGI_OFFER_RESOURCE_PRIORITY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	DXGI.lib
-	DXGI.dll
api_name:
-	IDXGIOutput1.GetDisplaySurfaceData1
product: Windows
targetos: Windows
req.lib: DXGI.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIOutput1::GetDisplaySurfaceData1


## -description


Copies the display surface (front buffer) to a user-provided resource.


## -parameters




### -param pDestination [in]

A pointer to a resource interface that represents the resource to which <b>GetDisplaySurfaceData1</b> copies the display surface.


## -returns



Returns one of the error codes described in the <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a> topic.




## -remarks



<b>GetDisplaySurfaceData1</b> is similar to <a href="https://msdn.microsoft.com/c068853b-12dd-4175-b11a-06bef3b987b5">IDXGIOutput::GetDisplaySurfaceData</a> except <b>GetDisplaySurfaceData1</b> takes an <a href="https://msdn.microsoft.com/de1f11a5-194b-438e-975b-3945179d0ed7">IDXGIResource</a> and <b>IDXGIOutput::GetDisplaySurfaceData</b> takes an <a href="https://msdn.microsoft.com/9210b966-9e9a-4cd1-ba70-6f1a9fda9d80">IDXGISurface</a>.

<b>GetDisplaySurfaceData1</b> returns an error if the input resource is not a 2D texture (represented by the <a href="https://msdn.microsoft.com/49cd6e21-6cb1-45ea-b83a-3c93f0560915">ID3D11Texture2D</a> interface) with an array size (<b>ArraySize</b> member of the <a href="https://msdn.microsoft.com/90c0f877-daf5-4b3d-9846-5bb414c55461">D3D11_TEXTURE2D_DESC</a> structure) that is equal to the swap chain buffers.

The original <a href="https://msdn.microsoft.com/c068853b-12dd-4175-b11a-06bef3b987b5">IDXGIOutput::GetDisplaySurfaceData</a> and the updated <b>GetDisplaySurfaceData1</b> behave exactly the same. <b>GetDisplaySurfaceData1</b> was required because textures with an array size equal to 2 (<b>ArraySize</b> = 2) do not implement <a href="https://msdn.microsoft.com/9210b966-9e9a-4cd1-ba70-6f1a9fda9d80">IDXGISurface</a>.


          You can call <b>GetDisplaySurfaceData1</b> only when an output is in full-screen mode. If <b>GetDisplaySurfaceData1</b> succeeds, it fills the destination resource.

Use <a href="https://msdn.microsoft.com/2ed41c7b-7b9b-49a1-a11d-9a94adee7824">IDXGIOutput::GetDesc</a> to determine the size (width and height) of the output when you want to allocate space for the destination resource. This is true regardless of target monitor rotation. A destination resource created by a graphics component (such as Direct3D 11) must be created with CPU write permission (see <a href="https://msdn.microsoft.com/0a19c2a7-2570-40e2-8328-cbf5d7263605">D3D11_CPU_ACCESS_WRITE</a>). Other surfaces can be created with CPU read-write permission (<b>D3D11_CPU_ACCESS_READ</b> | <b>D3D11_CPU_ACCESS_WRITE</b>). <b>GetDisplaySurfaceData1</b> modifies the surface data to fit the destination resource (stretch, shrink, convert format, rotate). <b>GetDisplaySurfaceData1</b> performs the stretch and shrink with point sampling. 




## -see-also




<a href="https://msdn.microsoft.com/27C7BD34-0746-4D5F-A746-45FFEE5BCD31">IDXGIOutput1</a>
 

 

