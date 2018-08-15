---
UID: NF:d3d10.ID3D10Multithread.Leave
title: ID3D10Multithread::Leave
author: windows-sdk-content
description: Leave a device's critical section.
old-location: direct3d10\id3d10multithread_leave.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10multithread_leave.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ID3D10Multithread interface [Direct3D 10],Leave method, ID3D10Multithread.Leave, ID3D10Multithread::Leave, Leave, Leave method [Direct3D 10], Leave method [Direct3D 10],ID3D10Multithread interface, d3d10/ID3D10Multithread::Leave, direct3d10.id3d10multithread_leave, f69302dd-2d93-2366-c5f5-206d6140c16e
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d10.h
req.include-header: 
req.redist: 
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
req.typenames: D3D10_USAGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Multithread.Leave
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10Multithread::Leave


## -description


Leave a device's critical section.


## -parameters






## -returns



Returns nothing.




## -remarks



This function is typically used in multithreaded applications when there is a series of graphics commands that must happen in order. <a href="https://msdn.microsoft.com/16617f82-f19c-4ec6-93ae-9f0ec4501a49">ID3D10Multithread::Enter</a> is typically called at the beginning of a series of graphics commands, and this function is typically called after those graphics commands.




## -see-also




<a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device Interface</a>



<a href="https://msdn.microsoft.com/ff4890fe-25a3-4515-b20d-45f68637e7b3">ID3D10Multithread</a>
 

 

