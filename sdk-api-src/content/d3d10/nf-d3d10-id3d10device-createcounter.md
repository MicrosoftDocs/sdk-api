---
UID: NF:d3d10.ID3D10Device.CreateCounter
title: ID3D10Device::CreateCounter
author: windows-sdk-content
description: Create a counter object for measuring GPU performance.
old-location: direct3d10\id3d10device_createcounter.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_createcounter.htm
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: 225224fa-54a2-8903-494c-754ad030e0af, CreateCounter, CreateCounter method [Direct3D 10], CreateCounter method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],CreateCounter method, ID3D10Device.CreateCounter, ID3D10Device::CreateCounter, d3d10/ID3D10Device::CreateCounter, direct3d10.id3d10device_createcounter
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d10.h
req.include-header: 
req.redist: 
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
req.typenames: D3D10_USAGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Device.CreateCounter
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10Device::CreateCounter


## -description


Create a counter object for measuring GPU performance.


## -parameters




### -param pCounterDesc [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/Bb204905(v=VS.85).aspx">D3D10_COUNTER_DESC</a>*</b>

Pointer to a counter description (see <a href="https://msdn.microsoft.com/en-us/library/Bb204905(v=VS.85).aspx">D3D10_COUNTER_DESC</a>).


### -param ppCounter [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173514(v=VS.85).aspx">ID3D10Counter</a>**</b>

Address of a pointer to a counter (see <a href="https://msdn.microsoft.com/en-us/library/Bb173514(v=VS.85).aspx">ID3D10Counter Interface</a>).


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If this function succeeds, it will return S_OK. If it fails, possible return values are: S_FALSE, E_OUTOFMEMORY, DXGI_ERROR_UNSUPPORTED, DXGI_ERROR_NONEXCLUSIVE, or E_INVALIDARG.

DXGI_ERROR_UNSUPPORTED is returned whenever the application requests to create a well-known counter, but the current device does not support it.

DXGI_ERROR_NONEXCLUSIVE indicates that another device object is currently using the counters, so they cannot be used by this device at the moment.

E_INVALIDARG is returned whenever an out-of-range well-known or device-dependent counter is requested, or when the simulataneously active counters have been exhausted.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173528(v=VS.85).aspx">ID3D10Device Interface</a>
 

 

