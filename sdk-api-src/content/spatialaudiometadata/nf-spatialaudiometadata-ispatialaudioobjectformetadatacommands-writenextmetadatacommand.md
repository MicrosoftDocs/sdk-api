---
UID: NF:spatialaudiometadata.ISpatialAudioObjectForMetadataCommands.WriteNextMetadataCommand
title: ISpatialAudioObjectForMetadataCommands::WriteNextMetadataCommand (spatialaudiometadata.h)
description: Writes a metadata command to the spatial audio object, each command may only be added once per object per processing cycle.
helpviewer_keywords: ["ISpatialAudioObjectForMetadataCommands interface [Core Audio]","WriteNextMetadataCommand method","ISpatialAudioObjectForMetadataCommands.WriteNextMetadataCommand","ISpatialAudioObjectForMetadataCommands::WriteNextMetadataCommand","WriteNextMetadataCommand","WriteNextMetadataCommand method [Core Audio]","WriteNextMetadataCommand method [Core Audio]","ISpatialAudioObjectForMetadataCommands interface","coreaudio.ispatialaudioobjectformetadatacommands_writenextmetadatacommand","spatialaudiometadata/ISpatialAudioObjectForMetadataCommands::WriteNextMetadataCommand"]
old-location: coreaudio\ispatialaudioobjectformetadatacommands_writenextmetadatacommand.htm
tech.root: CoreAudio
ms.assetid: 4880851E-C13F-49EC-BFC2-0F97F36D4D07
ms.date: 12/05/2018
ms.keywords: ISpatialAudioObjectForMetadataCommands interface [Core Audio],WriteNextMetadataCommand method, ISpatialAudioObjectForMetadataCommands.WriteNextMetadataCommand, ISpatialAudioObjectForMetadataCommands::WriteNextMetadataCommand, WriteNextMetadataCommand, WriteNextMetadataCommand method [Core Audio], WriteNextMetadataCommand method [Core Audio],ISpatialAudioObjectForMetadataCommands interface, coreaudio.ispatialaudioobjectformetadatacommands_writenextmetadatacommand, spatialaudiometadata/ISpatialAudioObjectForMetadataCommands::WriteNextMetadataCommand
req.header: spatialaudiometadata.h
req.include-header: Spatialaudioclient.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISpatialAudioObjectForMetadataCommands::WriteNextMetadataCommand
 - spatialaudiometadata/ISpatialAudioObjectForMetadataCommands::WriteNextMetadataCommand
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - spatialaudiometadata.h
api_name:
 - ISpatialAudioObjectForMetadataCommands.WriteNextMetadataCommand
---

# ISpatialAudioObjectForMetadataCommands::WriteNextMetadataCommand


## -description

Writes a metadata command to the spatial audio object, each command may only be added once per object per processing cycle. Valid commands and value lengths are defined by the metadata format specified in the <a href="/windows/desktop/api/spatialaudiometadata/ns-spatialaudiometadata-spatialaudioobjectrenderstreamformetadataactivationparams">SpatialAudioObjectRenderStreamForMetadataActivationParams</a> when the <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudioobjectrenderstreamformetadata">ISpatialAudioObjectRenderStreamForMetadata</a> was created.

## -parameters

### -param commandID [in]

The ID of the metadata command.

### -param valueBuffer [in]

The buffer containing the value data for the metadata command.

### -param valueBufferLength [in]

The length of the <i>valueBuffer</i>.

## -returns

If the method succeeds, it returns S_OK.

## -see-also

<a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudioobjectformetadatacommands">ISpatialAudioObjectForMetadataCommands</a>