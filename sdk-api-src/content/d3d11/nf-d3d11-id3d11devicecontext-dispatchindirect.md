---
UID: NF:d3d11.ID3D11DeviceContext.DispatchIndirect
title: ID3D11DeviceContext::DispatchIndirect
author: windows-sdk-content
description: Execute a command list over one or more thread groups.
old-location: direct3d11\id3d11devicecontext_dispatchindirect.htm
tech.root: direct3d11
ms.assetid: bb8840f5-ae4b-42d6-b51d-6844d0b18074
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: 4aaa5960-b4f6-bccf-2256-435d0fef6be6, DispatchIndirect, DispatchIndirect method [Direct3D 11], DispatchIndirect method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],DispatchIndirect method, ID3D11DeviceContext.DispatchIndirect, ID3D11DeviceContext::DispatchIndirect, d3d11/ID3D11DeviceContext::DispatchIndirect, direct3d11.id3d11devicecontext_dispatchindirect
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
 - ID3D11DeviceContext.DispatchIndirect
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
- ID3D11DeviceContext.DispatchIndirect
: 
---

# ID3D11DeviceContext::DispatchIndirect


## -description


Execute a command list over one or more thread groups.


## -parameters




### -param pBufferForArgs [in]

Type: <b><a href="https://msdn.microsoft.com/7224de57-75cb-4d68-9d70-f5dd2f92b1fd">ID3D11Buffer</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/7224de57-75cb-4d68-9d70-f5dd2f92b1fd">ID3D11Buffer</a>, which must be loaded with data that matches the argument list for <a href="https://msdn.microsoft.com/7d3401bb-521f-4ab0-8833-e5caf712d0c9">ID3D11DeviceContext::Dispatch</a>.


### -param AlignedByteOffsetForArgs [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A byte-aligned offset between the start of the buffer and the arguments.


## -returns



Returns nothing.




## -remarks



You call the <b>DispatchIndirect</b> method to execute commands in a <a href="https://msdn.microsoft.com/02c1f98e-fdd6-49b0-b8b2-efbd472ab599">compute shader</a>.

When an application creates a buffer that is associated with the <a href="https://msdn.microsoft.com/7224de57-75cb-4d68-9d70-f5dd2f92b1fd">ID3D11Buffer</a> interface that  <i>pBufferForArgs</i> points to, the application must set the <a href="https://msdn.microsoft.com/en-us/library/Ff476203(v=VS.85).aspx">D3D11_RESOURCE_MISC_DRAWINDIRECT_ARGS</a> flag in the <b>MiscFlags</b> member of the <a href="https://msdn.microsoft.com/en-us/library/Ff476092(v=VS.85).aspx">D3D11_BUFFER_DESC</a> structure that describes the buffer. To create the buffer, the application calls the <a href="https://msdn.microsoft.com/en-us/library/Ff476501(v=VS.85).aspx">ID3D11Device::CreateBuffer</a> method and in this call passes a pointer to <b>D3D11_BUFFER_DESC</b> in the <i>pDesc</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476385(v=VS.85).aspx">ID3D11DeviceContext</a>
 

 

