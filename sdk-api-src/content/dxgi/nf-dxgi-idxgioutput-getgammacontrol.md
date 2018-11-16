---
UID: NF:dxgi.IDXGIOutput.GetGammaControl
title: IDXGIOutput::GetGammaControl
author: windows-sdk-content
description: Gets the gamma control settings.
old-location: direct3ddxgi\idxgioutput_getgammacontrol.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgioutput_getgammacontrol.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetGammaControl, GetGammaControl method [DXGI], GetGammaControl method [DXGI],IDXGIOutput interface, IDXGIOutput interface [DXGI],GetGammaControl method, IDXGIOutput.GetGammaControl, IDXGIOutput::GetGammaControl, direct3ddxgi.idxgioutput_getgammacontrol, dxgi/IDXGIOutput::GetGammaControl, eec103ab-9b5d-9ed5-ce8f-90664ac48789
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
 - IDXGIOutput.GetGammaControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- dxgi.h
: 
- IDXGIOutput.GetGammaControl
: 
---

# IDXGIOutput::GetGammaControl


## -description


Gets the gamma control settings.


## -parameters




### -param pArray [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173061(v=VS.85).aspx">DXGI_GAMMA_CONTROL</a>*</b>

An array of gamma control settings (see <a href="https://msdn.microsoft.com/en-us/library/Bb173061(v=VS.85).aspx">DXGI_GAMMA_CONTROL</a>).


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns one of the <a href="https://msdn.microsoft.com/en-us/library/Bb509553(v=VS.85).aspx">DXGI_ERROR</a> values.




## -remarks




<div class="alert"><b>Note</b>  Calling this method is only supported while in full-screen mode.</div>
<div> </div>


For info about using gamma correction, see <a href="https://msdn.microsoft.com/97ACDAE3-514E-4AAF-A27D-E5FFC162DB2A">Using gamma correction</a>. 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb174546(v=VS.85).aspx">IDXGIOutput</a>
 

 

