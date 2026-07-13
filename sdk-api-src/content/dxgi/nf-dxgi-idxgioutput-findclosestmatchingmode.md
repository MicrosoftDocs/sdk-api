---
UID: NF:dxgi.IDXGIOutput.FindClosestMatchingMode
title: IDXGIOutput::FindClosestMatchingMode (dxgi.h)
description: Finds the display mode that most closely matches the requested display mode. (IDXGIOutput.FindClosestMatchingMode)
helpviewer_keywords: ["FindClosestMatchingMode","FindClosestMatchingMode method [DXGI]","FindClosestMatchingMode method [DXGI]","IDXGIOutput interface","IDXGIOutput interface [DXGI]","FindClosestMatchingMode method","IDXGIOutput.FindClosestMatchingMode","IDXGIOutput::FindClosestMatchingMode","c140400c-32d4-ec57-8da0-a37a23cfd5e4","direct3ddxgi.idxgioutput_findclosestmatchingmode","dxgi/IDXGIOutput::FindClosestMatchingMode"]
old-location: direct3ddxgi\idxgioutput_findclosestmatchingmode.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgioutput_findclosestmatchingmode.htm
ms.date: 12/05/2018
ms.keywords: FindClosestMatchingMode, FindClosestMatchingMode method [DXGI], FindClosestMatchingMode method [DXGI],IDXGIOutput interface, IDXGIOutput interface [DXGI],FindClosestMatchingMode method, IDXGIOutput.FindClosestMatchingMode, IDXGIOutput::FindClosestMatchingMode, c140400c-32d4-ec57-8da0-a37a23cfd5e4, direct3ddxgi.idxgioutput_findclosestmatchingmode, dxgi/IDXGIOutput::FindClosestMatchingMode
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
 - IDXGIOutput::FindClosestMatchingMode
 - dxgi/IDXGIOutput::FindClosestMatchingMode
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
 - IDXGIOutput.FindClosestMatchingMode
---

# IDXGIOutput::FindClosestMatchingMode


## -description

<p class="CCE_Message">[Starting with Direct3D 11.1, we recommend not to use <b>FindClosestMatchingMode</b> anymore to find the display mode that most closely matches the requested display mode. Instead, use <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutput1-findclosestmatchingmode1">IDXGIOutput1::FindClosestMatchingMode1</a>, which supports stereo display mode.]

Finds the display mode that most closely matches the requested display mode.

## -parameters

### -param pModeToMatch [in]

Type: <b>const <a href="/previous-versions/windows/desktop/legacy/bb173064(v=vs.85)">DXGI_MODE_DESC</a>*</b>

The desired display mode (see <a href="/previous-versions/windows/desktop/legacy/bb173064(v=vs.85)">DXGI_MODE_DESC</a>). Members of <b>DXGI_MODE_DESC</b> can be unspecified indicating no preference for 
        that member.  A value of 0 for <b>Width</b> or <b>Height</b> indicates the value is unspecified.  If either <b>Width</b> or 
        <b>Height</b> are 0, both must be 0.  A numerator and denominator of 0 in <b>RefreshRate</b> indicate it is unspecified. Other members 
        of <b>DXGI_MODE_DESC</b> have enumeration values indicating the member is unspecified.  If <i>pConcernedDevice</i> is <b>NULL</b>, <b>Format</b> cannot be DXGI_FORMAT_UNKNOWN.

### -param pClosestMatch [out]

Type: <b><a href="/previous-versions/windows/desktop/legacy/bb173064(v=vs.85)">DXGI_MODE_DESC</a>*</b>

The mode that most closely matches <i>pModeToMatch</i>.

### -param pConcernedDevice [in, optional]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

A pointer to the Direct3D device interface. If this parameter is <b>NULL</b>, only modes whose format matches that of <i>pModeToMatch</i> will 
        be returned; otherwise, only those formats that are supported for scan-out by the device are returned. For info about the formats that are supported for scan-out by the device at each feature level:

<ul>
<li>
<a href="/windows/desktop/direct3ddxgi/hardware-support-for-direct3d-12-1-formats">DXGI Format  Support for Direct3D Feature Level 12.1 Hardware</a>
</li>
<li>
<a href="/windows/desktop/direct3ddxgi/hardware-support-for-direct3d-12-0-formats">DXGI Format  Support for Direct3D Feature Level 12.0 Hardware</a>
</li>
<li>
<a href="/windows/desktop/direct3ddxgi/format-support-for-direct3d-11-1-feature-level-hardware">DXGI Format  Support for Direct3D Feature Level 11.1 Hardware</a>
</li>
<li>
<a href="/windows/desktop/direct3ddxgi/format-support-for-direct3d-11-0-feature-level-hardware">DXGI Format  Support for Direct3D Feature Level 11.0 Hardware</a>
</li>
<li>
<a href="/previous-versions/ff471324(v=vs.85)">Hardware Support for Direct3D 10Level9 Formats</a>
</li>
<li>
<a href="/windows/desktop/direct3ddxgi/format-support-for-direct3d-feature-level-10-1-hardware">Hardware Support for Direct3D 10.1 Formats</a>
</li>
<li>
<a href="/windows/desktop/direct3ddxgi/format-support-for-direct3d-feature-level-10-0-hardware">Hardware Support for Direct3D 10 Formats</a>
</li>
</ul>

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the following <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a>.

## -remarks

<b>FindClosestMatchingMode</b> behaves similarly to the <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutput1-findclosestmatchingmode1">IDXGIOutput1::FindClosestMatchingMode1</a> except <b>FindClosestMatchingMode</b> considers only the mono display modes. <b>IDXGIOutput1::FindClosestMatchingMode1</b> considers only stereo modes if you set the <b>Stereo</b> member in the <a href="/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_mode_desc1">DXGI_MODE_DESC1</a> structure that <i>pModeToMatch</i> points to, and considers only mono modes if <b>Stereo</b> is not set.


<a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutput1-findclosestmatchingmode1">IDXGIOutput1::FindClosestMatchingMode1</a> returns a matched display-mode set with only stereo modes or only mono modes.
<b>FindClosestMatchingMode</b> behaves as though you specified the input mode as mono.

## -see-also

<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgioutput">IDXGIOutput</a>
