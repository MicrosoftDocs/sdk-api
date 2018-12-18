---
UID: NF:d3d11.ID3D11View.GetResource
title: ID3D11View::GetResource
author: windows-sdk-content
description: Get the resource that is accessed through this view.
old-location: direct3d11\id3d11view_getresource.htm
tech.root: direct3d11
ms.assetid: f6f6c4db-80c0-49bc-bd15-53e3a52d9f3c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 9a136bd2-66f9-8800-9ce0-d8b9c402d899, GetResource, GetResource method [Direct3D 11], GetResource method [Direct3D 11],ID3D11View interface, ID3D11View interface [Direct3D 11],GetResource method, ID3D11View.GetResource, ID3D11View::GetResource, d3d11/ID3D11View::GetResource, direct3d11.id3d11view_getresource
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
 - ID3D11View.GetResource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11View::GetResource


## -description


Get the resource that is accessed through this view.


## -parameters




### -param ppResource [out]

Type: <b><a href="https://msdn.microsoft.com/3823ec00-cb3c-43ce-9f1a-be4e1e99d587">ID3D11Resource</a>**</b>

Address of a pointer to the resource that is accessed through this view. (See <a href="https://msdn.microsoft.com/3823ec00-cb3c-43ce-9f1a-be4e1e99d587">ID3D11Resource</a>.)


## -returns



Returns nothing.




## -remarks



This function increments the reference count of the resource by one, so it is necessary to call <b>Release</b> on the returned pointer when the application is done with it. Destroying (or losing) the returned pointer before <b>Release</b> is called will result in a memory leak.




## -see-also




<a href="https://msdn.microsoft.com/060973b4-bf7d-4be2-b087-85a5b1bca905">ID3D11View</a>
 

 

