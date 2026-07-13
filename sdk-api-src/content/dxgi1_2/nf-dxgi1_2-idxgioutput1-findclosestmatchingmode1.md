---
UID: NF:dxgi1_2.IDXGIOutput1.FindClosestMatchingMode1
title: IDXGIOutput1::FindClosestMatchingMode1 (dxgi1_2.h)
description: Finds the display mode that most closely matches the requested display mode. (IDXGIOutput1.FindClosestMatchingMode1)
helpviewer_keywords: ["FindClosestMatchingMode1","FindClosestMatchingMode1 method [DXGI]","FindClosestMatchingMode1 method [DXGI]","IDXGIOutput1 interface","IDXGIOutput1 interface [DXGI]","FindClosestMatchingMode1 method","IDXGIOutput1.FindClosestMatchingMode1","IDXGIOutput1::FindClosestMatchingMode1","direct3ddxgi.idxgioutput1_findclosestmatchingmode1","dxgi1_2/IDXGIOutput1::FindClosestMatchingMode1"]
old-location: direct3ddxgi\idxgioutput1_findclosestmatchingmode1.htm
tech.root: direct3ddxgi
ms.assetid: D71ED536-0D90-4E0D-8683-6260E31EAF20
ms.date: 12/05/2018
ms.keywords: FindClosestMatchingMode1, FindClosestMatchingMode1 method [DXGI], FindClosestMatchingMode1 method [DXGI],IDXGIOutput1 interface, IDXGIOutput1 interface [DXGI],FindClosestMatchingMode1 method, IDXGIOutput1.FindClosestMatchingMode1, IDXGIOutput1::FindClosestMatchingMode1, direct3ddxgi.idxgioutput1_findclosestmatchingmode1, dxgi1_2/IDXGIOutput1::FindClosestMatchingMode1
req.header: dxgi1_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - IDXGIOutput1::FindClosestMatchingMode1
 - dxgi1_2/IDXGIOutput1::FindClosestMatchingMode1
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
 - IDXGIOutput1.FindClosestMatchingMode1
---

# IDXGIOutput1::FindClosestMatchingMode1


## -description

Finds the display mode that most closely matches the requested display mode.

## -parameters

### -param pModeToMatch [in]

A pointer to the <a href="/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_mode_desc1">DXGI_MODE_DESC1</a> structure that describes the display mode to match. Members of <b>DXGI_MODE_DESC1</b> can be unspecified, which indicates no preference for 
        that member.  A value of 0 for <b>Width</b> or <b>Height</b> indicates that the value is unspecified.  If either <b>Width</b> or 
        <b>Height</b> is 0, both must be 0.  A numerator and denominator of 0 in <b>RefreshRate</b> indicate it is unspecified. Other members 
        of <b>DXGI_MODE_DESC1</b> have enumeration values that indicate that the member is unspecified.  If <i>pConcernedDevice</i> is <b>NULL</b>, the <b>Format</b> member of <b>DXGI_MODE_DESC1</b> cannot be <b>DXGI_FORMAT_UNKNOWN</b>.

### -param pClosestMatch [out]

A pointer to the <a href="/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_mode_desc1">DXGI_MODE_DESC1</a> structure that receives a description of the display mode that most closely matches the display mode described at <i>pModeToMatch</i>.

### -param pConcernedDevice [in, optional]

A pointer to the Direct3D device interface. If this parameter is <b>NULL</b>, <b>FindClosestMatchingMode1</b> returns only modes whose format matches that of <i>pModeToMatch</i>; otherwise, <b>FindClosestMatchingMode1</b> returns only those formats that are supported for scan-out by the device. For info about the formats that are supported for scan-out by the device at each feature level:

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

Returns one of the error codes described in the <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a> topic.

## -remarks

Direct3D devices require UNORM formats.

<b>FindClosestMatchingMode1</b> finds the closest matching available display mode to the mode that you specify in <i>pModeToMatch</i>.

If you set the <b>Stereo</b> member in the <a href="/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_mode_desc1">DXGI_MODE_DESC1</a> structure to which <i>pModeToMatch</i> points to specify a stereo mode as input, <b>FindClosestMatchingMode1</b> considers only stereo modes. <b>FindClosestMatchingMode1</b> considers only mono modes if <b>Stereo</b> is not set.

<b>FindClosestMatchingMode1</b> resolves similarly ranked members of display modes (that is, all specified, or all unspecified, and so on) in the following order:

<ol>
<li><b>ScanlineOrdering</b></li>
<li><b>Scaling</b></li>
<li><b>Format</b></li>
<li><b>Resolution</b></li>
<li><b>RefreshRate</b></li>
</ol>
When <b>FindClosestMatchingMode1</b> determines the closest value for a particular member, it uses previously matched members to filter the display mode list choices, and 
      ignores other members. For example, when <b>FindClosestMatchingMode1</b> matches <b>Resolution</b>, it already filtered the display mode list by a certain <b>ScanlineOrdering</b>, 
      <b>Scaling</b>, and <b>Format</b>, while it ignores <b>RefreshRate</b>. This ordering doesn't define the absolute ordering for every usage scenario of <b>FindClosestMatchingMode1</b>, because 
      the application can choose some values initially, which effectively changes the order of resolving members.

<b>FindClosestMatchingMode1</b> matches members of the display mode one at a time, generally in a specified order.

If a member is unspecified, <b>FindClosestMatchingMode1</b> gravitates toward the values for the desktop related to this output. 
      If this output is not part of the desktop, <b>FindClosestMatchingMode1</b> uses the default desktop output to find values. If an application uses a fully unspecified 
      display mode, <b>FindClosestMatchingMode1</b> typically returns a display mode that matches the desktop settings for this output.  
      Because unspecified members are lower priority than specified members, <b>FindClosestMatchingMode1</b> resolves unspecified members later than specified members.

## -see-also

<a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgioutput1">IDXGIOutput1</a>
