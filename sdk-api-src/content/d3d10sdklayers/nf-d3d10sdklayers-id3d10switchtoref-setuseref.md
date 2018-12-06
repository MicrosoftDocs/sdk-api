---
UID: NF:d3d10sdklayers.ID3D10SwitchToRef.SetUseRef
title: ID3D10SwitchToRef::SetUseRef
author: windows-sdk-content
description: Switch between a hardware and a software device.
old-location: direct3d10\id3d10switchtoref_setuseref.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10switchtoref_setuseref.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 7960e1b8-7255-59bd-3f8f-533b12811a49, ID3D10SwitchToRef interface [Direct3D 10],SetUseRef method, ID3D10SwitchToRef.SetUseRef, ID3D10SwitchToRef::SetUseRef, SetUseRef, SetUseRef method [Direct3D 10], SetUseRef method [Direct3D 10],ID3D10SwitchToRef interface, d3d10sdklayers/ID3D10SwitchToRef::SetUseRef, direct3d10.id3d10switchtoref_setuseref
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10SDKLayers.h
api_name:
 - ID3D10SwitchToRef.SetUseRef
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10SwitchToRef::SetUseRef


## -description


Switch between a hardware and a software device.


## -parameters




### -param UseRef [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

A boolean value. Set this to <b>TRUE</b> to change to a software device, set this to <b>FALSE</b> to change to a hardware device.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

The previous value of <i>UseRef</i>.




## -remarks



This API will fail if the device is not switchable; you must have created a device that is switchable by specifying the D3D10_CREATE_DEVICE_SWITCH_TO_REF flag during device creation (when calling <a href="https://msdn.microsoft.com/da48d6d4-f35b-4cd1-a358-8eec63dfa674">D3D10CreateDevice</a>).

Switching from a software device to a hardware device clears all cached objects from system memory. Switching from a hardware device to a software device causes resources to be downloaded to system memory.




## -see-also




<a href="https://msdn.microsoft.com/da48d6d4-f35b-4cd1-a358-8eec63dfa674">D3D10CreateDevice</a>



<a href="https://msdn.microsoft.com/c9865391-a75e-4bbe-907a-740ed5b3b29f">ID3D10SwitchToRef Interface</a>
 

 

