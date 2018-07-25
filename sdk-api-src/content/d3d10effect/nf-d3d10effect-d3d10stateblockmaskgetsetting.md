---
UID: NF:d3d10effect.D3D10StateBlockMaskGetSetting
title: D3D10StateBlockMaskGetSetting function
author: windows-sdk-content
description: Get an element in a state-block mask; determine if an element is allowed by the mask for capturing and applying.
old-location: direct3d10\d3d10stateblockmaskgetsetting.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10stateblockmaskgetsetting.htm
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: 6309c42d-db39-eb28-25e5-ba740c57a969, D3D10StateBlockMaskGetSetting, D3D10StateBlockMaskGetSetting function [Direct3D 10], d3d10effect/D3D10StateBlockMaskGetSetting, direct3d10.d3d10stateblockmaskgetsetting
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: d3d10effect.h
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
tech.root: 
req.typenames: D3D10_DEVICE_STATE_TYPES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D3D10.dll
api_name:
 - D3D10StateBlockMaskGetSetting
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: D3D10.dll
req.irql: 
---

# D3D10StateBlockMaskGetSetting function


## -description


Get an element in a state-block mask; determine if an element is allowed by the mask for capturing and applying.


## -parameters




### -param pMask [in]

Type: <b><a href="https://msdn.microsoft.com/library/Bb172453(v=VS.85).aspx">D3D10_STATE_BLOCK_MASK</a>*</b>

State block mask. See <a href="https://msdn.microsoft.com/library/Bb172453(v=VS.85).aspx">D3D10_STATE_BLOCK_MASK</a>.


### -param StateType [in]

Type: <b><a href="https://msdn.microsoft.com/library/Bb205039(v=VS.85).aspx">D3D10_DEVICE_STATE_TYPES</a></b>

The type of device state. See <a href="https://msdn.microsoft.com/library/Bb205039(v=VS.85).aspx">D3D10_DEVICE_STATE_TYPES</a>.


### -param Entry [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The entry within the device state. This is only relevant for state types that have more than one entry, such as D3D10_DST_GS_SAMPLERS.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Returns true if the specified feature is allowed by the mask for capturing and applying, and false otherwise.




## -see-also




<a href="https://msdn.microsoft.com/library/Bb205151(v=VS.85).aspx">Core Functions</a>



<a href="https://msdn.microsoft.com/library/Bb205177(v=VS.85).aspx">Effect Functions</a>
 

 

