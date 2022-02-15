---
UID: NF:d3d12video.ID3D12VideoDevice2.CreateVideoExtensionCommand
title: ID3D12VideoDevice2::CreateVideoExtensionCommand
description: Creates a video extension command.
tech.root: mf
ms.date: 6/7/2019
ms.keywords: ID3D12VideoDevice2::CreateVideoExtensionCommand
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
 - ID3D12VideoDevice2::CreateVideoExtensionCommand
 - d3d12video/ID3D12VideoDevice2::CreateVideoExtensionCommand
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - d3d12video.h
api_name:
 - ID3D12VideoDevice2::CreateVideoExtensionCommand
---

## -description

Creates a video extension command.

## -parameters

### -param pDesc

The [D3D12_VIDEO_EXTENSION_COMMAND_DESC](ns-d3d12video-d3d12_video_extension_command_desc.md) describing the command to be created.

### -param pCreationParameters

A pointer to the creation parameters structure, which is defined by the command.  The parameters structure must match the parameters enumerated by a call to [ID3D12VideoDevice::CheckFeatureSupport](nf-d3d12video-id3d12videodevice-checkfeaturesupport.md) with the feature value of [D3D12_FEATURE_VIDEO_EXTENSION_COMMAND_PARAMETERS](ne-d3d12video-d3d12_feature_video.md) and a parameter stage value of [D3D12_VIDEO_EXTENSION_COMMAND_PARAMETER_STAGE_CREATION](ne-d3d12video-d3d12_video_extension_command_parameter_stage.md).

### -param CreationParametersDataSizeInBytes

The size of the *pCreationParameters* parameter structure, in bytes.

### -param pProtectedResourceSession

A [ID3D12ProtectedResourceSession](../d3d12/nn-d3d12-id3d12protectedresourcesession.md) for managing access to protected resources.

### -param riid

The globally unique identifier (GUID) for the [ID3D12VideoExtensionCommand](nn-d3d12video-id3d12videoextensioncommand.md) interface.

### -param ppVideoExtensionCommand

A  pointer to a memory block that receives a pointer to the [ID3D12VideoExtensionCommand](nn-d3d12video-id3d12videoextensioncommand.md) interface.

## -returns

This method returns an HRESULT.

## -remarks

## -see-also
