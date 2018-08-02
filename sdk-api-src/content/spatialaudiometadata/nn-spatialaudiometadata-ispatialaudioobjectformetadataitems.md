---
UID: NN:spatialaudiometadata.ISpatialAudioObjectForMetadataItems
title: ISpatialAudioObjectForMetadataItems
author: windows-sdk-content
description: Used to write spatial audio metadata for applications that require multiple metadata items per buffer with frame-accurate placement.
old-location: coreaudio\ispatialaudioobjectformetadataitems.htm
old-project: CoreAudio
ms.assetid: 4861D2AA-E685-4A72-BE98-6FEEB72ACF67
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ISpatialAudioObjectForMetadataItems, ISpatialAudioObjectForMetadataItems interface [Core Audio], ISpatialAudioObjectForMetadataItems interface [Core Audio],described, coreaudio.ispatialaudioobjectformetadataitems, spatialaudiometadata/ISpatialAudioObjectForMetadataItems
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
 - ISpatialAudioObjectForMetadataItems
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ISpatialAudioObjectForMetadataItems interface


## -description


 Used to write spatial audio metadata for applications that require multiple metadata items per buffer with frame-accurate placement.  The data written via this interface must adhere to the format defined by the metadata format specified in the <a href="https://msdn.microsoft.com/5B92F521-537F-4296-B9A7-7EC6985530B3">SpatialAudioObjectRenderStreamForMetadataActivationParams</a> when the <a href="https://msdn.microsoft.com/1623B280-FC12-4C19-9D4A-D8463D1A1046">ISpatialAudioObjectRenderStreamForMetadata</a> was created.

This interface is a part of  Windows Sonic, Microsoft’s audio platform for more immersive audio which includes integrated spatial sound on Xbox and Windows.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISpatialAudioObjectForMetadataItems</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISpatialAudioObjectForMetadataItems</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISpatialAudioObjectForMetadataItems</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6EB7A7B7-6B52-4EB0-81CB-0F9626761CA8">ActivateSpatialAudioObjectForMetadataCommands</a>
</td>
<td align="left" width="63%">
Activate an <a href="https://msdn.microsoft.com/B142D5CC-7321-4F3C-804D-50E728C37D10">ISpatialAudioObjectForMetadataCommands</a> for rendering. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A9743D42-659A-404C-BB21-8A5086870F34">ActivateSpatialAudioObjectForMetadataItems</a>
</td>
<td align="left" width="63%">
Activate an <b>ISpatialAudioObjectForMetadataItems</b> for rendering. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/713289F7-32FC-4A1B-8E03-33E54F98B4E3">GetAudioObjectType</a>
</td>
<td align="left" width="63%">
Gets a value specifying the type of audio object that is represented by the <b>ISpatialAudioObjectForMetadataItems</b>. This value indicates if the object is dynamic or static. If the object is static, one and only one of the static audio channel values to which the object is assigned is returned.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/jj983413">GetBuffer</a>
</td>
<td align="left" width="63%">
Gets a buffer that is used to supply the audio data for the <b>ISpatialAudioObjectForMetadataItems</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/FD356AA9-F4BC-4864-8A9F-994EB527E123">GetSpatialAudioMetadataItems</a>
</td>
<td align="left" width="63%">
Gets a pointer to the <a href="https://msdn.microsoft.com/54A6B7DE-A41E-4214-AF02-CC19250B9037">ISpatialAudioMetadataItems</a> object which stores metadata items for  the  <b>ISpatialAudioObjectForMetadataItems</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8D957B91-9380-44D5-8AC4-F13FAC375D9F">IsActive</a>
</td>
<td align="left" width="63%">
Gets a value indicating whether the <b>ISpatialAudioObjectForMetadataItems</b> is valid. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/EF8A5E0D-ED1A-483F-98C6-CE636B4B1162">SetEndOfStream</a>
</td>
<td align="left" width="63%">
Instructs the system that the final block of audio data has been  submitted for the <b>ISpatialAudioObjectForMetadataItems</b> so that the object can be deactivated and it's resources reused. 

</td>
</tr>
</table> 

