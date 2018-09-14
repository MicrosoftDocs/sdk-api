---
UID: NF:dxgi1_4.IDXGIOutput4.CheckOverlayColorSpaceSupport
title: IDXGIOutput4::CheckOverlayColorSpaceSupport
author: windows-sdk-content
description: Checks for overlay color space support.
old-location: direct3ddxgi\idxgioutput4_checkoverlaycolorspacesupport.htm
tech.root: direct3ddxgi
ms.assetid: C9F582EA-DB16-4FF3-B7BD-ACEA019FF7D4
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CheckOverlayColorSpaceSupport, CheckOverlayColorSpaceSupport method [DXGI], CheckOverlayColorSpaceSupport method [DXGI],IDXGIOutput4 interface, IDXGIOutput4 interface [DXGI],CheckOverlayColorSpaceSupport method, IDXGIOutput4.CheckOverlayColorSpaceSupport, IDXGIOutput4::CheckOverlayColorSpaceSupport, direct3ddxgi.idxgioutput4_checkoverlaycolorspacesupport, dxgi1_4/IDXGIOutput4::CheckOverlayColorSpaceSupport
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dxgi1_4.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - IDXGIOutput4.CheckOverlayColorSpaceSupport
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDXGIOutput4::CheckOverlayColorSpaceSupport


## -description


Checks for overlay color space support.


## -parameters




### -param Format [in]

Type: <b><a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a></b>

A <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a>-typed value for the color format.


### -param ColorSpace [in]

Type: <b><a href="https://msdn.microsoft.com/E25C933F-0DB3-4BC4-9755-9361B2B9B9CB">DXGI_COLOR_SPACE_TYPE</a></b>

A <a href="https://msdn.microsoft.com/E25C933F-0DB3-4BC4-9755-9361B2B9B9CB">DXGI_COLOR_SPACE_TYPE</a>-typed value that specifies color space type to check overlay support for.


### -param pConcernedDevice [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

A pointer to the Direct3D device interface. <b>CheckOverlayColorSpaceSupport</b> returns only support info about this scan-out device. 


### -param pFlags [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a>*</b>

A pointer to a variable that receives a combination of <a href="https://msdn.microsoft.com/3664CEBA-42A2-45FF-AA6F-286C1AECF535">DXGI_OVERLAY_COLOR_SPACE_SUPPORT_FLAG</a>-typed values that are combined by using a bitwise OR operation. The resulting value specifies options for overlay color space support. 


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns <b>S_OK</b> on success, or it returns one of the error codes that are described in the <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a> topic.




## -see-also




<a href="https://msdn.microsoft.com/6B9B4242-7B10-4022-9105-6903FEAE1161">IDXGIOutput4</a>
 

 

