---
UID: NF:d3d11.ID3D11CommandList.GetContextFlags
title: ID3D11CommandList::GetContextFlags
author: windows-sdk-content
description: Gets the initialization flags associated with the deferred context that created the command list.
old-location: direct3d11\id3d11commandlist_getcontextflags.htm
tech.root: direct3d11
ms.assetid: a3d98f3f-6e66-408e-baee-661afb65c0a4
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: 64bf9914-05c2-c831-c3c4-d1181d8ca907, GetContextFlags, GetContextFlags method [Direct3D 11], GetContextFlags method [Direct3D 11],ID3D11CommandList interface, ID3D11CommandList interface [Direct3D 11],GetContextFlags method, ID3D11CommandList.GetContextFlags, ID3D11CommandList::GetContextFlags, d3d11/ID3D11CommandList::GetContextFlags, direct3d11.id3d11commandlist_getcontextflags
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
req.lib: D3d11.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11.lib
 - d3d11.dll
api_name:
 - ID3D11CommandList.GetContextFlags
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11CommandList::GetContextFlags


## -description


Gets the initialization flags associated with the deferred context that created the command list.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The context flag is reserved for future use and is always 0.




## -remarks



The GetContextFlags method gets the flags that were supplied to the <i>ContextFlags</i> parameter of <a href="https://msdn.microsoft.com/fbf01844-eaf1-4360-833e-c95ba686fff5">ID3D11Device::CreateDeferredContext</a>; however, the context flag is reserved for future use.




## -see-also




<a href="https://msdn.microsoft.com/432f1d21-bf13-4569-9c8f-04f5d2845150">ID3D11CommandList</a>
 

 

