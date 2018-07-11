---
UID: NN:spatialaudiometadata.ISpatialAudioObjectForMetadataCommands
title: ISpatialAudioObjectForMetadataCommands
author: windows-sdk-content
description: Used to write metadata commands for spatial audio.
old-location: coreaudio\ispatialaudioobjectformetadatacommands.htm
old-project: CoreAudio
ms.assetid: B142D5CC-7321-4F3C-804D-50E728C37D10
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: ISpatialAudioObjectForMetadataCommands, ISpatialAudioObjectForMetadataCommands interface [Core Audio], ISpatialAudioObjectForMetadataCommands interface [Core Audio],described, coreaudio.ispatialaudioobjectformetadatacommands, spatialaudiometadata/ISpatialAudioObjectForMetadataCommands
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: spatialaudiometadata.h
req.include-header: Spatialaudioclient.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - ISpatialAudioObjectForMetadataCommands
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# ISpatialAudioObjectForMetadataCommands interface


## -description


Used to write metadata commands for spatial audio. Valid commands and value lengths are defined by the metadata format specified in the <a href="https://msdn.microsoft.com/5B92F521-537F-4296-B9A7-7EC6985530B3">SpatialAudioObjectRenderStreamForMetadataActivationParams</a> when the <a href="https://msdn.microsoft.com/1623B280-FC12-4C19-9D4A-D8463D1A1046">ISpatialAudioObjectRenderStreamForMetadata</a> was created.

This interface is a part of  Windows Sonic, Microsoft’s audio platform for more immersive audio which includes integrated spatial sound on Xbox and Windows.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISpatialAudioObjectForMetadataCommands</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISpatialAudioObjectForMetadataCommands</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISpatialAudioObjectForMetadataCommands</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3896A6DF-158A-4DEA-961E-CFD38C2A4AC2">GetAudioObjectType</a>
</td>
<td align="left" width="63%">
Gets a value specifying the type of audio object that is represented by the <b>ISpatialAudioObjectForMetadataCommands</b>. This value indicates if the object is dynamic or static. If the object is static, one and only one of the static audio channel values to which the object is assigned is returned.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/jj983413">GetBuffer</a>
</td>
<td align="left" width="63%">
Gets a buffer that is used to supply the audio data for the <b>ISpatialAudioObjectForMetadataCommands</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0D6FB74F-1B3D-446D-AFC6-9EB3DEDD75A0">IsActive</a>
</td>
<td align="left" width="63%">
Gets a value indicating whether the <b>ISpatialAudioObjectForMetadataCommands</b> is valid. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/31AEA90B-9464-4A30-B2E4-EE93382E0C5D">SetEndOfStream</a>
</td>
<td align="left" width="63%">
Instructs the system that the final block of audio data has been  submitted for the <b>ISpatialAudioObjectForMetadataCommands</b> so that the object can be deactivated and it's resources reused. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4880851E-C13F-49EC-BFC2-0F97F36D4D07">WriteNextMetadataCommand</a>
</td>
<td align="left" width="63%">
Writes a metadata command to the spatial audio object, each command may only be added once per object per processing cycle. Valid commands and value lengths are defined by the metadata format specified in the <a href="https://msdn.microsoft.com/5B92F521-537F-4296-B9A7-7EC6985530B3">SpatialAudioObjectRenderStreamForMetadataActivationParams</a> when the <a href="https://msdn.microsoft.com/1623B280-FC12-4C19-9D4A-D8463D1A1046">ISpatialAudioObjectRenderStreamForMetadata</a> was created.

</td>
</tr>
</table> 

