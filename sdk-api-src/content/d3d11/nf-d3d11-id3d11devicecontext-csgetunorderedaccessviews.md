---
UID: NF:d3d11.ID3D11DeviceContext.CSGetUnorderedAccessViews
title: ID3D11DeviceContext::CSGetUnorderedAccessViews
author: windows-sdk-content
description: Gets an array of views for an unordered resource.
old-location: direct3d11\id3d11devicecontext_csgetunorderedaccessviews.htm
tech.root: direct3d11
ms.assetid: ae572062-0034-48c2-a3ce-abe40b50248b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CSGetUnorderedAccessViews, CSGetUnorderedAccessViews method [Direct3D 11], CSGetUnorderedAccessViews method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],CSGetUnorderedAccessViews method, ID3D11DeviceContext.CSGetUnorderedAccessViews, ID3D11DeviceContext::CSGetUnorderedAccessViews, afdfe129-87c0-6deb-9357-e78983622e7d, d3d11/ID3D11DeviceContext::CSGetUnorderedAccessViews, direct3d11.id3d11devicecontext_csgetunorderedaccessviews
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
 - ID3D11DeviceContext.CSGetUnorderedAccessViews
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11DeviceContext::CSGetUnorderedAccessViews


## -description


Gets an array of views for an unordered resource.


## -parameters




### -param StartSlot [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Index of the first element in the zero-based array to return (ranges from 0 to D3D11_1_UAV_SLOT_COUNT - 1).


### -param NumUAVs [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of views to get (ranges from 0 to D3D11_1_UAV_SLOT_COUNT - StartSlot).


### -param ppUnorderedAccessViews [out, optional]

Type: <b><a href="https://msdn.microsoft.com/9def4a7d-f145-4073-8d7d-bf3c7ac7a060">ID3D11UnorderedAccessView</a>**</b>

A pointer to an array of interface pointers (see <a href="https://msdn.microsoft.com/9def4a7d-f145-4073-8d7d-bf3c7ac7a060">ID3D11UnorderedAccessView</a>) to get.


## -returns



Returns nothing.




## -remarks



Any returned interfaces will have their reference count incremented by one. Applications should call <b>IUnknown::Release</b> on the returned interfaces when they are no longer needed to avoid memory leaks.




## -see-also




<a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>
 

 

