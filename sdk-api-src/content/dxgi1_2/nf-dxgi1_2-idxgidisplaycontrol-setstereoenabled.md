---
UID: NF:dxgi1_2.IDXGIDisplayControl.SetStereoEnabled
title: IDXGIDisplayControl::SetStereoEnabled (dxgi1_2.h)
author: windows-sdk-content
description: Set a Boolean value to either enable or disable the operating system's stereoscopic 3D display behavior.
old-location: direct3ddxgi\idxgidisplaycontrol_SetStereoEnabled.htm
tech.root: direct3ddxgi
ms.assetid: 4A449444-287D-4F1D-9A86-F6165C38048F
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDXGIDisplayControl interface [DXGI],SetStereoEnabled method, IDXGIDisplayControl.SetStereoEnabled, IDXGIDisplayControl::SetStereoEnabled, SetStereoEnabled, SetStereoEnabled method [DXGI], SetStereoEnabled method [DXGI],IDXGIDisplayControl interface, direct3ddxgi.idxgidisplaycontrol_SetStereoEnabled, dxgi1_2/IDXGIDisplayControl::SetStereoEnabled
ms.topic: method
f1_keywords: 
 - "dxgi1_2/IDXGIDisplayControl.SetStereoEnabled"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dxgi.lib
 - Dxgi.dll
api_name:
 - IDXGIDisplayControl.SetStereoEnabled
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDXGIDisplayControl::SetStereoEnabled


## -description


Set a Boolean value to either enable or disable the operating system's stereoscopic 3D display behavior.


## -parameters




### -param enabled

A Boolean value that either enables or disables the operating system's stereoscopic 3D display behavior. TRUE enables the operating system's stereoscopic 3D display behavior and FALSE disables it.


## -returns



Returns nothing.




## -remarks



<b>Platform Update for Windows 7:  </b>On Windows 7 or Windows Server 2008 R2 with the <a href="https://support.microsoft.com/help/2670838">Platform Update for Windows 7</a> installed, <b>SetStereoEnabled</b> doesn't change stereoscopic 3D display behavior because stereoscopic 3D display behavior isn’t available with the Platform Update for Windows 7. For more info about the Platform Update for Windows 7, see <a href="https://docs.microsoft.com/windows/desktop/direct3darticles/platform-update-for-windows-7">Platform Update for Windows 7</a>. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgidisplaycontrol">IDXGIDisplayControl</a>
 

 

