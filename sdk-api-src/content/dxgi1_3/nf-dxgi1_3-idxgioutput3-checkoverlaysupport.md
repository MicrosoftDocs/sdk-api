---
UID: NF:dxgi1_3.IDXGIOutput3.CheckOverlaySupport
title: IDXGIOutput3::CheckOverlaySupport
author: windows-sdk-content
description: Checks for overlay support.
old-location: direct3ddxgi\idxgioutput3_checkoverlaysupport.htm
tech.root: direct3ddxgi
ms.assetid: D7B90FF5-5E8B-4F9E-A442-B44449438388
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: CheckOverlaySupport, CheckOverlaySupport method [DXGI], CheckOverlaySupport method [DXGI],IDXGIOutput3 interface, IDXGIOutput3 interface [DXGI],CheckOverlaySupport method, IDXGIOutput3.CheckOverlaySupport, IDXGIOutput3::CheckOverlaySupport, direct3ddxgi.idxgioutput3_checkoverlaysupport, dxgi1_3/IDXGIOutput3::CheckOverlaySupport
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dxgi1_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dxgi.lib
 - Dxgi.dll
api_name:
 - IDXGIOutput3.CheckOverlaySupport
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- dxgi1_3.h
: 
- IDXGIOutput3.CheckOverlaySupport
: 
---

# IDXGIOutput3::CheckOverlaySupport


## -description


Checks for overlay support.


## -parameters




### -param EnumFormat [in]

Type: <b><a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a></b>

A <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a>-typed value for the color format.


### -param pConcernedDevice [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

A pointer to the Direct3D device interface. <b>CheckOverlaySupport</b> returns only support info about this scan-out device. 


### -param pFlags [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a>*</b>

A pointer to a variable that receives a combination of <a href="https://msdn.microsoft.com/D2657A18-1F95-485A-A76E-381413CEB7B8">DXGI_OVERLAY_SUPPORT_FLAG</a>-typed values that are combined by using a bitwise OR operation. The resulting value specifies options for overlay support. 


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns one of the error codes described in the <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a> topic.




## -see-also




<a href="https://msdn.microsoft.com/A116286A-F948-49AA-9D3B-F104E3312920">IDXGIOutput3</a>
 

 

