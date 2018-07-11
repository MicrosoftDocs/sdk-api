---
UID: NF:dxgi.IDXGIOutput.SetGammaControl
title: IDXGIOutput::SetGammaControl
author: windows-sdk-content
description: Sets the gamma controls.
old-location: direct3ddxgi\idxgioutput_setgammacontrol.htm
old-project: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgioutput_setgammacontrol.htm
ms.author: windowssdkdev
ms.date: 07/02/2018
ms.keywords: 1363de75-ecbe-4dfc-a09c-6cb809f2a5cf, IDXGIOutput interface [DXGI],SetGammaControl method, IDXGIOutput.SetGammaControl, IDXGIOutput::SetGammaControl, SetGammaControl, SetGammaControl method [DXGI], SetGammaControl method [DXGI],IDXGIOutput interface, direct3ddxgi.idxgioutput_setgammacontrol, dxgi/IDXGIOutput::SetGammaControl
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
 - IDXGIOutput.SetGammaControl
product: Windows
targetos: Windows
req.lib: DXGI.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIOutput::SetGammaControl


## -description


Sets the gamma controls.


## -parameters




### -param pArray [in]

Type: <b>const <a href="https://msdn.microsoft.com/1c215306-f278-4843-8411-eb7e45fb3054">DXGI_GAMMA_CONTROL</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/1c215306-f278-4843-8411-eb7e45fb3054">DXGI_GAMMA_CONTROL</a> structure that describes the gamma curve to set.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns one of the <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a> values.




## -remarks




<div class="alert"><b>Note</b>  Calling this method is only supported while in full-screen mode.</div>
<div> </div>


For info about using gamma correction, see <a href="https://msdn.microsoft.com/97ACDAE3-514E-4AAF-A27D-E5FFC162DB2A">Using gamma correction</a>. 




## -see-also




<a href="https://msdn.microsoft.com/c641995e-a4d9-4bfb-bdc0-7ffbe77c3599">IDXGIOutput</a>
 

 

