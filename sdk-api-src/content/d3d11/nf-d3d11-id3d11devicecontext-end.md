---
UID: NF:d3d11.ID3D11DeviceContext.End
title: ID3D11DeviceContext::End
author: windows-sdk-content
description: Mark the end of a series of commands.
old-location: direct3d11\id3d11devicecontext_end.htm
tech.root: direct3d11
ms.assetid: 9b941abc-04a3-4dd7-b72d-62cd5bd06b47
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: End, End method [Direct3D 11], End method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],End method, ID3D11DeviceContext.End, ID3D11DeviceContext::End, c700f203-34b8-01ee-d941-99cff256b5c2, d3d11/ID3D11DeviceContext::End, direct3d11.id3d11devicecontext_end
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
 - ID3D11DeviceContext.End
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
- ID3D11DeviceContext.End
: 
---

# ID3D11DeviceContext::End


## -description


Mark the end of a series of commands.


## -parameters




### -param pAsync [in]

Type: <b><a href="https://msdn.microsoft.com/37ff9dc0-5ec2-4cd5-b252-44e2dac45355">ID3D11Asynchronous</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/37ff9dc0-5ec2-4cd5-b252-44e2dac45355">ID3D11Asynchronous</a> interface.


## -returns



Returns nothing.




## -remarks



Use <a href="https://msdn.microsoft.com/5a9cdc60-2226-4d18-bfbd-5db10de35e53">ID3D11DeviceContext::Begin</a> to mark the beginning of the series of commands.




## -see-also




<a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>
 

 

