---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# D3D12_FEATURE_DATA_D3D12_OPTIONS2 structure


## -description


Details the adapter's support for certain optional features of Direct3D 12.


## -struct-fields




### -field DepthBoundsTestSupported

<a href="https://msdn.microsoft.com/en-us/library/jj159528.aspx">SAL</a>: <code>_Out_</code>

On return, contains true if depth-bounds tests are supported; otherwise, false.


### -field ProgrammableSamplePositionsTier

<a href="https://msdn.microsoft.com/en-us/library/jj159528.aspx">SAL</a>: <code>_Out_</code>

On return, contains a value that indicates the level of support offered for programmable sample positions.


## -remarks



Use this structure with <a href="https://msdn.microsoft.com/2E986E37-30C7-45FE-BC8B-A6DD5670938F">CheckFeatureSupport</a> to determine the level of support offered for the optional Depth-bounds test and programmable sample positions features.

See the enumeration constant D3D12_FEATURE_D3D12_OPTIONS2 in the <a href="https://msdn.microsoft.com/165ECFE0-1B18-4A26-8B9C-3CE53776A349">D3D12_FEATURE</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

