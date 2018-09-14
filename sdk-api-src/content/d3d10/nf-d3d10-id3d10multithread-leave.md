---
UID: NF:d3d10.ID3D10Multithread.Leave
title: ID3D10Multithread::Leave
author: windows-sdk-content
description: Leave a device's critical section.
old-location: direct3d10\id3d10multithread_leave.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10multithread_leave.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: ID3D10Multithread interface [Direct3D 10],Leave method, ID3D10Multithread.Leave, ID3D10Multithread::Leave, Leave, Leave method [Direct3D 10], Leave method [Direct3D 10],ID3D10Multithread interface, d3d10/ID3D10Multithread::Leave, direct3d10.id3d10multithread_leave, f69302dd-2d93-2366-c5f5-206d6140c16e
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d10.h
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
req.lib: D3D10.lib
req.dll: 
req.irql: 
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
req.typenames: 
req.redist: 
---

# ID3D10Multithread::Leave


## -description


Leave a device's critical section.


## -parameters






## -returns



Returns nothing.




## -remarks



This function is typically used in multithreaded applications when there is a series of graphics commands that must happen in order. <a href="https://msdn.microsoft.com/en-us/library/Bb173817(v=VS.85).aspx">ID3D10Multithread::Enter</a> is typically called at the beginning of a series of graphics commands, and this function is typically called after those graphics commands.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173528(v=VS.85).aspx">ID3D10Device Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb173816(v=VS.85).aspx">ID3D10Multithread</a>
 

 

