---
UID: NF:d3d11.ID3D11View.GetResource
title: ID3D11View::GetResource (d3d11.h)
author: windows-sdk-content
description: Get the resource that is accessed through this view.
old-location: direct3d11\id3d11view_getresource.htm
tech.root: direct3d11
ms.assetid: f6f6c4db-80c0-49bc-bd15-53e3a52d9f3c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 9a136bd2-66f9-8800-9ce0-d8b9c402d899, GetResource, GetResource method [Direct3D 11], GetResource method [Direct3D 11],ID3D11View interface, ID3D11View interface [Direct3D 11],GetResource method, ID3D11View.GetResource, ID3D11View::GetResource, d3d11/ID3D11View::GetResource, direct3d11.id3d11view_getresource
ms.topic: method
f1_keywords: 
 - "d3d11/ID3D11View.GetResource"
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
 - ID3D11View.GetResource
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D11View::GetResource


## -description


Get the resource that is accessed through this view.


## -parameters




### -param ppResource [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11resource">ID3D11Resource</a>**</b>

Address of a pointer to the resource that is accessed through this view. (See <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11resource">ID3D11Resource</a>.)


## -returns



Returns nothing.




## -remarks



This function increments the reference count of the resource by one, so it is necessary to call <b>Release</b> on the returned pointer when the application is done with it. Destroying (or losing) the returned pointer before <b>Release</b> is called will result in a memory leak.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11view">ID3D11View</a>
 

 

