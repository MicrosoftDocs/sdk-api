---
UID: NF:dxgi.IDXGIOutput.FindClosestMatchingMode
title: IDXGIOutput::FindClosestMatchingMode
author: windows-sdk-content
description: Finds the display mode that most closely matches the requested display mode.
old-location: direct3ddxgi\idxgioutput_findclosestmatchingmode.htm
old-project: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgioutput_findclosestmatchingmode.htm
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: FindClosestMatchingMode, FindClosestMatchingMode method [DXGI], FindClosestMatchingMode method [DXGI],IDXGIOutput interface, IDXGIOutput interface [DXGI],FindClosestMatchingMode method, IDXGIOutput.FindClosestMatchingMode, IDXGIOutput::FindClosestMatchingMode, c140400c-32d4-ec57-8da0-a37a23cfd5e4, direct3ddxgi.idxgioutput_findclosestmatchingmode, dxgi/IDXGIOutput::FindClosestMatchingMode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: DXGI_SWAP_EFFECT
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
product: Windows
targetos: Windows
req.lib: DXGI.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIOutput::FindClosestMatchingMode


## -description


<p class="CCE_Message">[Starting with Direct3D 11.1, we recommend not to use <b>FindClosestMatchingMode</b> anymore to find the display mode that most closely matches the requested display mode. Instead, use <a href="https://msdn.microsoft.com/D71ED536-0D90-4E0D-8683-6260E31EAF20">IDXGIOutput1::FindClosestMatchingMode1</a>, which supports stereo display mode.]

Finds the display mode that most closely matches the requested display mode.


## -parameters




### -param pModeToMatch [in]

Type: <b>const <a href="https://msdn.microsoft.com/ed39012c-0c3b-4c8e-ae83-c252c0fd3cff">DXGI_MODE_DESC</a>*</b>

The desired display mode (see <a href="https://msdn.microsoft.com/ed39012c-0c3b-4c8e-ae83-c252c0fd3cff">DXGI_MODE_DESC</a>). Members of <b>DXGI_MODE_DESC</b> can be unspecified indicating no preference for 
        that member.  A value of 0 for <b>Width</b> or <b>Height</b> indicates the value is unspecified.  If either <b>Width</b> or 
        <b>Height</b> are 0, both must be 0.  A numerator and denominator of 0 in <b>RefreshRate</b> indicate it is unspecified. Other members 
        of <b>DXGI_MODE_DESC</b> have enumeration values indicating the member is unspecified.  If <i>pConcernedDevice</i> is <b>NULL</b>, <b>Format</b>cannot be DXGI_FORMAT_UNKNOWN.


### -param pClosestMatch [out]

Type: <b><a href="https://msdn.microsoft.com/ed39012c-0c3b-4c8e-ae83-c252c0fd3cff">DXGI_MODE_DESC</a>*</b>

The mode that most closely matches <i>pModeToMatch</i>.


### -param pConcernedDevice [in, optional]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

A pointer to the Direct3D device interface. If this parameter is <b>NULL</b>, only modes whose format matches that of <i>pModeToMatch</i> will 
        be returned; otherwise, only those formats that are supported for scan-out by the device are returned. For info about the formats that are supported for scan-out by the device at each feature level:

<ul>
<li>
<a href="https://msdn.microsoft.com/0DC50FF3-3193-4F3B-9976-EE504C6FCC87">DXGI Format  Support for Direct3D Feature Level 12.1 Hardware</a>
</li>
<li>
<a href="https://msdn.microsoft.com/A039A82B-2E30-41A6-96B5-AD5538FE2285">DXGI Format  Support for Direct3D Feature Level 12.0 Hardware</a>
</li>
<li>
<a href="https://msdn.microsoft.com/90EADE0C-A984-4993-A3F8-D045C535DE64">DXGI Format  Support for Direct3D Feature Level 11.1 Hardware</a>
</li>
<li>
<a href="https://msdn.microsoft.com/735CDA40-557F-4D47-87B7-97A8E120B9D2">DXGI Format  Support for Direct3D Feature Level 11.0 Hardware</a>
</li>
<li>
<a href="direct3ddxgi.d3d11_graphics_programming_guide_dxgi_hw_formats_10level9">Hardware Support for Direct3D 10Level9 Formats</a>
</li>
<li>
<a href="https://msdn.microsoft.com/011ad888-1c1d-4cbd-ab70-12fb8adc000f">Hardware Support for Direct3D 10.1 Formats</a>
</li>
<li>
<a href="https://msdn.microsoft.com/529ced9a-d4fa-4b41-932b-343638cd5c7c">Hardware Support for Direct3D 10 Formats</a>
</li>
</ul>

## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a>.




## -remarks



<b>FindClosestMatchingMode</b> behaves similarly to the <a href="https://msdn.microsoft.com/D71ED536-0D90-4E0D-8683-6260E31EAF20">IDXGIOutput1::FindClosestMatchingMode1</a> except <b>FindClosestMatchingMode</b> considers only the mono display modes. <b>IDXGIOutput1::FindClosestMatchingMode1</b> considers only stereo modes if you set the <b>Stereo</b> member in the <a href="https://msdn.microsoft.com/8F44CF77-D3A1-44F7-AB7F-69E5727A4378">DXGI_MODE_DESC1</a> structure that <i>pModeToMatch</i> points to, and considers only mono modes if <b>Stereo</b> is not set.


<a href="https://msdn.microsoft.com/D71ED536-0D90-4E0D-8683-6260E31EAF20">IDXGIOutput1::FindClosestMatchingMode1</a> returns a matched display-mode set with only stereo modes or only mono modes.
<b>FindClosestMatchingMode</b> behaves as though you specified the input mode as mono.




## -see-also




<a href="https://msdn.microsoft.com/c641995e-a4d9-4bfb-bdc0-7ffbe77c3599">IDXGIOutput</a>
 

 

