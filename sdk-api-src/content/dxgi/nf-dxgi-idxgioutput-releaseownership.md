---
UID: NF:dxgi.IDXGIOutput.ReleaseOwnership
title: IDXGIOutput::ReleaseOwnership
author: windows-sdk-content
description: Releases ownership of the output.
old-location: direct3ddxgi\idxgioutput_releaseownership.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgioutput_releaseownership.htm
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: 85bdbad9-3499-5766-c623-04b46be2a80a, IDXGIOutput interface [DXGI],ReleaseOwnership method, IDXGIOutput.ReleaseOwnership, IDXGIOutput::ReleaseOwnership, ReleaseOwnership, ReleaseOwnership method [DXGI], ReleaseOwnership method [DXGI],IDXGIOutput interface, direct3ddxgi.idxgioutput_releaseownership, dxgi/IDXGIOutput::ReleaseOwnership
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
 - IDXGIOutput.ReleaseOwnership
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDXGIOutput::ReleaseOwnership


## -description


Releases ownership of the output.


## -parameters






## -returns



Returns nothing.




## -remarks



If you are not using a swap chain, get access to an output by calling <a href="https://msdn.microsoft.com/8687a41c-8d18-47e2-bb58-ccbf6a21566f">IDXGIOutput::TakeOwnership</a> and release it when you are finished by calling <b>IDXGIOutput::ReleaseOwnership</b>. An application that uses a swap chain will typically not call either of these methods.




## -see-also




<a href="https://msdn.microsoft.com/c641995e-a4d9-4bfb-bdc0-7ffbe77c3599">IDXGIOutput</a>
 

 

