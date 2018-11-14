---
UID: NF:d3d11.ID3D11DeviceContext.Unmap
title: ID3D11DeviceContext::Unmap
author: windows-sdk-content
description: Invalidate the pointer to a resource and reenable the GPU's access to that resource.
old-location: direct3d11\id3d11devicecontext_unmap.htm
tech.root: direct3d11
ms.assetid: 67797b77-c0a5-47b4-ba54-4282b6aa5b13
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 83629121-3205-9ee6-6495-a815e1ef2ab5, ID3D11DeviceContext interface [Direct3D 11],Unmap method, ID3D11DeviceContext.Unmap, ID3D11DeviceContext::Unmap, Unmap, Unmap method [Direct3D 11], Unmap method [Direct3D 11],ID3D11DeviceContext interface, d3d11/ID3D11DeviceContext::Unmap, direct3d11.id3d11devicecontext_unmap
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
 - ID3D11DeviceContext.Unmap
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
- ID3D11DeviceContext.Unmap
: 
---

# ID3D11DeviceContext::Unmap


## -description


Invalidate the pointer to a resource and reenable the GPU's access to that resource.


## -parameters




### -param pResource [in]

Type: <b><a href="https://msdn.microsoft.com/3823ec00-cb3c-43ce-9f1a-be4e1e99d587">ID3D11Resource</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/3823ec00-cb3c-43ce-9f1a-be4e1e99d587">ID3D11Resource</a> interface.
          


### -param Subresource [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A subresource to be unmapped.


## -returns



Returns nothing.




## -remarks



For info about how to use <b>Unmap</b>, see <a href="https://msdn.microsoft.com/E73EA4B0-BD14-430C-89CA-4CFCF92C7548">How to: Use dynamic resources</a>.
      

<b>Windows Phone 8:
        </b> This API is supported.
      




## -see-also




<a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>
 

 

