---
UID: NF:dxgi1_2.IDXGIDisplayControl.IsStereoEnabled
title: IDXGIDisplayControl::IsStereoEnabled (dxgi1_2.h)
description: Retrieves a Boolean value that indicates whether the operating system's stereoscopic 3D display behavior is enabled.
helpviewer_keywords: ["IDXGIDisplayControl interface [DXGI]","IsStereoEnabled method","IDXGIDisplayControl.IsStereoEnabled","IDXGIDisplayControl::IsStereoEnabled","IsStereoEnabled","IsStereoEnabled method [DXGI]","IsStereoEnabled method [DXGI]","IDXGIDisplayControl interface","direct3ddxgi.idxgidisplaycontrol_IsStereoEnabled","dxgi1_2/IDXGIDisplayControl::IsStereoEnabled"]
old-location: direct3ddxgi\idxgidisplaycontrol_IsStereoEnabled.htm
tech.root: direct3ddxgi
ms.assetid: AE6AA254-3534-4E0F-A206-BAC4536B8B80
ms.date: 12/05/2018
ms.keywords: IDXGIDisplayControl interface [DXGI],IsStereoEnabled method, IDXGIDisplayControl.IsStereoEnabled, IDXGIDisplayControl::IsStereoEnabled, IsStereoEnabled, IsStereoEnabled method [DXGI], IsStereoEnabled method [DXGI],IDXGIDisplayControl interface, direct3ddxgi.idxgidisplaycontrol_IsStereoEnabled, dxgi1_2/IDXGIDisplayControl::IsStereoEnabled
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
 - IDXGIDisplayControl::IsStereoEnabled
 - dxgi1_2/IDXGIDisplayControl::IsStereoEnabled
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
 - IDXGIDisplayControl.IsStereoEnabled
---

# IDXGIDisplayControl::IsStereoEnabled


## -description

Retrieves a Boolean value that indicates whether the operating system's stereoscopic 3D display behavior is enabled.



## -returns

<b>IsStereoEnabled</b> returns TRUE when the operating system's stereoscopic 3D display behavior is enabled and FALSE when this behavior is disabled.

<b>Platform Update for Windows 7:  </b>On Windows 7 or Windows Server 2008 R2 with the <a href="https://support.microsoft.com/help/2670838">Platform Update for Windows 7</a> installed, <b>IsStereoEnabled</b> always returns FALSE because stereoscopic 3D display behavior isn’t available with the Platform Update for Windows 7. For more info about the Platform Update for Windows 7, see <a href="/windows/desktop/direct3darticles/platform-update-for-windows-7">Platform Update for Windows 7</a>.

## -remarks

You pass a Boolean value to the  <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidisplaycontrol-setstereoenabled">IDXGIDisplayControl::SetStereoEnabled</a> method to either enable or disable the operating system's stereoscopic 3D display behavior. TRUE enables the operating system's stereoscopic 3D display behavior and FALSE disables it.

## -see-also

<a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgidisplaycontrol">IDXGIDisplayControl</a>
