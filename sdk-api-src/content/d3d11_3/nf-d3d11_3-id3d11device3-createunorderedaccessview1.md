---
UID: NF:d3d11_3.ID3D11Device3.CreateUnorderedAccessView1
title: ID3D11Device3::CreateUnorderedAccessView1
author: windows-sdk-content
description: Creates a view for accessing an unordered access resource.
old-location: direct3d11\id3d11device3_createunorderedaccessview1.htm
old-project: direct3d11
ms.assetid: AB64DDED-4C2D-4952-BAA5-3139F973C962
ms.author: windowssdkdev
ms.date: 04/06/2018
ms.keywords: CreateUnorderedAccessView1, CreateUnorderedAccessView1 method [Direct3D 11], CreateUnorderedAccessView1 method [Direct3D 11],ID3D11Device3 interface, ID3D11Device3 interface [Direct3D 11],CreateUnorderedAccessView1 method, ID3D11Device3.CreateUnorderedAccessView1, ID3D11Device3::CreateUnorderedAccessView1, d3d11_3/ID3D11Device3::CreateUnorderedAccessView1, direct3d11.id3d11device3_createunorderedaccessview1
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d11_3.h
req.include-header: 
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



          Creates a view for accessing an <a href="https://msdn.microsoft.com/597cc12f-dd0e-4603-b670-3f584f25e192">unordered access</a> resource.
        


## -parameters




### -param pResource [in]

Type: <b><a href="https://msdn.microsoft.com/3823ec00-cb3c-43ce-9f1a-be4e1e99d587">ID3D11Resource</a>*</b>


            Pointer to an <a href="https://msdn.microsoft.com/3823ec00-cb3c-43ce-9f1a-be4e1e99d587">ID3D11Resource</a> that represents a resources that will serve as an input to a shader.
          


### -param pDesc1 [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/833B4B8A-5702-4C17-AFD2-DFDF69354DDD">D3D11_UNORDERED_ACCESS_VIEW_DESC1</a>*</b>


            Pointer to a <a href="https://msdn.microsoft.com/833B4B8A-5702-4C17-AFD2-DFDF69354DDD">D3D11_UNORDERED_ACCESS_VIEW_DESC1</a> structure that represents an unordered-access view description. Set this parameter to <b>NULL</b> to create a view that accesses the entire resource (using the format the resource was created with).
          


### -param ppUAView1 [out, optional]

Type: <b><a href="https://msdn.microsoft.com/0D4F7634-0AB1-41C2-8D4F-8C42C1D973D2">ID3D11UnorderedAccessView1</a>**</b>


            A pointer to a memory block that receives a pointer to a <a href="https://msdn.microsoft.com/0D4F7634-0AB1-41C2-8D4F-8C42C1D973D2">ID3D11UnorderedAccessView1</a> interface for the created unordered-access view. Set this parameter to <b>NULL</b> to validate the other input parameters (the method will return <b>S_FALSE</b> if the other input parameters pass validation).
          


## -returns



Type: <b><a href="https://msdn.microsoft.com/library/windows/desktop/455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>


              This method returns E_OUTOFMEMORY if there is insufficient memory to create the unordered-access view.  See <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a> for other possible return values.
            




## -see-also




<a href="https://msdn.microsoft.com/0AA10851-0077-4075-BD41-72FCD7BC0556">ID3D11Device3</a>
 

 

