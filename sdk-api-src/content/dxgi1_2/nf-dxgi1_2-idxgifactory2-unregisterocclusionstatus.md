---
UID: NF:dxgi1_2.IDXGIFactory2.UnregisterOcclusionStatus
title: IDXGIFactory2::UnregisterOcclusionStatus (dxgi1_2.h)
description: Unregisters a window or an event to stop it from receiving notification when occlusion status changes.
helpviewer_keywords: ["IDXGIFactory2 interface [DXGI]","UnregisterOcclusionStatus method","IDXGIFactory2.UnregisterOcclusionStatus","IDXGIFactory2::UnregisterOcclusionStatus","UnregisterOcclusionStatus","UnregisterOcclusionStatus method [DXGI]","UnregisterOcclusionStatus method [DXGI]","IDXGIFactory2 interface","direct3ddxgi.idxgifactory2_unregisterocclusionstatus","dxgi1_2/IDXGIFactory2::UnregisterOcclusionStatus"]
old-location: direct3ddxgi\idxgifactory2_unregisterocclusionstatus.htm
tech.root: direct3ddxgi
ms.assetid: 754A627C-0365-4AF5-A6DF-A8D646254ECF
ms.date: 12/05/2018
ms.keywords: IDXGIFactory2 interface [DXGI],UnregisterOcclusionStatus method, IDXGIFactory2.UnregisterOcclusionStatus, IDXGIFactory2::UnregisterOcclusionStatus, UnregisterOcclusionStatus, UnregisterOcclusionStatus method [DXGI], UnregisterOcclusionStatus method [DXGI],IDXGIFactory2 interface, direct3ddxgi.idxgifactory2_unregisterocclusionstatus, dxgi1_2/IDXGIFactory2::UnregisterOcclusionStatus
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
 - IDXGIFactory2::UnregisterOcclusionStatus
 - dxgi1_2/IDXGIFactory2::UnregisterOcclusionStatus
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
 - IDXGIFactory2.UnregisterOcclusionStatus
---

# IDXGIFactory2::UnregisterOcclusionStatus


## -description

Unregisters a window or an event to stop it from receiving notification when occlusion status changes.

## -parameters

### -param dwCookie [in]

A key value for the window or event to unregister. The  <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatuswindow">IDXGIFactory2::RegisterOcclusionStatusWindow</a> or  <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatusevent">IDXGIFactory2::RegisterOcclusionStatusEvent</a> method returns this value.

## -remarks

<b>Platform Update for Windows 7:  </b>On Windows 7 or Windows Server 2008 R2 with the <a href="https://support.microsoft.com/help/2670838">Platform Update for Windows 7</a> installed, <b>UnregisterOcclusionStatus</b> has no effect. For more info about the Platform Update for Windows 7, see <a href="/windows/desktop/direct3darticles/platform-update-for-windows-7">Platform Update for Windows 7</a>.

## -see-also

<a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2">IDXGIFactory2</a>