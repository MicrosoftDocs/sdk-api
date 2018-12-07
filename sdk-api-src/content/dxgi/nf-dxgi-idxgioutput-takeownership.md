---
UID: NF:dxgi.IDXGIOutput.TakeOwnership
title: IDXGIOutput::TakeOwnership
author: windows-sdk-content
description: Takes ownership of an output.
old-location: direct3ddxgi\idxgioutput_takeownership.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgioutput_takeownership.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDXGIOutput interface [DXGI],TakeOwnership method, IDXGIOutput.TakeOwnership, IDXGIOutput::TakeOwnership, TakeOwnership, TakeOwnership method [DXGI], TakeOwnership method [DXGI],IDXGIOutput interface, bb1e2d75-a9d5-a0db-2197-ed0246f07a00, direct3ddxgi.idxgioutput_takeownership, dxgi/IDXGIOutput::TakeOwnership
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: DXGI.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DXGI.lib
 - DXGI.dll
api_name:
 - IDXGIOutput.TakeOwnership
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDXGIOutput::TakeOwnership


## -description


Takes ownership of an output.


## -parameters




### -param pDevice [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface of a device (such as an <a href="https://msdn.microsoft.com/en-us/library/Bb173528(v=VS.85).aspx">ID3D10Device</a>).


### -param Exclusive

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Set to <b>TRUE</b> to enable other threads or applications to take ownership of the device; otherwise, set to <b>FALSE</b>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns one of the <a href="https://msdn.microsoft.com/en-us/library/Bb509553(v=VS.85).aspx">DXGI_ERROR</a> values.




## -remarks



When you are finished with the output, call <a href="https://msdn.microsoft.com/en-us/library/Bb174554(v=VS.85).aspx">IDXGIOutput::ReleaseOwnership</a>.

<b>TakeOwnership</b> should not be called directly by applications, since results will be unpredictable. It is called implicitly by the DXGI swap chain object during full-screen transitions, and should not be used as a substitute for swap-chain methods.

<h3><a id="Notes_for_Windows_Store_apps"></a><a id="notes_for_windows_store_apps"></a><a id="NOTES_FOR_WINDOWS_STORE_APPS"></a>Notes for Windows Store apps</h3>
If a Windows Store app uses <b>TakeOwnership</b>, it fails with <a href="https://msdn.microsoft.com/en-us/library/Bb509553(v=VS.85).aspx">DXGI_ERROR_NOT_CURRENTLY_AVAILABLE</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb174546(v=VS.85).aspx">IDXGIOutput</a>
 

 

