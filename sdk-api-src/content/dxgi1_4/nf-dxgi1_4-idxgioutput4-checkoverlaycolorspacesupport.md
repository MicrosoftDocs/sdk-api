---
UID: NF:dxgi1_4.IDXGIOutput4.CheckOverlayColorSpaceSupport
title: IDXGIOutput4::CheckOverlayColorSpaceSupport (dxgi1_4.h)
description: Checks for overlay color space support.
helpviewer_keywords: ["CheckOverlayColorSpaceSupport","CheckOverlayColorSpaceSupport method [DXGI]","CheckOverlayColorSpaceSupport method [DXGI]","IDXGIOutput4 interface","IDXGIOutput4 interface [DXGI]","CheckOverlayColorSpaceSupport method","IDXGIOutput4.CheckOverlayColorSpaceSupport","IDXGIOutput4::CheckOverlayColorSpaceSupport","direct3ddxgi.idxgioutput4_checkoverlaycolorspacesupport","dxgi1_4/IDXGIOutput4::CheckOverlayColorSpaceSupport"]
old-location: direct3ddxgi\idxgioutput4_checkoverlaycolorspacesupport.htm
tech.root: direct3ddxgi
ms.assetid: C9F582EA-DB16-4FF3-B7BD-ACEA019FF7D4
ms.date: 12/05/2018
ms.keywords: CheckOverlayColorSpaceSupport, CheckOverlayColorSpaceSupport method [DXGI], CheckOverlayColorSpaceSupport method [DXGI],IDXGIOutput4 interface, IDXGIOutput4 interface [DXGI],CheckOverlayColorSpaceSupport method, IDXGIOutput4.CheckOverlayColorSpaceSupport, IDXGIOutput4::CheckOverlayColorSpaceSupport, direct3ddxgi.idxgioutput4_checkoverlaycolorspacesupport, dxgi1_4/IDXGIOutput4::CheckOverlayColorSpaceSupport
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDXGIOutput4::CheckOverlayColorSpaceSupport
 - dxgi1_4/IDXGIOutput4::CheckOverlayColorSpaceSupport
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
 - IDXGIOutput4.CheckOverlayColorSpaceSupport
---

# IDXGIOutput4::CheckOverlayColorSpaceSupport


## -description

Checks for overlay color space support.

## -parameters

### -param Format [in]

Type: <b><a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a></b>

A <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a>-typed value for the color format.

### -param ColorSpace [in]

Type: <b><a href="/windows/desktop/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type">DXGI_COLOR_SPACE_TYPE</a></b>

A <a href="/windows/desktop/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type">DXGI_COLOR_SPACE_TYPE</a>-typed value that specifies color space type to check overlay support for.

### -param pConcernedDevice [in]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

A pointer to the Direct3D device interface. <b>CheckOverlayColorSpaceSupport</b> returns only support info about this scan-out device.

### -param pFlags [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a>*</b>

A pointer to a variable that receives a combination of <a href="/windows/desktop/api/dxgi1_4/ne-dxgi1_4-dxgi_overlay_color_space_support_flag">DXGI_OVERLAY_COLOR_SPACE_SUPPORT_FLAG</a>-typed values that are combined by using a bitwise OR operation. The resulting value specifies options for overlay color space support.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns <b>S_OK</b> on success, or it returns one of the error codes that are described in the <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a> topic.

## -see-also

<a href="/windows/desktop/api/dxgi1_4/nn-dxgi1_4-idxgioutput4">IDXGIOutput4</a>