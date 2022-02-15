---
UID: NN:dxgi1_2.IDXGIDisplayControl
title: IDXGIDisplayControl (dxgi1_2.h)
description: The IDXGIDisplayControl interface exposes methods to indicate user preference for the operating system's stereoscopic 3D display behavior and to set stereoscopic 3D display status to enable or disable.
helpviewer_keywords: ["IDXGIDisplayControl","IDXGIDisplayControl interface [DXGI]","IDXGIDisplayControl interface [DXGI]","described","direct3ddxgi.idxgidisplaycontrol","dxgi1_2/IDXGIDisplayControl"]
old-location: direct3ddxgi\idxgidisplaycontrol.htm
tech.root: direct3ddxgi
ms.assetid: 8E9A059E-D7E2-4179-9ECA-D66BC9CD3757
ms.date: 12/05/2018
ms.keywords: IDXGIDisplayControl, IDXGIDisplayControl interface [DXGI], IDXGIDisplayControl interface [DXGI],described, direct3ddxgi.idxgidisplaycontrol, dxgi1_2/IDXGIDisplayControl
req.header: dxgi1_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps only]
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
 - IDXGIDisplayControl
 - dxgi1_2/IDXGIDisplayControl
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
 - IDXGIDisplayControl
---

# IDXGIDisplayControl interface


## -description

The <b>IDXGIDisplayControl</b> interface exposes methods to indicate user preference for the operating system's stereoscopic 3D display behavior and to set stereoscopic 3D display status to enable or disable.
        



We recommend that you not use <b>IDXGIDisplayControl</b> to query or set system-wide stereoscopic 3D settings in your stereoscopic 3D apps. Instead, for your windowed apps, call the <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-iswindowedstereoenabled">IDXGIFactory2::IsWindowedStereoEnabled</a> method to determine whether to render in stereo; for your full-screen apps, call the <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutput1-getdisplaymodelist1">IDXGIOutput1::GetDisplayModeList1</a> method and then determine whether any of the returned display modes support rendering in stereo.

## -inheritance

The <b>IDXGIDisplayControl</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDXGIDisplayControl</b> also has these types of members:

## -remarks

<div class="alert"><b>Note</b>  The <b>IDXGIDisplayControl</b> interface is only used by the <b>Display</b> app of the operating system's Control Panel or by control applets from third party graphics vendors. This interface is not meant for developers of end-user apps.
        </div>
<div> </div>
<div class="alert"><b>Note</b>  The <b>IDXGIDisplayControl</b> interface does not exist for Windows Store apps.
        </div>
<div> </div>
Call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> from a factory object (<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgifactory">IDXGIFactory</a>, <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgifactory1">IDXGIFactory1</a> or <a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2">IDXGIFactory2</a>) to retrieve the <b>IDXGIDisplayControl</b> interface. The following code shows how.
        


```
IDXGIDisplayControl * pDXGIDisplayControl;
hr = g_pDXGIFactory->QueryInterface(__uuidof(IDXGIDisplayControl), (void **)&pDXGIDisplayControl);
```


The operating system processes changes to stereo-enabled configuration asynchronously. Therefore, these changes might not be immediately visible in every process that calls <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidisplaycontrol-isstereoenabled">IDXGIDisplayControl::IsStereoEnabled</a> to query for stereo configuration.  Control applets can use the <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerstereostatusevent">IDXGIFactory2::RegisterStereoStatusEvent</a> or <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerstereostatuswindow">IDXGIFactory2::RegisterStereoStatusWindow</a> method to register for notifications of all stereo configuration changes.
        

<b>Platform Update for Windows 7:  </b>Stereoscopic 3D display behavior isn’t available with the Platform Update for Windows 7. For more info about the Platform Update for Windows 7, see <a href="/windows/desktop/direct3darticles/platform-update-for-windows-7">Platform Update for Windows 7</a>.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
