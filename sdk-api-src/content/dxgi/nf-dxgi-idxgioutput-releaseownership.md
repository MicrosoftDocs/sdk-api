---
UID: NF:dxgi.IDXGIOutput.ReleaseOwnership
title: IDXGIOutput::ReleaseOwnership (dxgi.h)
description: Releases ownership of the output.
helpviewer_keywords: ["85bdbad9-3499-5766-c623-04b46be2a80a","IDXGIOutput interface [DXGI]","ReleaseOwnership method","IDXGIOutput.ReleaseOwnership","IDXGIOutput::ReleaseOwnership","ReleaseOwnership","ReleaseOwnership method [DXGI]","ReleaseOwnership method [DXGI]","IDXGIOutput interface","direct3ddxgi.idxgioutput_releaseownership","dxgi/IDXGIOutput::ReleaseOwnership"]
old-location: direct3ddxgi\idxgioutput_releaseownership.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgioutput_releaseownership.htm
ms.date: 12/05/2018
ms.keywords: 85bdbad9-3499-5766-c623-04b46be2a80a, IDXGIOutput interface [DXGI],ReleaseOwnership method, IDXGIOutput.ReleaseOwnership, IDXGIOutput::ReleaseOwnership, ReleaseOwnership, ReleaseOwnership method [DXGI], ReleaseOwnership method [DXGI],IDXGIOutput interface, direct3ddxgi.idxgioutput_releaseownership, dxgi/IDXGIOutput::ReleaseOwnership
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDXGIOutput::ReleaseOwnership
 - dxgi/IDXGIOutput::ReleaseOwnership
dev_langs:
 - c++
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
---

# IDXGIOutput::ReleaseOwnership


## -description

Releases ownership of the output.



## -remarks

If you are not using a swap chain, get access to an output by calling <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgioutput-takeownership">IDXGIOutput::TakeOwnership</a> and release it when you are finished by calling <b>IDXGIOutput::ReleaseOwnership</b>. An application that uses a swap chain will typically not call either of these methods.

## -see-also

<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgioutput">IDXGIOutput</a>
