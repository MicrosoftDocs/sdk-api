---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# ISpatialAudioObjectRenderStreamForMetadata::ActivateSpatialAudioObjectForMetadataItems


## -description


Activate an <a href="https://msdn.microsoft.com/4861D2AA-E685-4A72-BE98-6FEEB72ACF67">ISpatialAudioObjectForMetadataItems</a> for rendering. 


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



A dynamic <a href="https://msdn.microsoft.com/4861D2AA-E685-4A72-BE98-6FEEB72ACF67">ISpatialAudioObjectForMetadataItems</a> is one that was activated by setting the <i>type</i> parameter to the   <b>ActivateSpatialAudioObjectForMetadataItems</b> method to <b>AudioObjectType_Dynamic</b>. The client has a limit of the maximum number of dynamic spatial audio objects that can be activated at one time. After the limit has been reached, attempting to activate additional audio objects will result in this method returning an SPTLAUDCLNT_E_NO_MORE_OBJECTS error. To avoid this, call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> on each dynamic <b>ISpatialAudioObjectForMetadataItems</b> after it is no longer being used to free up the resource so that it can be reallocated. See <a href="https://msdn.microsoft.com/8D957B91-9380-44D5-8AC4-F13FAC375D9F">ISpatialAudioObjectForMetadataItems::IsActive</a>  and <a href="https://msdn.microsoft.com/EF8A5E0D-ED1A-483F-98C6-CE636B4B1162">ISpatialAudioObjectForMetadataItems::SetEndOfStream</a> for more information on the managing the lifetime of spatial audio objects.




## -see-also




<a href="https://msdn.microsoft.com/4861D2AA-E685-4A72-BE98-6FEEB72ACF67">ISpatialAudioObjectForMetadataItems</a>
 

 

