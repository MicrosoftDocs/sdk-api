---
UID: NF:d3d11.ID3D11DeviceContext.Unmap
title: ID3D11DeviceContext::Unmap
author: windows-sdk-content
description: Invalidate the pointer to a resource and reenable the GPU's access to that resource.
old-location: direct3d11\id3d11devicecontext_unmap.htm
old-project: direct3d11
ms.assetid: 67797b77-c0a5-47b4-ba54-4282b6aa5b13
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 83629121-3205-9ee6-6495-a815e1ef2ab5, ID3D11DeviceContext interface [Direct3D 11],Unmap method, ID3D11DeviceContext.Unmap, ID3D11DeviceContext::Unmap, Unmap, Unmap method [Direct3D 11], Unmap method [Direct3D 11],ID3D11DeviceContext interface, d3d11/ID3D11DeviceContext::Unmap, direct3d11.id3d11devicecontext_unmap
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d11.h
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
req.typenames: D3D11_VPOV_DIMENSION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11DeviceContext.Unmap
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11DeviceContext::Unmap


## -description


Invalidate the pointer to a resource and reenable the GPU's access to that resource.


## -parameters




### -param pResource [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476584(v=VS.85).aspx">ID3D11Resource</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/en-us/library/Ff476584(v=VS.85).aspx">ID3D11Resource</a> interface.
          


### -param Subresource [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

A subresource to be unmapped.


## -returns



Returns nothing.




## -remarks



For info about how to use <b>Unmap</b>, see <a href="https://msdn.microsoft.com/en-us/library/Dn508285(v=VS.85).aspx">How to: Use dynamic resources</a>.
      

<b>Windows Phone 8:
        </b> This API is supported.
      




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476385(v=VS.85).aspx">ID3D11DeviceContext</a>
 

 

