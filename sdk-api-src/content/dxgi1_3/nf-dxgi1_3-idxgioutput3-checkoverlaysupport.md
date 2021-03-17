---
UID: NF:dxgi1_3.IDXGIOutput3.CheckOverlaySupport
title: IDXGIOutput3::CheckOverlaySupport (dxgi1_3.h)
description: Checks for overlay support.
helpviewer_keywords: ["CheckOverlaySupport","CheckOverlaySupport method [DXGI]","CheckOverlaySupport method [DXGI]","IDXGIOutput3 interface","IDXGIOutput3 interface [DXGI]","CheckOverlaySupport method","IDXGIOutput3.CheckOverlaySupport","IDXGIOutput3::CheckOverlaySupport","direct3ddxgi.idxgioutput3_checkoverlaysupport","dxgi1_3/IDXGIOutput3::CheckOverlaySupport"]
old-location: direct3ddxgi\idxgioutput3_checkoverlaysupport.htm
tech.root: direct3ddxgi
ms.assetid: D7B90FF5-5E8B-4F9E-A442-B44449438388
ms.date: 12/05/2018
ms.keywords: CheckOverlaySupport, CheckOverlaySupport method [DXGI], CheckOverlaySupport method [DXGI],IDXGIOutput3 interface, IDXGIOutput3 interface [DXGI],CheckOverlaySupport method, IDXGIOutput3.CheckOverlaySupport, IDXGIOutput3::CheckOverlaySupport, direct3ddxgi.idxgioutput3_checkoverlaysupport, dxgi1_3/IDXGIOutput3::CheckOverlaySupport
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDXGIOutput3::CheckOverlaySupport
 - dxgi1_3/IDXGIOutput3::CheckOverlaySupport
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
 - IDXGIOutput3.CheckOverlaySupport
---

# IDXGIOutput3::CheckOverlaySupport


## -description

Checks for overlay support.

## -parameters

### -param EnumFormat [in]

Type: <b><a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a></b>

A <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a>-typed value for the color format.

### -param pConcernedDevice [in]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

A pointer to the Direct3D device interface. <b>CheckOverlaySupport</b> returns only support info about this scan-out device.

### -param pFlags [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a>*</b>

A pointer to a variable that receives a combination of <a href="/windows/desktop/api/dxgi1_3/ne-dxgi1_3-dxgi_overlay_support_flag">DXGI_OVERLAY_SUPPORT_FLAG</a>-typed values that are combined by using a bitwise OR operation. The resulting value specifies options for overlay support.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the error codes described in the <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a> topic.

## -see-also

<a href="/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgioutput3">IDXGIOutput3</a>