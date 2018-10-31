---
UID: NF:dxgi1_2.IDXGIDisplayControl.IsStereoEnabled
title: IDXGIDisplayControl::IsStereoEnabled
author: windows-sdk-content
description: Retrieves a Boolean value that indicates whether the operating system's stereoscopic 3D display behavior is enabled.
old-location: direct3ddxgi\idxgidisplaycontrol_IsStereoEnabled.htm
tech.root: direct3ddxgi
ms.assetid: AE6AA254-3534-4E0F-A206-BAC4536B8B80
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IDXGIDisplayControl interface [DXGI],IsStereoEnabled method, IDXGIDisplayControl.IsStereoEnabled, IDXGIDisplayControl::IsStereoEnabled, IsStereoEnabled, IsStereoEnabled method [DXGI], IsStereoEnabled method [DXGI],IDXGIDisplayControl interface, direct3ddxgi.idxgidisplaycontrol_IsStereoEnabled, dxgi1_2/IDXGIDisplayControl::IsStereoEnabled
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IDXGIDisplayControl.IsStereoEnabled
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDXGIDisplayControl::IsStereoEnabled


## -description


Retrieves a Boolean value that indicates whether the operating system's stereoscopic 3D display behavior is enabled.


## -parameters






## -returns



<b>IsStereoEnabled</b> returns TRUE when the operating system's stereoscopic 3D display behavior is enabled and FALSE when this behavior is disabled.

<b>Platform Update for Windows 7:  </b>On Windows 7 or Windows Server 2008 R2 with the <a href="http://support.microsoft.com/kb/2670838">Platform Update for Windows 7</a> installed, <b>IsStereoEnabled</b> always returns FALSE because stereoscopic 3D display behavior isn’t available with the Platform Update for Windows 7. For more info about the Platform Update for Windows 7, see <a href="https://msdn.microsoft.com/C6DC0D38-E17C-4924-AF7C-6AE74C6C50D1">Platform Update for Windows 7</a>. 




## -remarks



You pass a Boolean value to the  <a href="https://msdn.microsoft.com/4A449444-287D-4F1D-9A86-F6165C38048F">IDXGIDisplayControl::SetStereoEnabled</a> method to either enable or disable the operating system's stereoscopic 3D display behavior. TRUE enables the operating system's stereoscopic 3D display behavior and FALSE disables it.




## -see-also




<a href="https://msdn.microsoft.com/8E9A059E-D7E2-4179-9ECA-D66BC9CD3757">IDXGIDisplayControl</a>
 

 

