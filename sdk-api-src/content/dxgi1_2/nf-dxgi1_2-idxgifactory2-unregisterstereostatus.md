---
UID: NF:dxgi1_2.IDXGIFactory2.UnregisterStereoStatus
title: IDXGIFactory2::UnregisterStereoStatus (dxgi1_2.h)

description: Unregisters a window or an event to stop it from receiving notification when stereo status changes.
old-location: direct3ddxgi\idxgifactory2_UnregisterStereoStatus.htm
tech.root: direct3ddxgi
ms.assetid: 8E3994C4-DA37-4D17-9F4D-C31E48CDE170

ms.date: 12/05/2018
ms.keywords: IDXGIFactory2 interface [DXGI],UnregisterStereoStatus method, IDXGIFactory2.UnregisterStereoStatus, IDXGIFactory2::UnregisterStereoStatus, UnregisterStereoStatus, UnregisterStereoStatus method [DXGI], UnregisterStereoStatus method [DXGI],IDXGIFactory2 interface, direct3ddxgi.idxgifactory2_UnregisterStereoStatus, dxgi1_2/IDXGIFactory2::UnregisterStereoStatus
ms.topic: method
f1_keywords: 
 - "dxgi1_2/IDXGIFactory2.UnregisterStereoStatus"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dxgi.lib
 - Dxgi.dll
api_name:
 - IDXGIFactory2.UnregisterStereoStatus
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDXGIFactory2::UnregisterStereoStatus


## -description


Unregisters a window or an event to stop it from receiving notification when stereo status changes.


## -parameters




### -param dwCookie [in]

A key value for the window or event to unregister. The  <a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerstereostatuswindow">IDXGIFactory2::RegisterStereoStatusWindow</a> or  <a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerstereostatusevent">IDXGIFactory2::RegisterStereoStatusEvent</a> method returns this value. 


## -returns



Returns nothing.




## -remarks



<b>Platform Update for Windows 7:  </b>On Windows 7 or Windows Server 2008 R2 with the <a href="https://support.microsoft.com/help/2670838">Platform Update for Windows 7</a> installed, <b>UnregisterStereoStatus</b> has no effect. For more info about the Platform Update for Windows 7, see <a href="https://docs.microsoft.com/windows/desktop/direct3darticles/platform-update-for-windows-7">Platform Update for Windows 7</a>. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2">IDXGIFactory2</a>
 

 

