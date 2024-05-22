---
UID: NF:dxgi1_5.IDXGIOutput5.DuplicateOutput1
title: IDXGIOutput5::DuplicateOutput1 (dxgi1_5.h)
description: Allows specifying a list of supported formats for fullscreen surfaces that can be returned by the IDXGIOutputDuplication object.
helpviewer_keywords: ["DuplicateOutput1","DuplicateOutput1 method [DXGI]","DuplicateOutput1 method [DXGI]","IDXGIOutput5 interface","IDXGIOutput5 interface [DXGI]","DuplicateOutput1 method","IDXGIOutput5.DuplicateOutput1","IDXGIOutput5::DuplicateOutput1","direct3ddxgi.idxgioutput5_duplicateoutput1","dxgi1_5/IDXGIOutput5::DuplicateOutput1"]
old-location: direct3ddxgi\idxgioutput5_duplicateoutput1.htm
tech.root: direct3ddxgi
ms.assetid: B6723F05-E0D9-4814-8AB8-796ECF9C5C0C
ms.date: 12/05/2018
ms.keywords: DuplicateOutput1, DuplicateOutput1 method [DXGI], DuplicateOutput1 method [DXGI],IDXGIOutput5 interface, IDXGIOutput5 interface [DXGI],DuplicateOutput1 method, IDXGIOutput5.DuplicateOutput1, IDXGIOutput5::DuplicateOutput1, direct3ddxgi.idxgioutput5_duplicateoutput1, dxgi1_5/IDXGIOutput5::DuplicateOutput1
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
req.lib: Dxgi.lib
req.dll: Dxgi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDXGIOutput5::DuplicateOutput1
 - dxgi1_5/IDXGIOutput5::DuplicateOutput1
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dxgi.dll
api_name:
 - IDXGIOutput5.DuplicateOutput1
---

# IDXGIOutput5::DuplicateOutput1


## -description

Allows specifying a list of supported formats for fullscreen surfaces that can be returned by the <a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgioutputduplication">IDXGIOutputDuplication</a> object.

## -parameters

### -param pDevice [in]

Type: <b>IUnknown*</b>

A pointer to the Direct3D device interface that you can use to process the desktop image. This device must be created from the adapter to which the output is connected.

### -param Flags

Type: <b>UINT</b>

A bitfield of <b>DXGI_OUTDUPL_FLAG</b> enumeration values describing the kind of capture surface to create.

### -param SupportedFormatsCount [in]

Type: <b>UINT</b>

Specifies the number of supported formats.

### -param pSupportedFormats [in]

Type: <b>const <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a>*</b>

Specifies an array, of length  <i>SupportedFormatsCount</i> of  <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a> entries.

### -param ppOutputDuplication [out]

Type: <b>IDXGIOutputDuplication**</b>

A pointer to a variable that receives the new <a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgioutputduplication">IDXGIOutputDuplication</a> interface.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>


<ul>
<li>S_OK if <b>DuplicateOutput1</b> successfully created the desktop duplication interface.</li>
<li>E_INVALIDARG for one of the following reasons: <ul>
<li>The specified device (<i>pDevice</i>) is invalid, was not created on the correct adapter, or was not created from <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgifactory1">IDXGIFactory1</a> (or a later version of a DXGI factory interface that inherits from <b>IDXGIFactory1</b>).</li>
<li>The calling application is already duplicating this desktop output.</li>
</ul>
</li>
<li>E_ACCESSDENIED if the application does not have access privilege  to the current desktop image.  For example, only an application that runs at LOCAL_SYSTEM can access the secure desktop.</li>
<li>
DXGI_ERROR_UNSUPPORTED if the created <a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgioutputduplication">IDXGIOutputDuplication</a> interface does not support the current desktop mode or scenario.  For example, 8bpp and non-DWM desktop modes are not supported.

If <b>DuplicateOutput1</b> fails with DXGI_ERROR_UNSUPPORTED, the application can wait for system notification of desktop switches and mode changes and then call <b>DuplicateOutput1</b> again after such a notification occurs.  For more information, see the desktop switch (<a href="/windows/desktop/WinAuto/event-constants">EVENT_SYSTEM_DESKTOPSWITCH</a>) and mode change notification (<a href="/windows/desktop/gdi/wm-displaychange">WM_DISPLAYCHANGE</a>). 

</li>
<li>DXGI_ERROR_NOT_CURRENTLY_AVAILABLE if DXGI reached the limit on the maximum number of concurrent duplication applications (default of four). Therefore, the calling application cannot create any desktop duplication interfaces until the other applications close.</li>
<li>DXGI_ERROR_SESSION_DISCONNECTED if <b>DuplicateOutput1</b> failed because the session is currently disconnected.</li>
<li>Other error codes are described in the <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a> topic.</li>
</ul>

## -remarks

This method allows directly receiving the original back buffer format used by a running fullscreen application. For comparison, using the original <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutput1-duplicateoutput">DuplicateOutput</a> function always converts the fullscreen surface to a 32-bit BGRA format. In cases where the current fullscreen application is using a different buffer format, a conversion to 32-bit BGRA incurs a performance penalty. Besides the performance benefit of being able to skip format conversion, using <b>DuplicateOutput1</b> also allows receiving the full gamut of colors in cases where a high-color format (such as R10G10B10A2) is being presented.



The <i>pSupportedFormats</i> array should only contain display scan-out formats. See <a href="/windows/desktop/direct3ddxgi/format-support-for-direct3d-11-0-feature-level-hardware">Format Support for Direct3D Feature Level 11.0 Hardware</a> for  required scan-out formats at each feature level. If the current fullscreen buffer format is not contained in the <i>pSupportedFormats</i> array, DXGI will pick one of the supplied formats and convert the fullscreen buffer to that format before returning from <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe">IDXGIOutputDuplication::AcquireNextFrame</a>. The list of supported formats should always contain DXGI_FORMAT_B8G8R8A8_UNORM, as this is the most common format for the desktop.

## -see-also

<a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutput1-duplicateoutput">DuplicateOutput</a>



<a href="/windows/desktop/api/dxgi1_5/nn-dxgi1_5-idxgioutput5">IDXGIOutput5</a>
