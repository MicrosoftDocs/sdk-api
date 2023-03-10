---
UID: NF:dxgi.IDXGIOutput.GetDisplayModeList
title: IDXGIOutput::GetDisplayModeList (dxgi.h)
description: Gets the display modes that match the requested format and other input options. (IDXGIOutput.GetDisplayModeList)
helpviewer_keywords: ["3a76a6e4-1ab8-3f7a-7a2b-1bd9540d34fa","GetDisplayModeList","GetDisplayModeList method [DXGI]","GetDisplayModeList method [DXGI]","IDXGIOutput interface","IDXGIOutput interface [DXGI]","GetDisplayModeList method","IDXGIOutput.GetDisplayModeList","IDXGIOutput::GetDisplayModeList","direct3ddxgi.idxgioutput_getdisplaymodelist","dxgi/IDXGIOutput::GetDisplayModeList"]
old-location: direct3ddxgi\idxgioutput_getdisplaymodelist.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgioutput_getdisplaymodelist.htm
ms.date: 12/05/2018
ms.keywords: 3a76a6e4-1ab8-3f7a-7a2b-1bd9540d34fa, GetDisplayModeList, GetDisplayModeList method [DXGI], GetDisplayModeList method [DXGI],IDXGIOutput interface, IDXGIOutput interface [DXGI],GetDisplayModeList method, IDXGIOutput.GetDisplayModeList, IDXGIOutput::GetDisplayModeList, direct3ddxgi.idxgioutput_getdisplaymodelist, dxgi/IDXGIOutput::GetDisplayModeList
req.header: dxgi.h
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
 - IDXGIOutput::GetDisplayModeList
 - dxgi/IDXGIOutput::GetDisplayModeList
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
 - IDXGIOutput.GetDisplayModeList
---

# IDXGIOutput::GetDisplayModeList


## -description

<p class="CCE_Message">[Starting with Direct3D 11.1, we recommend not to use <b>GetDisplayModeList</b> anymore to retrieve the matching display mode. Instead, use <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutput1-getdisplaymodelist1">IDXGIOutput1::GetDisplayModeList1</a>, which supports stereo display mode.]

Gets the display modes that match the requested format and other input options.

## -parameters

### -param EnumFormat

Type: <b><a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a></b>

The color format (see <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a>).

### -param Flags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Options for modes to include (see <a href="/windows/desktop/direct3ddxgi/dxgi-enum-modes">DXGI_ENUM_MODES</a>).
            DXGI_ENUM_MODES_SCALING needs to be specified to expose the display modes that require scaling.  Centered modes, requiring no 
            scaling and corresponding directly to the display output, are enumerated by default.

### -param pNumModes [in, out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a>*</b>

Set <i>pDesc</i> to <b>NULL</b> so that <i>pNumModes</i> returns the number of display modes that match the format and the options.
        Otherwise, <i>pNumModes</i> returns the number of display modes returned in <i>pDesc</i>.

### -param pDesc [out, optional]

Type: <b><a href="/previous-versions/windows/desktop/legacy/bb173064(v=vs.85)">DXGI_MODE_DESC</a>*</b>

A pointer to a list of display modes (see <a href="/previous-versions/windows/desktop/legacy/bb173064(v=vs.85)">DXGI_MODE_DESC</a>); set to <b>NULL</b> to get the number of display modes.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the following <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a>. It is rare, but possible, that the display modes available can change immediately after calling 
      this method, in which case DXGI_ERROR_MORE_DATA is returned (if there is not enough room for all the display modes).  
      If <b>GetDisplayModeList</b> is called from a Remote Desktop Services session (formerly Terminal Services session), DXGI_ERROR_NOT_CURRENTLY_AVAILABLE is returned.

## -remarks

In general, when switching from windowed to full-screen mode, a swap chain automatically chooses a display mode that meets (or exceeds) the resolution, color 
      depth and refresh rate of the swap chain. To exercise more control over the display mode, use this API to poll the set of display modes that are validated 
      against monitor capabilities, or all modes that match the desktop (if the desktop settings are not validated against the monitor).

As shown, this API is designed to be called twice. First to get the number of modes available, and second to return a description of the modes.


```

UINT num = 0;
DXGI_FORMAT format = DXGI_FORMAT_R32G32B32A32_FLOAT;
UINT flags         = DXGI_ENUM_MODES_INTERLACED;

pOutput->GetDisplayModeList( format, flags, &num, 0);

...

DXGI_MODE_DESC * pDescs = new DXGI_MODE_DESC[num];
pOutput->GetDisplayModeList( format, flags, &num, pDescs);
      
```

## -see-also

<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgioutput">IDXGIOutput</a>
