---
UID: NF:d3d11_3.ID3D11Device3.CreateQuery1
title: ID3D11Device3::CreateQuery1
author: windows-sdk-content
description: Creates a query object for querying information from the graphics processing unit (GPU).
old-location: direct3d11\id3d11device3_createquery1.htm
tech.root: direct3d11
ms.assetid: 8D170F97-DA95-48FE-84F6-2BBB3E388BB4
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CreateQuery1, CreateQuery1 method [Direct3D 11], CreateQuery1 method [Direct3D 11],ID3D11Device3 interface, ID3D11Device3 interface [Direct3D 11],CreateQuery1 method, ID3D11Device3.CreateQuery1, ID3D11Device3::CreateQuery1, d3d11_3/ID3D11Device3::CreateQuery1, direct3d11.id3d11device3_createquery1
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ID3D11Device3.CreateQuery1
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11Device3::CreateQuery1


## -description


Creates a query object for querying information from the graphics processing unit (GPU). 


## -parameters




### -param pQueryDesc1 [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/Dn899156(v=VS.85).aspx">D3D11_QUERY_DESC1</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/Dn899156(v=VS.85).aspx">D3D11_QUERY_DESC1</a> structure that represents a query description.


### -param ppQuery1 [out, optional]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dn899236(v=VS.85).aspx">ID3D11Query1</a>**</b>

A pointer to a memory block that receives a pointer to a <a href="https://msdn.microsoft.com/en-us/library/Dn899236(v=VS.85).aspx">ID3D11Query1</a> interface for the created query object. Set this parameter to <b>NULL</b> to validate the other input parameters (the method will return <b>S_FALSE</b> if the other input parameters pass validation).


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns E_OUTOFMEMORY if there is insufficient memory to create the query object.  
        See <a href="https://msdn.microsoft.com/en-us/library/Ff476174(v=VS.85).aspx">Direct3D 11 Return Codes</a> for other possible return values.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn899218(v=VS.85).aspx">ID3D11Device3</a>
 

 

