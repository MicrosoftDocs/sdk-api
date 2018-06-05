---
UID: NS:d3d12.D3D12_FEATURE_DATA_COMMAND_QUEUE_PRIORITY
title: D3D12_FEATURE_DATA_COMMAND_QUEUE_PRIORITY
author: windows-sdk-content
description: Details the adapter's support for prioritization of different command queue types.
old-location: direct3d12\d3d12_feature_data_command_queue_priority.htm
old-project: direct3d12
ms.assetid: 70DB58DB-7EE0-4E5C-8B24-22DA9347A80F
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: D3D12_FEATURE_DATA_COMMAND_QUEUE_PRIORITY, D3D12_FEATURE_DATA_COMMAND_QUEUE_PRIORITY structure, d3d12/D3D12_FEATURE_DATA_COMMAND_QUEUE_PRIORITY, direct3d12.d3d12_feature_data_command_queue_priority
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: D3D12_FEATURE_DATA_COMMAND_QUEUE_PRIORITY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	d3d12.h
api_name:
-	D3D12_FEATURE_DATA_COMMAND_QUEUE_PRIORITY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D12_FEATURE_DATA_COMMAND_QUEUE_PRIORITY structure


## -description


Details the adapter's support for prioritization of different command queue types.


## -struct-fields




### -field CommandListType

<a href="https://msdn.microsoft.com/en-us/library/jj159528.aspx">SAL</a>: <code>_In_</code>

The type of the command list you're interested in.


### -field Priority

<a href="https://msdn.microsoft.com/en-us/library/jj159528.aspx">SAL</a>: <code>_In_</code>

The priority level you're interested in.


### -field PriorityForTypeIsSupported

<a href="https://msdn.microsoft.com/en-us/library/jj159528.aspx">SAL</a>: <code>_Out_</code>

On return, contains true if the specfied command list type supports the specified priority level; otherwise, false.


## -remarks



Use this structure with <a href="https://msdn.microsoft.com/2E986E37-30C7-45FE-BC8B-A6DD5670938F">CheckFeatureSupport</a> to determine the priority levels supported by various command queue types.

See the enumeration constant <b>D3D12_FEATURE_COMMAND_QUEUE_PRIORITY</b> in the <a href="https://msdn.microsoft.com/165ECFE0-1B18-4A26-8B9C-3CE53776A349">D3D12_FEATURE</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

