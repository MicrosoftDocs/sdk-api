---
UID: NF:d3d10sdklayers.ID3D10InfoQueue.SetMuteDebugOutput
title: ID3D10InfoQueue::SetMuteDebugOutput method
author: windows-driver-content
description: Set a boolean that turns the debug output on or off.
old-location: direct3d10\id3d10infoqueue_setmutedebugoutput.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10infoqueue_setmutedebugoutput.htm
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: ID3D10InfoQueue, ID3D10InfoQueue interface [Direct3D 10], SetMuteDebugOutput method, ID3D10InfoQueue::SetMuteDebugOutput, SetMuteDebugOutput method [Direct3D 10], SetMuteDebugOutput method [Direct3D 10], ID3D10InfoQueue interface, SetMuteDebugOutput,ID3D10InfoQueue.SetMuteDebugOutput, d3d10sdklayers/ID3D10InfoQueue::SetMuteDebugOutput, direct3d10.id3d10infoqueue_setmutedebugoutput, fc4951da-744c-9cda-d7ab-407692014dd0
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d10sdklayers.h
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
req.typenames: D3D10_MESSAGE_SEVERITY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D10SDKLayers.h
api_name:
-	ID3D10InfoQueue.SetMuteDebugOutput
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10InfoQueue::SetMuteDebugOutput method


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




<a href="https://msdn.microsoft.com/b1405273-53f4-49da-acf5-832e73a25ac2">ID3D10InfoQueue Interface</a>
 

 

