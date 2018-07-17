---
UID: NF:dxgi.IDXGIOutput.GetGammaControlCapabilities
title: IDXGIOutput::GetGammaControlCapabilities
author: windows-sdk-content
description: Gets a description of the gamma-control capabilities.
old-location: direct3ddxgi\idxgioutput_getgammacontrolcapabilities.htm
old-project: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgioutput_getgammacontrolcapabilities.htm
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: 7a21bfd4-6142-892e-82c8-bfe1be182780, GetGammaControlCapabilities, GetGammaControlCapabilities method [DXGI], GetGammaControlCapabilities method [DXGI],IDXGIOutput interface, IDXGIOutput interface [DXGI],GetGammaControlCapabilities method, IDXGIOutput.GetGammaControlCapabilities, IDXGIOutput::GetGammaControlCapabilities, direct3ddxgi.idxgioutput_getgammacontrolcapabilities, dxgi/IDXGIOutput::GetGammaControlCapabilities
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
 - IDXGIOutput.GetGammaControlCapabilities
product: Windows
targetos: Windows
req.lib: DXGI.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIOutput::GetGammaControlCapabilities


## -description


Gets a description of the gamma-control capabilities.


## -parameters




### -param pGammaCaps [out]

Type: <b><a href="https://msdn.microsoft.com/library/Bb173062(v=VS.85).aspx">DXGI_GAMMA_CONTROL_CAPABILITIES</a>*</b>

A pointer to a  description of the gamma-control capabilities (see <a href="https://msdn.microsoft.com/library/Bb173062(v=VS.85).aspx">DXGI_GAMMA_CONTROL_CAPABILITIES</a>).


## -returns



Type: <b><a href="https://msdn.microsoft.com/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns one of the <a href="https://msdn.microsoft.com/library/Bb509553(v=VS.85).aspx">DXGI_ERROR</a> values.




## -remarks




<div class="alert"><b>Note</b>  Calling this method is only supported while in full-screen mode.</div>
<div> </div>


For info about using gamma correction, see <a href="https://msdn.microsoft.com/97ACDAE3-514E-4AAF-A27D-E5FFC162DB2A">Using gamma correction</a>. 




## -see-also




<a href="https://msdn.microsoft.com/library/Bb174546(v=VS.85).aspx">IDXGIOutput</a>
 

 

