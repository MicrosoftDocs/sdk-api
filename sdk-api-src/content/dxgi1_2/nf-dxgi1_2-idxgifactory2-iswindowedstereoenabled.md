---
UID: NF:dxgi1_2.IDXGIFactory2.IsWindowedStereoEnabled
title: IDXGIFactory2::IsWindowedStereoEnabled (dxgi1_2.h)
description: Determines whether to use stereo mode.
helpviewer_keywords: ["IDXGIFactory2 interface [DXGI]","IsWindowedStereoEnabled method","IDXGIFactory2.IsWindowedStereoEnabled","IDXGIFactory2::IsWindowedStereoEnabled","IsWindowedStereoEnabled","IsWindowedStereoEnabled method [DXGI]","IsWindowedStereoEnabled method [DXGI]","IDXGIFactory2 interface","direct3ddxgi.idxgifactory2_iswindowedstereoenabled","dxgi1_2/IDXGIFactory2::IsWindowedStereoEnabled"]
old-location: direct3ddxgi\idxgifactory2_iswindowedstereoenabled.htm
tech.root: direct3ddxgi
ms.assetid: 81DA1DD6-7D36-4848-ADCB-1F7B765B0A62
ms.date: 12/05/2018
ms.keywords: IDXGIFactory2 interface [DXGI],IsWindowedStereoEnabled method, IDXGIFactory2.IsWindowedStereoEnabled, IDXGIFactory2::IsWindowedStereoEnabled, IsWindowedStereoEnabled, IsWindowedStereoEnabled method [DXGI], IsWindowedStereoEnabled method [DXGI],IDXGIFactory2 interface, direct3ddxgi.idxgifactory2_iswindowedstereoenabled, dxgi1_2/IDXGIFactory2::IsWindowedStereoEnabled
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
req.lib: Dxgi.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDXGIFactory2::IsWindowedStereoEnabled
 - dxgi1_2/IDXGIFactory2::IsWindowedStereoEnabled
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
 - IDXGIFactory2.IsWindowedStereoEnabled
---

## -description

Determines whether to use stereo mode.



## -returns

Indicates whether to use stereo mode. <b>TRUE</b> indicates that you can use stereo mode; otherwise, <b>FALSE</b>.

<b>Platform Update for Windows 7:  </b>On Windows 7 or Windows Server 2008 R2 with the <a href="https://support.microsoft.com/help/2670838">Platform Update for Windows 7</a> installed, <b>IsWindowedStereoEnabled</b> always returns FALSE because stereoscopic 3D display behavior isn’t available with the Platform Update for Windows 7. For more info about the Platform Update for Windows 7, see <a href="/windows/desktop/direct3darticles/platform-update-for-windows-7">Platform Update for Windows 7</a>.

## -remarks

We recommend that windowed applications call <b>IsWindowedStereoEnabled</b> before they attempt to use stereo. <b>IsWindowedStereoEnabled</b> returns <b>TRUE</b> if both of the following items are true:

<ul>
<li>All adapters in the computer have drivers that are capable of stereo. This only means that the driver is implemented to the Windows Display Driver Model (WDDM) for Windows 8 (WDDM 1.2). However, the adapter does not necessarily have to be able to scan out stereo.</li>
<li>The current desktop mode (desktop modes are mono) and system policy and hardware are configured so that the Desktop Window Manager (DWM) performs stereo composition on at least one adapter output.</li>
</ul>
The creation of a windowed stereo swap chain succeeds if the first requirement is met. However, if the adapter can't scan out stereo, the output on that adapter is reduced to mono.

The <a href="https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20stereoscopic%203D%20sample">Direct3D 11.1 Simple Stereo 3D Sample</a> shows how to add a stereoscopic 3D effect and how to respond to system stereo changes.

## -see-also

<a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2">IDXGIFactory2</a>
