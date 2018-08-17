---
UID: NF:d3d11_3.ID3D11Device3.CreateUnorderedAccessView1
title: ID3D11Device3::CreateUnorderedAccessView1
author: windows-sdk-content
description: Creates a view for accessing an unordered access resource.
old-location: direct3d11\id3d11device3_createunorderedaccessview1.htm
old-project: direct3d11
ms.assetid: AB64DDED-4C2D-4952-BAA5-3139F973C962
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CreateUnorderedAccessView1, CreateUnorderedAccessView1 method [Direct3D 11], CreateUnorderedAccessView1 method [Direct3D 11],ID3D11Device3 interface, ID3D11Device3 interface [Direct3D 11],CreateUnorderedAccessView1 method, ID3D11Device3.CreateUnorderedAccessView1, ID3D11Device3::CreateUnorderedAccessView1, d3d11_3/ID3D11Device3::CreateUnorderedAccessView1, direct3d11.id3d11device3_createunorderedaccessview1
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d11_3.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.typenames: D3D11_TEXTURE_LAYOUT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11Device3.CreateUnorderedAccessView1
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11Device3::CreateUnorderedAccessView1


## -description


Creates a view for accessing an <a href="https://msdn.microsoft.com/en-us/library/Ff476335(v=VS.85).aspx">unordered access</a> resource.
        


## -parameters




### -param pResource [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ff476584(v=VS.85).aspx">ID3D11Resource</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/Ff476584(v=VS.85).aspx">ID3D11Resource</a> that represents a resources that will serve as an input to a shader.
          


### -param pDesc1 [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/Dn899203(v=VS.85).aspx">D3D11_UNORDERED_ACCESS_VIEW_DESC1</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/Dn899203(v=VS.85).aspx">D3D11_UNORDERED_ACCESS_VIEW_DESC1</a> structure that represents an unordered-access view description. Set this parameter to <b>NULL</b> to create a view that accesses the entire resource (using the format the resource was created with).
          


### -param ppUAView1 [out, optional]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dn899248(v=VS.85).aspx">ID3D11UnorderedAccessView1</a>**</b>

A pointer to a memory block that receives a pointer to a <a href="https://msdn.microsoft.com/en-us/library/Dn899248(v=VS.85).aspx">ID3D11UnorderedAccessView1</a> interface for the created unordered-access view. Set this parameter to <b>NULL</b> to validate the other input parameters (the method will return <b>S_FALSE</b> if the other input parameters pass validation).
          


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns E_OUTOFMEMORY if there is insufficient memory to create the unordered-access view.  See <a href="https://msdn.microsoft.com/en-us/library/Ff476174(v=VS.85).aspx">Direct3D 11 Return Codes</a> for other possible return values.
            




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn899218(v=VS.85).aspx">ID3D11Device3</a>
 

 

