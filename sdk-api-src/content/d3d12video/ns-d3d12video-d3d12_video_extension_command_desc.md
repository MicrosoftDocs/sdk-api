---
UID: NS:d3d12video.D3D12_VIDEO_EXTENSION_COMMAND_DESC
title: D3D12_VIDEO_EXTENSION_COMMAND_DESC
ms.date: 11/4/2019
targetos: Windows
description: Describes a video extension command. (D3D12_VIDEO_EXTENSION_COMMAND_DESC)
tech.root: mf
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: d3d12video.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.target-type: 
req.typenames: D3D12_VIDEO_EXTENSION_COMMAND_DESC
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_EXTENSION_COMMAND_DESC
f1_keywords:
 - D3D12_VIDEO_EXTENSION_COMMAND_DESC
 - d3d12video/D3D12_VIDEO_EXTENSION_COMMAND_DESC
dev_langs:
 - c++
---

## -description

Describes a video extension command.

## -struct-fields

### -field NodeMask

For single GPU operation, set this to zero. If there are multiple GPU nodes, set a bit to identify the node (the device's physical adapter) to which the command queue applies. Each bit in the mask corresponds to a single node. Only 1 bit may be set.

### -field CommandId

The unique identifier for the video extension command.

## -remarks

Pass this structure to [ID3D12VideoDevice2::CreateVideoExtensionCommand](nf-d3d12video-id3d12videodevice2-createvideoextensioncommand.md) to create an instance of [ID3D12VideoExtensionCommand](nn-d3d12video-id3d12videoextensioncommand.md).

## -see-also

