---
UID: NF:d3d12.ID3D12Object.SetName
title: ID3D12Object::SetName
author: windows-sdk-content
description: Associates a name with the device object. This name is for use in debug diagnostics and tools.
old-location: direct3d12\id3d12object_setname.htm
old-project: direct3d12
ms.assetid: A1DEEB16-BF75-4391-ADF0-AC22EECBC71A
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: ID3D12Object interface,SetName method, ID3D12Object.SetName, ID3D12Object::SetName, SetName, SetName method, SetName method,ID3D12Object interface, d3d12/ID3D12Object::SetName, direct3d12.id3d12object_setname
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d12.h
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
tech.root: 
req.typenames: D3D_SHADER_MODEL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D12.dll
api_name:
 - ID3D12Object.SetName
product: Windows
targetos: Windows
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
---

# ID3D12Object::SetName


## -description


Associates a name with the device object.
          This name is for use in debug diagnostics and tools.
        


## -parameters




### -param Name [in]

Type: <b>LPCWSTR</b>

A <b>NULL</b>-terminated <b>UNICODE</b> string that contains the name to associate with the device object.
          


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the <a href="https://msdn.microsoft.com/5F6CC962-7DB7-489F-82A4-9388313014D3">Direct3D 12 Return Codes</a>.
          




## -remarks



This method takes UNICODE names.
        The older Direct3D 11 debug object naming system through
        <a href="https://msdn.microsoft.com/1B3E8202-7CB3-4D9F-A1AE-70E66652773C">ID3D12Object::SetPrivateData</a>with <b>WKPDID_D3DDebugObjectName</b> used ASCII.
       




## -see-also




<a href="https://msdn.microsoft.com/B2288866-E95F-46B8-A7A1-19888F029C03">Direct3D 12 Programming Environment Setup</a>



<a href="https://msdn.microsoft.com/D2B2BC74-E89D-4D3A-8808-6E4A94992769">ID3D12Object</a>
 

 

