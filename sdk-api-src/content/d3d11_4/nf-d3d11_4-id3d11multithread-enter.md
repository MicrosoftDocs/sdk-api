---
UID: NF:d3d11_4.ID3D11Multithread.Enter
title: ID3D11Multithread::Enter
author: windows-sdk-content
description: Enter a device's critical section.
old-location: direct3d11\id3d11multithread_enter.htm
tech.root: direct3d11
ms.assetid: A742D03A-0A47-4B08-952A-836A272D1519
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: Enter, Enter method [Direct3D 11], Enter method [Direct3D 11],ID3D11Multithread interface, ID3D11Multithread interface [Direct3D 11],Enter method, ID3D11Multithread.Enter, ID3D11Multithread::Enter, d3d11_4/ID3D11Multithread::Enter, direct3d11.id3d11multithread_enter
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d11_4.h
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
req.lib: D3d11_4.lib
req.dll: D3d11_4.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11_4.dll
api_name:
 - ID3D11Multithread.Enter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11Multithread::Enter


## -description


Enter a device's critical section.


## -parameters






## -returns



This method does not return a value.




## -remarks



If <a href="https://msdn.microsoft.com/E8BF9A25-CCEA-44F3-AE7C-376E5B672079">SetMultithreadProtected</a> is set to true, then entering a device's critical section prevents other threads from simultaneously calling that device's methods, calling DXGI methods, and calling the methods of all resource, view, shader, state, and asynchronous interfaces.

This function should be used in multithreaded applications when there is a series of graphics commands that must happen in order. This function is typically called at the beginning of the series of graphics commands, and <a href="https://msdn.microsoft.com/CECBE440-3F9E-4649-B257-BAD3E7F5CF2F">Leave</a> is typically called after those graphics commands.




## -see-also




<a href="https://msdn.microsoft.com/1A07694E-7D61-4A59-82E3-048F04C8D57A">ID3D11Multithread</a>
 

 

