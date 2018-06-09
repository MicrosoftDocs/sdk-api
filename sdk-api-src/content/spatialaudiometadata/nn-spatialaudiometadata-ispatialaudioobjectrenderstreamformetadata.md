---
UID: NN:spatialaudiometadata.ISpatialAudioObjectRenderStreamForMetadata
title: ISpatialAudioObjectRenderStreamForMetadata
author: windows-sdk-content
description: Provides methods for controlling a spatial audio object render stream for metadata, including starting, stopping, and resetting the stream.
old-location: coreaudio\ispatialaudioobjectrenderstreamformetadata.htm
old-project: CoreAudio
ms.assetid: 1623B280-FC12-4C19-9D4A-D8463D1A1046
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: ISpatialAudioObjectRenderStreamForMetadata, ISpatialAudioObjectRenderStreamForMetadata interface [Core Audio], ISpatialAudioObjectRenderStreamForMetadata interface [Core Audio],described, coreaudio.ispatialaudioobjectrenderstreamformetadata, spatialaudiometadata/ISpatialAudioObjectRenderStreamForMetadata
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: spatialaudiometadata.h
req.include-header: 
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
 - SpatialAudioMetadata.h
api_name:
 - ISpatialAudioObjectRenderStreamForMetadata
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# ISpatialAudioObjectRenderStreamForMetadata interface


## -description


Provides methods for controlling a spatial audio object render stream for metadata, including starting, stopping, and resetting the stream. Also provides methods for activating new <a href="https://msdn.microsoft.com/B142D5CC-7321-4F3C-804D-50E728C37D10">ISpatialAudioObjectForMetadataCommands</a> and <a href="https://msdn.microsoft.com/4861D2AA-E685-4A72-BE98-6FEEB72ACF67">ISpatialAudioObjectForMetadataItems</a> instances and notifying the system when you are beginning and ending the process of updating activated spatial audio objects and data.

This interface is a part of  Windows Sonic, Microsoft’s audio platform for more immersive audio which includes integrated spatial sound on Xbox and Windows.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISpatialAudioObjectRenderStreamForMetadata</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISpatialAudioObjectRenderStreamForMetadata</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISpatialAudioObjectRenderStreamForMetadata</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0BECB2AC-A889-443D-8360-E266F21AA240">BeginUpdatingAudioObjects</a>
</td>
<td align="left" width="63%">
Puts the system into the state where audio object data can be submitted for processing and the <b>ISpatialAudioObjectRenderStreamForMetadata</b> state can be modified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/FD49F2D6-D510-4995-9B09-65F7CCCB7337">EndUpdatingAudioObjects</a>
</td>
<td align="left" width="63%">
Notifies the system that the app has finished supplying audio data for the spatial audio objects activated with <a href="coreaudio.ispatialaudioobjectformetadataitems_activatespatialaudioobjectformetadatacommands">ActivateSpatialAudioObjectForMetadataCommands</a> or <a href="https://msdn.microsoft.com/A9743D42-659A-404C-BB21-8A5086870F34">ActivateSpatialAudioObjectForMetadataItems</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A92C6CC8-BD49-480A-BED2-E434E271951B">GetAvailableDynamicObjectCount</a>
</td>
<td align="left" width="63%">
Gets the number of dynamic spatial audio objects that are currently available.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/568F3D03-7296-475B-880B-E6FD0C2BD863">GetService</a>
</td>
<td align="left" width="63%">
Gets additional services from the <b>ISpatialAudioObjectRenderStreamForMetadata</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a>
</td>
<td align="left" width="63%">
Reset a stopped audio stream.   
      


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh973223">Start</a>
</td>
<td align="left" width="63%">
Starts the spatial audio stream.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn927275">Stop</a>
</td>
<td align="left" width="63%">
Stops a running audio stream.   

</td>
</tr>
</table> 

