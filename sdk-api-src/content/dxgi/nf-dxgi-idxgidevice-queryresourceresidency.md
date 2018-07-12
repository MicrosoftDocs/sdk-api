---
UID: NF:dxgi.IDXGIDevice.QueryResourceResidency
title: IDXGIDevice::QueryResourceResidency
author: windows-sdk-content
description: Gets the residency status of an array of resources.
old-location: direct3ddxgi\idxgidevice_queryresourceresidency.htm
old-project: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgidevice_queryresourceresidency.htm
ms.author: windowssdkdev
ms.date: 07/02/2018
ms.keywords: 0f2dfe96-267a-14d2-b7ec-deb2ed3c3450, IDXGIDevice interface [DXGI],QueryResourceResidency method, IDXGIDevice.QueryResourceResidency, IDXGIDevice::QueryResourceResidency, QueryResourceResidency, QueryResourceResidency method [DXGI], QueryResourceResidency method [DXGI],IDXGIDevice interface, direct3ddxgi.idxgidevice_queryresourceresidency, dxgi/IDXGIDevice::QueryResourceResidency
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dxgi.h
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
tech.root: 
req.typenames: DXGI_SWAP_EFFECT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DXGI.lib
 - DXGI.dll
api_name:
 - IDXGIDevice.QueryResourceResidency
product: Windows
targetos: Windows
req.lib: DXGI.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIDevice::QueryResourceResidency


## -description


Gets the residency status of an array of resources.


## -parameters




### -param ppResources [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

An array of <a href="https://msdn.microsoft.com/library/Bb174560(v=VS.85).aspx">IDXGIResource</a> interfaces.


### -param pResidencyStatus [out]

Type: <b><a href="https://msdn.microsoft.com/library/Bb173070(v=VS.85).aspx">DXGI_RESIDENCY</a>*</b>

An array of <a href="https://msdn.microsoft.com/library/Bb173070(v=VS.85).aspx">DXGI_RESIDENCY</a> flags. Each element describes the residency status for corresponding element in 
        the <i>ppResources</i> argument array.


### -param NumResources

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of resources in the <i>ppResources</i> argument array and <i>pResidencyStatus</i> argument array.


## -returns



Type: <b><a href="https://msdn.microsoft.com/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns S_OK if successful; otherwise, returns <a href="https://msdn.microsoft.com/library/Bb509553(v=VS.85).aspx">DXGI_ERROR_DEVICE_REMOVED</a>, E_INVALIDARG, or 
      E_POINTER (see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a> and WinError.h for more information).




## -remarks



The information returned by the <i>pResidencyStatus</i> argument array describes the residency status at the time that the <b>QueryResourceResidency</b> method was called.  
      

<div class="alert"><b>Note</b>  The residency status will constantly change.</div>
<div> </div>
If you call the <b>QueryResourceResidency</b> method during a device removed state, the <i>pResidencyStatus</i> argument will return the <a href="https://msdn.microsoft.com/library/Bb173070(v=VS.85).aspx">DXGI_RESIDENCY_RESIDENT_IN_SHARED_MEMORY</a> flag.

<div class="alert"><b>Note</b>  This method should not be called every frame as it incurs a non-trivial amount of overhead.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/library/Bb174527(v=VS.85).aspx">IDXGIDevice</a>
 

 

