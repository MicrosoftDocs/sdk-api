---
UID: NF:d3d12.ID3D12Fence1.GetCreationFlags
title: ID3D12Fence1::GetCreationFlags
author: windows-sdk-content
description: Gets the flags used to create the fence represented by the current instance.
old-location: direct3d12\id3d12fence1_getcreationflags.htm
tech.root: direct3d12
ms.assetid: 59FF0D7D-CE1F-49AD-8AFE-8C0E7DE05F36
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: GetCreationFlags, GetCreationFlags method, GetCreationFlags method,ID3D12fence1 interface, ID3D12Fence1.GetCreationFlags, ID3D12Fence1::GetCreationFlags, ID3D12fence1 interface,GetCreationFlags method, ID3D12fence1::GetCreationFlags, d3d12/ID3D12fence1::GetCreationFlags, direct3d12.id3d12fence1_getcreationflags
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D12.dll
api_name:
 - ID3D12fence1.GetCreationFlags
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12Fence1::GetCreationFlags


## -description


Gets the flags used to create the fence represented by the current instance.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/EF725566-B77A-40EE-B5E3-86C5D13CC7D5">D3D12_FENCE_FLAGS</a></b>

The flags used to create the fence.




## -remarks



The flags returned by <b>GetCreationFlags</b> are used mainly for opening a shared fence.




## -see-also




<a href="https://msdn.microsoft.com/292FA25B-7C72-4092-8822-DB15951A8309">Id3d12fence1</a>



<a href="https://msdn.microsoft.com/93903F50-A6CA-41C2-863D-68D645586B4C">Synchronization and Multi-Engine</a>
 

 

