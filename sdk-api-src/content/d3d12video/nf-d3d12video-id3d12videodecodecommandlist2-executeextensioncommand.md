---
UID: NF:d3d12video.ID3D12VideoDecodeCommandList2.ExecuteExtensionCommand
title: ID3D12VideoDecodeCommandList2::ExecuteExtensionCommand
ms.date: 11/4/2019
targetos: Windows
description: Records a command to execute a video extension command into a decode command list.
tech.root: mf
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
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
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
 - ID3D12VideoDecodeCommandList2::ExecuteExtensionCommand
f1_keywords:
 - ID3D12VideoDecodeCommandList2::ExecuteExtensionCommand
 - d3d12video/ID3D12VideoDecodeCommandList2::ExecuteExtensionCommand
dev_langs:
 - c++
---

## -description

Records a command to execute a video extension command into a decode command list.

## -parameters

### -param pExtensionCommand

Pointer to an [ID3D12VideoExtensionCommand](nn-d3d12video-id3d12videoextensioncommand.md) representing the video extension command to execute.  The caller is responsible for maintaining object lifetime until command execution is complete.

### -param pExecutionParameters

A pointer to the execution parameters structure, which is defined by the command.  The parameters structure must match the parameters enumerated by a call to [ID3D12VideoDevice::CheckFeatureSupport](nf-d3d12video-id3d12videodevice-checkfeaturesupport.md) with the feature value of [D3D12_FEATURE_VIDEO_EXTENSION_COMMAND_PARAMETERS](ne-d3d12video-d3d12_feature_video.md) and a parameter stage value of [D3D12_VIDEO_EXTENSION_COMMAND_PARAMETER_STAGE_EXECUTION](ne-d3d12video-d3d12_video_extension_command_parameter_stage.md).

### -param ExecutionParametersSizeInBytes

The size of the *pExecutionParameters* parameter structure, in bytes.

## -remarks

Errors initializing the extension command are reported via debug layers and the return value of the command list's [Close](nf-d3d12video-id3d12videodecodecommandlist-close.md) method.

## -see-also

