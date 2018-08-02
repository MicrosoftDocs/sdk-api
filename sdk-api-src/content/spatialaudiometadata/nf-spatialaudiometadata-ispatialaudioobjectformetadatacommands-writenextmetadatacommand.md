---
UID: NF:spatialaudiometadata.ISpatialAudioObjectForMetadataCommands.WriteNextMetadataCommand
title: ISpatialAudioObjectForMetadataCommands::WriteNextMetadataCommand
author: windows-sdk-content
description: Writes a metadata command to the spatial audio object, each command may only be added once per object per processing cycle.
old-location: coreaudio\ispatialaudioobjectformetadatacommands_writenextmetadatacommand.htm
old-project: CoreAudio
ms.assetid: 4880851E-C13F-49EC-BFC2-0F97F36D4D07
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ISpatialAudioObjectForMetadataCommands interface [Core Audio],WriteNextMetadataCommand method, ISpatialAudioObjectForMetadataCommands.WriteNextMetadataCommand, ISpatialAudioObjectForMetadataCommands::WriteNextMetadataCommand, WriteNextMetadataCommand, WriteNextMetadataCommand method [Core Audio], WriteNextMetadataCommand method [Core Audio],ISpatialAudioObjectForMetadataCommands interface, coreaudio.ispatialaudioobjectformetadatacommands_writenextmetadatacommand, spatialaudiometadata/ISpatialAudioObjectForMetadataCommands::WriteNextMetadataCommand
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: SpatialAudioMetadataWriterOverflowMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - spatialaudiometadata.h
api_name:
 - ISpatialAudioObjectForMetadataCommands.WriteNextMetadataCommand
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ISpatialAudioObjectForMetadataCommands::WriteNextMetadataCommand


## -description


Writes a metadata command to the spatial audio object, each command may only be added once per object per processing cycle. Valid commands and value lengths are defined by the metadata format specified in the <a href="https://msdn.microsoft.com/5B92F521-537F-4296-B9A7-7EC6985530B3">SpatialAudioObjectRenderStreamForMetadataActivationParams</a> when the <a href="https://msdn.microsoft.com/1623B280-FC12-4C19-9D4A-D8463D1A1046">ISpatialAudioObjectRenderStreamForMetadata</a> was created.


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




<a href="https://msdn.microsoft.com/B142D5CC-7321-4F3C-804D-50E728C37D10">ISpatialAudioObjectForMetadataCommands</a>
 

 

