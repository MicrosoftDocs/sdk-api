---
UID: NF:dxgi1_2.IDXGIOutput1.GetDisplayModeList1
title: IDXGIOutput1::GetDisplayModeList1 (dxgi1_2.h)
description: Gets the display modes that match the requested format and other input options. (IDXGIOutput1.GetDisplayModeList1)
helpviewer_keywords: ["GetDisplayModeList1","GetDisplayModeList1 method [DXGI]","GetDisplayModeList1 method [DXGI]","IDXGIOutput1 interface","IDXGIOutput1 interface [DXGI]","GetDisplayModeList1 method","IDXGIOutput1.GetDisplayModeList1","IDXGIOutput1::GetDisplayModeList1","direct3ddxgi.idxgioutput1_getdisplaymodelist1","dxgi1_2/IDXGIOutput1::GetDisplayModeList1"]
old-location: direct3ddxgi\idxgioutput1_getdisplaymodelist1.htm
tech.root: direct3ddxgi
ms.assetid: 49522ED9-30AD-4F39-96D2-BB6677D72349
ms.date: 12/05/2018
ms.keywords: GetDisplayModeList1, GetDisplayModeList1 method [DXGI], GetDisplayModeList1 method [DXGI],IDXGIOutput1 interface, IDXGIOutput1 interface [DXGI],GetDisplayModeList1 method, IDXGIOutput1.GetDisplayModeList1, IDXGIOutput1::GetDisplayModeList1, direct3ddxgi.idxgioutput1_getdisplaymodelist1, dxgi1_2/IDXGIOutput1::GetDisplayModeList1
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
 - IDXGIOutput1::GetDisplayModeList1
 - dxgi1_2/IDXGIOutput1::GetDisplayModeList1
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
 - IDXGIOutput1.GetDisplayModeList1
---

# IDXGIOutput1::GetDisplayModeList1


## -description

Gets the display modes that match the requested format and other input options.

## -parameters

### -param EnumFormat

A <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a>-typed value for the color format.

### -param Flags

A combination of <a href="/windows/desktop/direct3ddxgi/dxgi-enum-modes">DXGI_ENUM_MODES</a>-typed values that are combined by using a bitwise OR operation. The resulting value specifies options for display modes to include. You must specify DXGI_ENUM_MODES_SCALING to expose the display modes that require scaling.  Centered modes that require no 
            scaling and correspond directly to the display output are enumerated by default.

### -param pNumModes [in, out]

A pointer to a variable that receives the number of display modes that <b>GetDisplayModeList1</b> returns in the memory block to which <i>pDesc</i> points. Set <i>pDesc</i> to <b>NULL</b> so that <i>pNumModes</i> returns the number of display modes that match the format and the options.
        Otherwise, <i>pNumModes</i> returns the number of display modes returned in <i>pDesc</i>.

### -param pDesc [out, optional]

A pointer to a list of display modes; set to <b>NULL</b> to get the number of display modes.

## -returns

Returns one of the error codes described in the <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a> topic. It is rare, but possible, that the display modes available can change immediately after calling 
      this method, in which case DXGI_ERROR_MORE_DATA is returned (if there is not enough room for all the display modes).

## -remarks

<b>GetDisplayModeList1</b> is updated from  <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgioutput-getdisplaymodelist">GetDisplayModeList</a> to return a list of <a href="/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_mode_desc1">DXGI_MODE_DESC1</a> structures, which are updated mode descriptions.  <b>GetDisplayModeList</b> behaves as though it calls <b>GetDisplayModeList1</b> because  <b>GetDisplayModeList</b> can return all of the modes that are specified by <a href="/windows/desktop/direct3ddxgi/dxgi-enum-modes">DXGI_ENUM_MODES</a>, including stereo mode.  However, <b>GetDisplayModeList</b> returns a list of <a href="/previous-versions/windows/desktop/legacy/bb173064(v=vs.85)">DXGI_MODE_DESC</a> structures, which are the former mode descriptions and do not indicate stereo mode.

The <b>GetDisplayModeList1</b> method does not enumerate stereo modes unless you specify the <a href="/windows/desktop/direct3ddxgi/dxgi-enum-modes">DXGI_ENUM_MODES_STEREO</a> flag in the <i>Flags</i> parameter.  If you specify DXGI_ENUM_MODES_STEREO, stereo modes are included in the list of returned modes that the <i>pDesc</i> parameter points to.  In other words, the method returns both stereo and mono modes.

In general, when you switch from windowed to full-screen mode, a swap chain automatically chooses a display mode that meets (or exceeds) the resolution, color 
      depth, and refresh rate of the swap chain. To exercise more control over the display mode, use <b>GetDisplayModeList1</b> to poll the set of display modes that are validated 
      against monitor capabilities, or all modes that match the desktop (if the desktop settings are not validated against the monitor).

The following example code shows that you need to call <b>GetDisplayModeList1</b> twice. First call <b>GetDisplayModeList1</b> to get the number of modes available, and second call <b>GetDisplayModeList1</b> to return a description of the modes.


```

UINT num = 0;
DXGI_FORMAT format = DXGI_FORMAT_R32G32B32A32_FLOAT;
UINT flags         = DXGI_ENUM_MODES_INTERLACED;

pOutput->GetDisplayModeList1( format, flags, &num, 0);

...

DXGI_MODE_DESC1 * pDescs = new DXGI_MODE_DESC1[num];
pOutput->GetDisplayModeList1( format, flags, &num, pDescs);
      
```

## -see-also

<a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgioutput1">IDXGIOutput1</a>
