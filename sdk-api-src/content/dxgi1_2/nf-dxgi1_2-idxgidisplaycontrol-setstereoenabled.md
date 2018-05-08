---
UID: NF:dxgi1_2.IDXGIDisplayControl.SetStereoEnabled
title: IDXGIDisplayControl::SetStereoEnabled
author: windows-driver-content
description: Set a Boolean value to either enable or disable the operating system's stereoscopic 3D display behavior.
old-location: direct3ddxgi\idxgidisplaycontrol_SetStereoEnabled.htm
old-project: direct3ddxgi
ms.assetid: 4A449444-287D-4F1D-9A86-F6165C38048F
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: IDXGIDisplayControl interface [DXGI],SetStereoEnabled method, IDXGIDisplayControl.SetStereoEnabled, IDXGIDisplayControl::SetStereoEnabled, SetStereoEnabled, SetStereoEnabled method [DXGI], SetStereoEnabled method [DXGI],IDXGIDisplayControl interface, direct3ddxgi.idxgidisplaycontrol_SetStereoEnabled, dxgi1_2/IDXGIDisplayControl::SetStereoEnabled
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
req.typenames: DXGI_OFFER_RESOURCE_PRIORITY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Dxgi.lib
-	Dxgi.dll
api_name:
-	IDXGIDisplayControl.SetStereoEnabled
product: Windows
targetos: Windows
req.lib: Dxgi.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
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



<b>Platform Update for Windows 7:  </b>On Windows 7 or Windows Server 2008 R2 with the <a href="http://support.microsoft.com/kb/2670838">Platform Update for Windows 7</a> installed, <b>SetStereoEnabled</b> doesn't change stereoscopic 3D display behavior because stereoscopic 3D display behavior isn’t available with the Platform Update for Windows 7. For more info about the Platform Update for Windows 7, see <a href="https://msdn.microsoft.com/C6DC0D38-E17C-4924-AF7C-6AE74C6C50D1">Platform Update for Windows 7</a>. 




## -see-also




<a href="https://msdn.microsoft.com/8E9A059E-D7E2-4179-9ECA-D66BC9CD3757">IDXGIDisplayControl</a>
 

 

