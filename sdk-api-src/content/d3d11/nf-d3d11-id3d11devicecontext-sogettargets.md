---
UID: NF:d3d11.ID3D11DeviceContext.SOGetTargets
title: ID3D11DeviceContext::SOGetTargets
author: windows-sdk-content
description: Get the target output buffers for the stream-output stage of the pipeline.
old-location: direct3d11\id3d11devicecontext_sogettargets.htm
tech.root: direct3d11
ms.assetid: 878402ed-0c89-42db-8210-d9a90b347226
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 90e06f28-a9a0-3b66-9901-3e60886b896d, ID3D11DeviceContext interface [Direct3D 11],SOGetTargets method, ID3D11DeviceContext.SOGetTargets, ID3D11DeviceContext::SOGetTargets, SOGetTargets, SOGetTargets method [Direct3D 11], SOGetTargets method [Direct3D 11],ID3D11DeviceContext interface, d3d11/ID3D11DeviceContext::SOGetTargets, direct3d11.id3d11devicecontext_sogettargets
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d11.h
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11DeviceContext.SOGetTargets
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d11.h
: 
- ID3D11DeviceContext.SOGetTargets
: 
---

# ID3D11DeviceContext::SOGetTargets


## -description


Get the target output buffers for the stream-output stage of the pipeline.


## -parameters




### -param NumBuffers [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Number of buffers to get.


### -param ppSOTargets [out, optional]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476351(v=VS.85).aspx">ID3D11Buffer</a>**</b>

An array of output buffers (see <a href="https://msdn.microsoft.com/en-us/library/Ff476351(v=VS.85).aspx">ID3D11Buffer</a>) to be retrieved from the device.
          


## -returns



Returns nothing.




## -remarks



A maximum of four output buffers can be retrieved.

The offsets to the output buffers pointed to in the returned <i>ppSOTargets</i> array may be assumed to be -1 (append), as defined for use in <a href="https://msdn.microsoft.com/en-us/library/Ff476484(v=VS.85).aspx">ID3D11DeviceContext::SOSetTargets</a>.
        

Any returned interfaces will have their reference count incremented by one. Applications should call IUnknown::Release on the returned interfaces when they are no longer needed to avoid memory leaks.

<b>Windows Phone 8:
        </b> This API is supported.
      




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476385(v=VS.85).aspx">ID3D11DeviceContext</a>
 

 

