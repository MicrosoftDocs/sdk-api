---
UID: NF:dxgi1_5.IDXGISwapChain4.SetHDRMetaData
title: IDXGISwapChain4::SetHDRMetaData (dxgi1_5.h)
description: This method sets High Dynamic Range (HDR) and Wide Color Gamut (WCG) header metadata.
helpviewer_keywords: ["IDXGISwapChain4 interface [DXGI]","SetHDRMetaData method","IDXGISwapChain4.SetHDRMetaData","IDXGISwapChain4::SetHDRMetaData","SetHDRMetaData","SetHDRMetaData method [DXGI]","SetHDRMetaData method [DXGI]","IDXGISwapChain4 interface","direct3ddxgi.idxgiswapchain4_sethdrmetadata","dxgi1_5/IDXGISwapChain4::SetHDRMetaData"]
old-location: direct3ddxgi\idxgiswapchain4_sethdrmetadata.htm
tech.root: direct3ddxgi
ms.assetid: 03EBBB29-EAC3-4FE7-9CA7-D9F62CFDA8FB
ms.date: 12/05/2018
ms.keywords: IDXGISwapChain4 interface [DXGI],SetHDRMetaData method, IDXGISwapChain4.SetHDRMetaData, IDXGISwapChain4::SetHDRMetaData, SetHDRMetaData, SetHDRMetaData method [DXGI], SetHDRMetaData method [DXGI],IDXGISwapChain4 interface, direct3ddxgi.idxgiswapchain4_sethdrmetadata, dxgi1_5/IDXGISwapChain4::SetHDRMetaData
req.header: dxgi1_5.h
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
req.lib: Dxgi1_5.lib
req.dll: Dxgi1_5.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDXGISwapChain4::SetHDRMetaData
 - dxgi1_5/IDXGISwapChain4::SetHDRMetaData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dxgi1_5.dll
api_name:
 - IDXGISwapChain4.SetHDRMetaData
---

# IDXGISwapChain4::SetHDRMetaData


## -description

> [!WARNING]
> It is no longer recommended for apps to explicitly set HDR metadata on their swap chain using **SetHDRMetaData**. Windows does not guarantee that swap chain metadata is sent to the monitor, and monitors do not handle HDR metadata consistently. Therefore it's recommended that apps always tone-map content into the range reported by the monitor. For more details on how to write apps that react dynamically to monitor capabilities, see [Using DirectX with high dynamic range displays and Advanced Color](/windows/win32/direct3darticles/high-dynamic-range).
>
> See Remarks for more details.

This method sets High Dynamic Range (HDR) and Wide Color Gamut (WCG)  header metadata.

## -parameters

### -param Type [in]

Type: <b><a href="/windows/desktop/api/dxgi1_5/ne-dxgi1_5-dxgi_hdr_metadata_type">DXGI_HDR_METADATA_TYPE</a></b>

Specifies one member of the  <a href="/windows/desktop/api/dxgi1_5/ne-dxgi1_5-dxgi_hdr_metadata_type">DXGI_HDR_METADATA_TYPE</a> enum.

### -param Size [in]

Type: <b>UINT</b>

Specifies the size of <i>pMetaData</i>, in bytes.

### -param pMetaData [in, optional]

Type: <b>void*</b>

Specifies a void pointer that references the metadata, if it exists. Refer to the <a href="/windows/desktop/api/dxgi1_5/ns-dxgi1_5-dxgi_hdr_metadata_hdr10">DXGI_HDR_METADATA_HDR10</a> structure.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns an HRESULT success or error code.

## -remarks

This method sets metadata to enable a monitor's output to be adjusted depending on its capabilities. However it does not change how pixel values are interpreted by Windows or monitors. To adjust the color space of the swap chain, use [**SetColorSpace1**](..\dxgi1_4\nf-dxgi1_4-idxgiswapchain3-setcolorspace1.md) instead.

Applications should not rely on the metadata being sent to the monitor as the metadata may be ignored. Monitors do not consistently process HDR metadata, resulting in varied appearance of your content across different monitors. In order to ensure more consistent output across a range of monitors, devices, and use cases, it is recommended to not use **SetHDRMetaData** and to instead tone-map content into the gamut and luminance range supported by the monitor. See [IDXGIOutput6::GetDesc1](../dxgi1_6/nf-dxgi1_6-idxgioutput6-getdesc1.md) to retrieve the monitor's supported gamut and luminance range. Monitors adhering to the VESA DisplayHDR standard will automatically perform a form of clipping for content outside of the monitor's supported gamut and luminance range.

For more details on how to write apps that react dynamically to monitor capabilities, see [Using DirectX with high dynamic range displays and Advanced Color](/windows/win32/direct3darticles/high-dynamic-range).

## -see-also

<a href="/windows/desktop/direct3ddxgi/dxgi-1-5-improvements">DXGI 1.5 Improvements</a>



<a href="/windows/desktop/api/dxgi1_5/nn-dxgi1_5-idxgiswapchain4">IDXGISwapChain4</a>