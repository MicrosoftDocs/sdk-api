---
UID: NF:d3d12.ID3D12Device.SetStablePowerState
title: ID3D12Device::SetStablePowerState
author: windows-sdk-content
description: A development-time aid for certain types of profiling and experimental prototyping.
old-location: direct3d12\id3d12device_setstablepowerstate.htm
tech.root: direct3d12
ms.assetid: 6078DAEF-DD8B-4F1F-86C8-96CE7BD691E4
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: ID3D12Device interface,SetStablePowerState method, ID3D12Device.SetStablePowerState, ID3D12Device::SetStablePowerState, SetStablePowerState, SetStablePowerState method, SetStablePowerState method,ID3D12Device interface, d3d12/ID3D12Device::SetStablePowerState, direct3d12.id3d12device_setstablepowerstate
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
 - ID3D12Device.SetStablePowerState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12Device::SetStablePowerState


## -description


A development-time aid for certain types of profiling and experimental prototyping.


## -parameters




### -param Enable

Type: <b>BOOL</b>

Specifies a BOOL that turns the stable power state on or off.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the <a href="https://msdn.microsoft.com/5F6CC962-7DB7-489F-82A4-9388313014D3">Direct3D 12 Return Codes</a>.




## -remarks



This method is only useful during the development of applications. It enables developers to profile GPU usage of multiple algorithms without experiencing artifacts from <a href="https://en.wikipedia.org/wiki/Dynamic_frequency_scaling">dynamic frequency scaling</a>.

Do not call this method in normal execution for a shipped application. This method only works while the machine is in <a href="https://msdn.microsoft.com/en-us/windows/uwp/get-started/enable-your-device-for-development">developer mode</a>. If developer mode is not enabled, then device removal will occur. Instead, call this method in response to an off-by-default, developer-facing switch. Calling it in response to command line parameters, config files, registry keys, and developer console commands are reasonable usage scenarios. 

A stable power state typically fixes GPU clock rates at a slower setting that is significantly lower than that experienced by users under normal application load. This reduction in clock rate affects the entire system. Slow clock rates are required to ensure processors don’t exhaust power, current, and thermal limits. Normal usage scenarios commonly leverage a processors ability to dynamically over-clock. Any conclusions made by comparing two designs under a stable power state should be double-checked with supporting results from real usage scenarios.




## -see-also




<a href="https://msdn.microsoft.com/D32B3397-A1E0-48AF-9251-2EDA96261A9F">ID3D12Device</a>
 

 

