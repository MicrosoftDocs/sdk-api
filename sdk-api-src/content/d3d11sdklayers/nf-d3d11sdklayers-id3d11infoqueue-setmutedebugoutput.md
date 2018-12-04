---
UID: NF:d3d11sdklayers.ID3D11InfoQueue.SetMuteDebugOutput
title: ID3D11InfoQueue::SetMuteDebugOutput
author: windows-sdk-content
description: Set a boolean that turns the debug output on or off.
old-location: direct3d11\id3d11infoqueue_setmutedebugoutput.htm
tech.root: direct3d11
ms.assetid: 0b155d2c-f7b0-4879-8086-8cccbca16a25
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: 845ced1c-0b30-f73c-38de-69cd6425f139, ID3D11InfoQueue interface [Direct3D 11],SetMuteDebugOutput method, ID3D11InfoQueue.SetMuteDebugOutput, ID3D11InfoQueue::SetMuteDebugOutput, SetMuteDebugOutput, SetMuteDebugOutput method [Direct3D 11], SetMuteDebugOutput method [Direct3D 11],ID3D11InfoQueue interface, d3d11sdklayers/ID3D11InfoQueue::SetMuteDebugOutput, direct3d11.id3d11infoqueue_setmutedebugoutput
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d11sdklayers.h
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
 - ID3D11InfoQueue.SetMuteDebugOutput
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11InfoQueue::SetMuteDebugOutput


## -description


Set a boolean that turns the debug output on or off.


## -parameters




### -param bMute [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Disable/Enable the debug output (<b>TRUE</b> to disable or mute the output, <b>FALSE</b> to enable the output).


## -returns



Returns nothing.




## -remarks



This will stop messages that pass the storage filter from being printed out in the debug output, however those messages will still be added to the message queue.




## -see-also




<a href="https://msdn.microsoft.com/240820c7-1c1f-4e2d-8b3e-497fd931d7d2">ID3D11InfoQueue Interface</a>
 

 

