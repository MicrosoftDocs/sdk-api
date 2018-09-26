---
UID: NF:spatialaudiometadata.ISpatialAudioObjectRenderStreamForMetadata.ActivateSpatialAudioObjectForMetadataCommands
title: ISpatialAudioObjectRenderStreamForMetadata::ActivateSpatialAudioObjectForMetadataCommands
author: windows-sdk-content
description: Activate an ISpatialAudioObjectForMetadataCommands for rendering.
old-location: coreaudio\ispatialaudioobjectrenderstreamformetadataitems_activatespatialaudioobjectformetadatacommands.htm
tech.root: CoreAudio
ms.assetid: 6EB7A7B7-6B52-4EB0-81CB-0F9626761CA8
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: ActivateSpatialAudioObjectForMetadataCommands, ActivateSpatialAudioObjectForMetadataCommands method [Core Audio], ActivateSpatialAudioObjectForMetadataCommands method [Core Audio],ISpatialAudioObjectRenderStreamForMetadata interface, ISpatialAudioObjectRenderStreamForMetadata interface [Core Audio],ActivateSpatialAudioObjectForMetadataCommands method, ISpatialAudioObjectRenderStreamForMetadata.ActivateSpatialAudioObjectForMetadataCommands, ISpatialAudioObjectRenderStreamForMetadata::ActivateSpatialAudioObjectForMetadataCommands, coreaudio.ispatialaudioobjectformetadataitems_activatespatialaudioobjectformetadatacommands, coreaudio.ispatialaudioobjectrenderstreamformetadataitems_activatespatialaudioobjectformetadatacommands, spatialaudiometadata/ISpatialAudioObjectRenderStreamForMetadata::ActivateSpatialAudioObjectForMetadataCommands
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: spatialaudiometadata.h
req.include-header: 
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - spatialaudiometadata.h
api_name:
 - ISpatialAudioObjectRenderStreamForMetadata.ActivateSpatialAudioObjectForMetadataCommands
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISpatialAudioObjectRenderStreamForMetadata::ActivateSpatialAudioObjectForMetadataCommands


## -description


Activate an <a href="https://msdn.microsoft.com/B142D5CC-7321-4F3C-804D-50E728C37D10">ISpatialAudioObjectForMetadataCommands</a> for rendering. 


## -parameters




### -param type [in]

The type of audio object to activate. For dynamic audio objects, this value must be <b>AudioObjectType_Dynamic</b>. For static audio objects, specify one of the static audio channel values from the enumeration. Specifying <b>AudioObjectType_None</b> will produce an audio object that is not spatialized.


### -param audioObject [out]

Receives a pointer to the activated interface. 


## -returns



If the method succeeds, it returns S_OK. If it fails, possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SPTLAUDCLNT_E_NO_MORE_OBJECTS</b></dt>
</dl>
</td>
<td width="60%">
The maximum number of simultaneous spatial audio objects has been exceeded. Call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> on unused audio objects before attempting to activate additional objects.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SPTLAUDCLNT_E_STATIC_OBJECT_NOT_AVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
The static channel specified in the <i>type</i> parameter was not included in the <b>StaticObjectTypeMask</b> field of the <a href="https://msdn.microsoft.com/5B92F521-537F-4296-B9A7-7EC6985530B3">SpatialAudioObjectRenderStreamForMetadataActivationParams</a> passed into <a href="https://msdn.microsoft.com/CBBB5A62-D342-4FB7-890C-9FE37949CC07">ISpatialAudioClient::ActivateSpatialAudioStream</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SPTLAUDCLNT_E_OBJECT_ALREADY_ACTIVE</b></dt>
</dl>
</td>
<td width="60%">
A spatial audio object has already been activated for the static channel specified in the <i>type</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The supplied pointer is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The value specified in the <i>type</i> parameter is not one of the values defined by the <a href="https://msdn.microsoft.com/DFFE770F-41C0-4048-A38F-FB96353E9216">AudioObjectType</a> enumeration.

</td>
</tr>
</table>
 




## -remarks



A dynamic <a href="https://msdn.microsoft.com/B142D5CC-7321-4F3C-804D-50E728C37D10">ISpatialAudioObjectForMetadataCommands</a> is one that was activated by setting the <i>type</i> parameter to the   <b>ActivateSpatialAudioObjectForMetadataCommands</b> method to <b>AudioObjectType_Dynamic</b>. The client has a limit of the maximum number of dynamic spatial audio objects that can be activated at one time. After the limit has been reached, attempting to activate additional audio objects will result in this method returning an SPTLAUDCLNT_E_NO_MORE_OBJECTS error. To avoid this, call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> on each dynamic <b>ISpatialAudioObjectForMetadataCommands</b> after it is no longer being used to free up the resource so that it can be reallocated. See  <a href="https://msdn.microsoft.com/3339E021-4AC3-43CB-9306-C8D58541CA5F">ISpatialAudioObjectBase::IsActive</a> and  <a href="https://msdn.microsoft.com/17294E5D-04D7-43B9-AD41-392344309308">ISpatialAudioObjectBase::SetEndOfStream</a> for more information on the managing the lifetime of spatial audio objects.




## -see-also




<a href="https://msdn.microsoft.com/4861D2AA-E685-4A72-BE98-6FEEB72ACF67">ISpatialAudioObjectForMetadataItems</a>
 

 

