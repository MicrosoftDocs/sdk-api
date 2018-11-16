---
UID: NF:d3d12sdklayers.ID3D12InfoQueue.SetMuteDebugOutput
title: ID3D12InfoQueue::SetMuteDebugOutput
author: windows-sdk-content
description: Set a boolean that turns the debug output on or off.
old-location: direct3d12\id3d12infoqueue_setmutedebugoutput.htm
tech.root: direct3d12
ms.assetid: 470155C2-095B-44EF-8ED3-18E1B2DADE4B
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ID3D12InfoQueue interface,SetMuteDebugOutput method, ID3D12InfoQueue.SetMuteDebugOutput, ID3D12InfoQueue::SetMuteDebugOutput, SetMuteDebugOutput, SetMuteDebugOutput method, SetMuteDebugOutput method,ID3D12InfoQueue interface, d3d12sdklayers/ID3D12InfoQueue::SetMuteDebugOutput, direct3d12.id3d12infoqueue_setmutedebugoutput
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d12sdklayers.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12sdklayers.h
api_name:
 - ID3D12InfoQueue.SetMuteDebugOutput
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d12sdklayers.h
: 
- ID3D12InfoQueue.SetMuteDebugOutput
: 
---

# ID3D12InfoQueue::SetMuteDebugOutput


## -description


Set a boolean that turns the debug output on or off.




## -parameters




### -param bMute [in]

Type: <b>BOOL</b>

Disable/Enable the debug output (true to disable or mute the output, false to enable the output).


          


## -returns



This method does not return a value.
          




## -remarks



This will stop messages that pass the storage filter from being printed out in the debug output, however those messages will still be added to the message queue.






## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn950163(v=VS.85).aspx">ID3D12InfoQueue</a>
 

 

