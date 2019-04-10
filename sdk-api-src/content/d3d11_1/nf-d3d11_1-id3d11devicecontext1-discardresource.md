---
UID: NF:d3d11_1.ID3D11DeviceContext1.DiscardResource
title: ID3D11DeviceContext1::DiscardResource (d3d11_1.h)
author: windows-sdk-content
description: Discards a resource from the device context.
old-location: direct3d11\id3d11devicecontext1_discardresource.htm
tech.root: direct3d11
ms.assetid: 6C27231E-BF61-4D50-B5B1-59961B82534B
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DiscardResource, DiscardResource method [Direct3D 11], DiscardResource method [Direct3D 11],ID3D11DeviceContext1 interface, ID3D11DeviceContext1 interface [Direct3D 11],DiscardResource method, ID3D11DeviceContext1.DiscardResource, ID3D11DeviceContext1::DiscardResource, d3d11_1/ID3D11DeviceContext1::DiscardResource, direct3d11.id3d11devicecontext1_discardresource
ms.topic: method
req.header: d3d11_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - ID3D11DeviceContext1.DiscardResource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11DeviceContext1::DiscardResource


## -description


Discards a resource from the device context.


## -parameters




### -param pResource [in]

Type: <b><a href="https://msdn.microsoft.com/3823ec00-cb3c-43ce-9f1a-be4e1e99d587">ID3D11Resource</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/3823ec00-cb3c-43ce-9f1a-be4e1e99d587">ID3D11Resource</a> interface for the resource to discard. The resource must have been created with usage <a href="https://msdn.microsoft.com/en-us/library/Ff476259(v=VS.85).aspx">D3D11_USAGE_DEFAULT</a> or <a href="https://msdn.microsoft.com/en-us/library/Ff476259(v=VS.85).aspx">D3D11_USAGE_DYNAMIC</a>, otherwise the runtime drops the call to <b>DiscardResource</b>; if the debug layer is enabled, the runtime returns an error message.


## -returns



Returns nothing




## -remarks



<b>DiscardResource</b> informs the graphics processing unit (GPU) that the existing content in the resource that <i>pResource</i> points to is no longer needed.




## -see-also




<a href="https://msdn.microsoft.com/DD2A556D-AEF0-407E-A497-CF17ACDEB1A7">ID3D11DeviceContext1</a>
 

 

