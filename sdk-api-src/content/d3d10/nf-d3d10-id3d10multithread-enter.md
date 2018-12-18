---
UID: NF:d3d10.ID3D10Multithread.Enter
title: ID3D10Multithread::Enter
author: windows-sdk-content
description: Enter a device's critical section.
old-location: direct3d10\id3d10multithread_enter.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10multithread_enter.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Enter, Enter method [Direct3D 10], Enter method [Direct3D 10],ID3D10Multithread interface, ID3D10Multithread interface [Direct3D 10],Enter method, ID3D10Multithread.Enter, ID3D10Multithread::Enter, d34de96c-b476-19e4-cf57-4e43604474ab, d3d10/ID3D10Multithread::Enter, direct3d10.id3d10multithread_enter
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
 - ID3D10Multithread.Enter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10Multithread::Enter


## -description


Enter a device's critical section.


## -parameters






## -returns



Returns nothing.




## -remarks



Entering a device's critical section prevents other threads from simultaneously calling that device's methods (if <a href="https://msdn.microsoft.com/en-us/library/Bb173820(v=VS.85).aspx">multithread protection</a> is set to true), calling DXGI methods, and calling the methods of all resource, view, shader, state, and asynchronous interfaces.

This function should be used in multithreaded applications when there is a series of graphics commands that must happen in order. This function is typically called at the beginning of the series of graphics commands, and <a href="https://msdn.microsoft.com/en-us/library/Bb173819(v=VS.85).aspx">ID3D10Multithread::Leave</a> is typically called after those graphics commands.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173528(v=VS.85).aspx">ID3D10Device Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb173816(v=VS.85).aspx">ID3D10Multithread</a>
 

 

