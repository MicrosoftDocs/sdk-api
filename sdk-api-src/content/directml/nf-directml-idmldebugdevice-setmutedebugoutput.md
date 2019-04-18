---
UID: NF:directml.IDMLDebugDevice.SetMuteDebugOutput
title: IDMLDebugDevice::SetMuteDebugOutput
author: windows-sdk-content
description: Determine whether to mute DirectML from sending messages to the ID3D12InfoQueue.
old-location: direct3d12\idmldebugdevice_setmutedebugoutput.htm
tech.root: direct3d12
ms.assetid: 74BA5FE6-1197-4BF0-A5FE-FAFE650C4C8E
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDMLDebugDevice interface,SetMuteDebugOutput method, IDMLDebugDevice.SetMuteDebugOutput, IDMLDebugDevice::SetMuteDebugOutput, SetMuteDebugOutput, SetMuteDebugOutput method, SetMuteDebugOutput method,IDMLDebugDevice interface, direct3d12.idmldebugdevice_setmutedebugoutput, directml/IDMLDebugDevice::SetMuteDebugOutput
ms.topic: method
req.header: directml.h
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
req.lib: DirectML.lib
req.dll: DirectML.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectML.dll
api_name:
 - IDMLDebugDevice.SetMuteDebugOutput
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDMLDebugDevice::SetMuteDebugOutput


## -description






Determine whether to mute DirectML from sending messages to the <a href="https://msdn.microsoft.com/61667AAC-05AC-4745-8992-E9377641D411">ID3D12InfoQueue</a>.


## -parameters




### -param mute

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

If <b>TRUE</b>,  DirectML is muted, and it will not send messages to the <a href="https://msdn.microsoft.com/61667AAC-05AC-4745-8992-E9377641D411">ID3D12InfoQueue</a>. If <b>FALSE</b>,  DirectML is not muted, and it will send messages to the <b>ID3D12InfoQueue</b>.


## -returns



This method does not return a value.




## -see-also




[IDMLDebugDevice](/windows/desktop/api/directml/nn-directml-idmldebugdevice)
 

 

