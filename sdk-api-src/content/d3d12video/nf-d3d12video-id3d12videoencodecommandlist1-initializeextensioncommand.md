---
UID: NF:d3d12video.ID3D12VideoEncodeCommandList1.InitializeExtensionCommand
tech.root: 
title: ID3D12VideoEncodeCommandList1::InitializeExtensionCommand
ms.date: 07/13/2021
targetos: Windows
description: Records a command to initializes or re-initializes a video extension command into a video encode command list.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: d3d12video.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - d3d12video.h
api_name:
 - ID3D12VideoEncodeCommandList1::InitializeExtensionCommand
f1_keywords:
 - ID3D12VideoEncodeCommandList1::InitializeExtensionCommand
 - d3d12video/ID3D12VideoEncodeCommandList1::InitializeExtensionCommand
dev_langs:
 - c++
---

## -description

Records a command to initializes or re-initializes a video extension command into a video encode command list.

## -parameters

### -param pExtensionCommand

Pointer to an [ID3D12VideoExtensionCommand](nn-d3d12video-id3d12videoextensioncommand.md) representing the video extension command to initialize.  The caller is responsible for maintaining object lifetime until command execution is complete.

### -param pInitializationParameters

A pointer to the creation parameters structure, which is defined by the command.  The parameters structure must match the parameters enumerated by a call to [ID3D12VideoDevice::CheckFeatureSupport](nf-d3d12video-id3d12videodevice-checkfeaturesupport.md) with the feature value of [D3D12_FEATURE_VIDEO_EXTENSION_COMMAND_PARAMETERS](ne-d3d12video-d3d12_feature_video.md) and a parameter stage value of [D3D12_VIDEO_EXTENSION_COMMAND_PARAMETER_STAGE_INITIALIZATION](ne-d3d12video-d3d12_video_extension_command_parameter_stage.md).

### -param InitializationParametersSizeInBytes

The size of the *pInitializationParameters* parameter structure, in bytes.

## -remarks

Errors initializing the extension command are reported via debug layers and the return value of the command list's [Close](nf-d3d12video-id3d12videodecodecommandlist-close.md) method.

## -see-also

