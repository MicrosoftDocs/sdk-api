---
UID: NE:d3d10_1.D3D10_FEATURE_LEVEL1
title: D3D10_FEATURE_LEVEL1
author: windows-sdk-content
description: The version of hardware acceleration requested.
old-location: direct3d10\d3d10_feature_level1.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_feature_level1.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 31af56cc-826c-6632-ae68-1b2e713c38ad, D3D10_FEATURE_LEVEL1, D3D10_FEATURE_LEVEL1 enumeration [Direct3D 10], D3D10_FEATURE_LEVEL_10_0, D3D10_FEATURE_LEVEL_10_1, D3D10_FEATURE_LEVEL_9_1, D3D10_FEATURE_LEVEL_9_2, D3D10_FEATURE_LEVEL_9_3, d3d10_1/D3D10_FEATURE_LEVEL1, d3d10_1/D3D10_FEATURE_LEVEL_10_0, d3d10_1/D3D10_FEATURE_LEVEL_10_1, d3d10_1/D3D10_FEATURE_LEVEL_9_1, d3d10_1/D3D10_FEATURE_LEVEL_9_2, d3d10_1/D3D10_FEATURE_LEVEL_9_3, direct3d10.d3d10_feature_level1
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d3d10_1.h
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
 - HeaderDef
api_location:
 - D3D10_1.h
api_name:
 - D3D10_FEATURE_LEVEL1
product: Windows
targetos: Windows
req.typenames: D3D10_FEATURE_LEVEL1
req.redist: 
---

# D3D10_FEATURE_LEVEL1 enumeration


## -description


The version of hardware acceleration requested.


## -enum-fields




### -field D3D10_FEATURE_LEVEL_10_0

The hardware supports Direct3D 10.0 features.


### -field D3D10_FEATURE_LEVEL_10_1

The hardware supports Direct3D 10.1 features.


### -field D3D10_FEATURE_LEVEL_9_1

The hardware supports 9.1 <a href="https://msdn.microsoft.com/5ad0525c-249f-452d-950b-df8fa2addde2">feature level</a>.


### -field D3D10_FEATURE_LEVEL_9_2

The hardware supports 9.2 <a href="https://msdn.microsoft.com/5ad0525c-249f-452d-950b-df8fa2addde2">feature level</a>.


### -field D3D10_FEATURE_LEVEL_9_3

The hardware supports 9.3 <a href="https://msdn.microsoft.com/5ad0525c-249f-452d-950b-df8fa2addde2">feature level</a>.


## -remarks



Use this enumeration when creating a device with <a href="https://msdn.microsoft.com/6eed32f7-985e-4456-815e-d289acba7ae7">D3D10CreateDevice1</a> or <a href="https://msdn.microsoft.com/c1ab6862-6499-41cc-9f20-34cfae1d66e2">D3D10CreateDeviceAndSwapChain1</a>.

Note that 10level9 feature levels 9_1, 9_2, and 9_3 are only available with the Direct3D 11 runtime (Windows 7, Windows Server 2008 R2, updated 
      Windows Vista with Service Pack 2 (SP2) [<a href="http://go.microsoft.com/fwlink/p/?linkid=160189">KB 971644</a>], and updated Windows Server 2008 [<a href="http://go.microsoft.com/fwlink/p/?linkid=183689">KB 971512</a>]).

For information about limitations creating nonhardware-type devices on certain feature levels, see <a href="https://msdn.microsoft.com/7e022e5d-daa3-48fa-b9fe-4b569220e55e">Limitations Creating WARP and Reference Devices</a>.

For an overview of 
      the capabilities of each feature level, see <a href="https://msdn.microsoft.com/5ad0525c-249f-452d-950b-df8fa2addde2">Overview For Each Feature Level</a>.




## -see-also




<a href="https://msdn.microsoft.com/3d1541bf-75d8-459d-a912-4068e9a0a9e4">Core Enumerations</a>



<a href="https://msdn.microsoft.com/529ced9a-d4fa-4b41-932b-343638cd5c7c">Hardware Support for Direct3D 10 Formats</a>



<a href="https://msdn.microsoft.com/011ad888-1c1d-4cbd-ab70-12fb8adc000f">Hardware Support for Direct3D 10.1 Formats</a>
 

 

