---
UID: NF:d3d12video.ID3D12VideoDevice2.ExecuteExtensionCommand
title: ID3D12VideoDevice2::ExecuteExtensionCommand
description: Executes a video extension command.
tech.root: mf
ms.date: 8/19/2019
ms.keywords: ID3D12VideoDevice2::ExecuteExtensionCommand
targetos: Windows
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
f1_keywords:
 - ID3D12VideoDevice2::ExecuteExtensionCommand
 - d3d12video/ID3D12VideoDevice2::ExecuteExtensionCommand
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - d3d12video.h
api_name:
 - ID3D12VideoDevice2::ExecuteExtensionCommand
---

## -description

Executes a video extension command.

## -parameters

### -param pExtensionCommand

Pointer to an [ID3D12VideoExtensionCommand](nn-d3d12video-id3d12videoextensioncommand.md) representing the video extension command to execute.  The caller is responsible for maintaining object lifetime until command execution is complete.

### -param pExecutionParameters

A pointer to the execution input parameters structure, which is defined by the command.  The parameters structure must match the parameters enumerated by a call to [ID3D12VideoDevice::CheckFeatureSupport](nf-d3d12video-id3d12videodevice-checkfeaturesupport.md) with the feature value of [D3D12_FEATURE_VIDEO_EXTENSION_COMMAND_PARAMETERS](ne-d3d12video-d3d12_feature_video.md) and a parameter stage value of [D3D12_VIDEO_EXTENSION_COMMAND_PARAMETER_STAGE_EXECUTION](ne-d3d12video-d3d12_video_extension_command_parameter_stage.md).

### -param ExecutionParametersSizeInBytes

The size of the *pExecutionParameters* parameter structure, in bytes.

### -param pOutputData

A pointer to the execution output parameters structure, which is defined by the command.

### -param OutputDataSizeInBytes

Receives the size of the *pExecutionParameters* parameter structure, in bytes.

## -returns

This method returns HRESULT.

## -remarks

Video extension commands executed through this method must complete before this method returns. For efficiency, extension implementations should schedule work in command lists instead of using this method, whenever possible. Each video command list type provides an **ExecuteExtensionCommand** for scheduled work. These include:

- [ID3D12VideoDecodeComandlist2::ExecuteExtensionCommand](nf-d3d12video-id3d12videodecodecommandlist2-executeextensioncommand.md)
- [ID3D12VideoEncodeComandlist1::ExecuteExtensionCommand](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice2-executeextensioncommand)
- [ID3D12VideoProcessComandlist2::ExecuteExtensionCommand](nf-d3d12video-id3d12videoprocesscommandlist2-executeextensioncommand.md)

## -see-also

- [ID3D12VideoDecodeComandlist2::ExecuteExtensionCommand](nf-d3d12video-id3d12videodecodecommandlist2-executeextensioncommand.md)
- [ID3D12VideoEncodeComandlist1::ExecuteExtensionCommand](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice2-executeextensioncommand)
- [ID3D12VideoProcessComandlist2::ExecuteExtensionCommand](nf-d3d12video-id3d12videoprocesscommandlist2-executeextensioncommand.md)
