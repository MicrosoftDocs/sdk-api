---
UID: NF:dxgi1_6.IDXGIOutput6.GetDesc1
title: IDXGIOutput6::GetDesc1 (dxgi1_6.h)
description: Get an extended description of the output that includes color characteristics and connection type.
helpviewer_keywords: ["GetDesc1","GetDesc1 method [DXGI]","GetDesc1 method [DXGI]","IDXGIOutput6 interface","IDXGIOutput6 interface [DXGI]","GetDesc1 method","IDXGIOutput6.GetDesc1","IDXGIOutput6::GetDesc1","direct3ddxgi.idxgioutput6_getdesc1","dxgi1_6/IDXGIOutput6::GetDesc1"]
old-location: direct3ddxgi\idxgioutput6_getdesc1.htm
tech.root: direct3ddxgi
ms.assetid: DE251D64-BB41-49D7-AC46-791089502286
ms.date: 12/05/2018
ms.keywords: GetDesc1, GetDesc1 method [DXGI], GetDesc1 method [DXGI],IDXGIOutput6 interface, IDXGIOutput6 interface [DXGI],GetDesc1 method, IDXGIOutput6.GetDesc1, IDXGIOutput6::GetDesc1, direct3ddxgi.idxgioutput6_getdesc1, dxgi1_6/IDXGIOutput6::GetDesc1
req.header: dxgi1_6.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: DXGI.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDXGIOutput6::GetDesc1
 - dxgi1_6/IDXGIOutput6::GetDesc1
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DXGI.lib
 - DXGI.dll
api_name:
 - IDXGIOutput6.GetDesc1
---

# IDXGIOutput6::GetDesc1


## -description

Get an extended description of the output that includes color characteristics and connection type.

## -parameters

### -param pDesc [out]

Type: <b><a href="/windows/desktop/api/dxgi1_6/ns-dxgi1_6-dxgi_output_desc1">DXGI_OUTPUT_DESC1</a>*</b>

A pointer to the output description (see <a href="/windows/win32/api/dxgi1_6/ns-dxgi1_6-dxgi_output_desc1">DXGI_OUTPUT_DESC1</a>).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns a code that indicates success or failure. S_OK if successful, <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR_INVALID_CALL</a> if <i>pDesc</i> is passed in as <b>NULL</b>.

## -remarks

Some scenarios do not have well-defined values for all fields in this struct. For example, if this IDXGIOutput represents a clone/duplicate set, or if the EDID has missing or invalid data. In these cases, the OS will provide some default values that correspond to a standard SDR display.

An output's reported color and luminance characteristics can adjust dynamically while the system is running due to user action or changing ambient conditions. Therefore, apps should periodically query **IDXGIFactory::IsCurrent** and re-create their **IDXGIFactory** if it returns **FALSE**. Then re-query **GetDesc1** from the new factory's equivalent output to retrieve the newest color information.

For more details on how to write apps that react dynamically to monitor capabilities, see [Using DirectX with high dynamic range displays and Advanced Color](/windows/win32/direct3darticles/high-dynamic-range). 

On a high DPI desktop, <b>GetDesc1</b> returns the visualized screen size unless the app is marked high DPI aware. For info about writing DPI-aware Win32 apps, see <a href="/windows/desktop/hidpi/high-dpi-desktop-application-development-on-windows">High DPI</a>.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="/windows/desktop/api/dxgi1_6/nn-dxgi1_6-idxgioutput6">IDXGIOutput6</a>