---
UID: NF:spatialaudiohrtf.ISpatialAudioObjectRenderStreamForHrtf.ActivateSpatialAudioObjectForHrtf
title: ISpatialAudioObjectRenderStreamForHrtf::ActivateSpatialAudioObjectForHrtf
author: windows-sdk-content
description: Activates an ISpatialAudioObjectForHrtf for audio rendering.
old-location: coreaudio\ispatialaudiorenderstreamforhrtf_activatespatialaudioobjectforhrtf.htm
tech.root: CoreAudio
ms.assetid: 3E26D14B-5F69-4EBD-A48D-D63E24520D59
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ActivateSpatialAudioObjectForHrtf, ActivateSpatialAudioObjectForHrtf method [Core Audio], ActivateSpatialAudioObjectForHrtf method [Core Audio],ISpatialAudioObjectRenderStreamForHrtf interface, ISpatialAudioObjectRenderStreamForHrtf interface [Core Audio],ActivateSpatialAudioObjectForHrtf method, ISpatialAudioObjectRenderStreamForHrtf.ActivateSpatialAudioObjectForHrtf, ISpatialAudioObjectRenderStreamForHrtf::ActivateSpatialAudioObjectForHrtf, coreaudio.ispatialaudiorenderstreamforhrtf_activatespatialaudioobjectforhrtf, spatialaudiohrtf/ISpatialAudioObjectRenderStreamForHrtf::ActivateSpatialAudioObjectForHrtf
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: spatialaudiohrtf.h
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
 - spatialaudiohrtf.h
api_name:
 - ISpatialAudioObjectRenderStreamForHrtf.ActivateSpatialAudioObjectForHrtf
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- spatialaudiohrtf.h
: 
- ISpatialAudioObjectRenderStreamForHrtf.ActivateSpatialAudioObjectForHrtf
: 
---

# ISpatialAudioObjectRenderStreamForHrtf::ActivateSpatialAudioObjectForHrtf


## -description


Activates an <a href="https://msdn.microsoft.com/E69F1D09-B937-4BCC-A040-18EF8A838289">ISpatialAudioObjectForHrtf</a> for audio rendering.


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
<dt><b>SPTLAUDCLNT_E_NO_MORE_OBJECTS </b></dt>
</dl>
</td>
<td width="60%">
The system has reached the maximum number of simultaneous audio objects.

</td>
</tr>
</table>
 




## -remarks



A dynamic <a href="https://msdn.microsoft.com/E69F1D09-B937-4BCC-A040-18EF8A838289">ISpatialAudioObjectForHrtf</a> is one that was activated by setting the <i>type</i> parameter to the   <b>ActivateSpatialAudioObjectForHrtf</b> method to <b>AudioObjectType_Dynamic</b>. The client has a limit of the maximum number of dynamic spatial audio objects that can be activated at one time. After the limit has been reached, attempting to activate additional audio objects will result in this method returning an SPTLAUDCLNT_E_NO_MORE_OBJECTS error. To avoid this, call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> on each dynamic <b>ISpatialAudioObjectForHrtf</b> after it is no longer being used to free up the resource so that it can be reallocated. See <a href="https://msdn.microsoft.com/3339E021-4AC3-43CB-9306-C8D58541CA5F">ISpatialAudioObjectgBase::IsActive</a> and  <a href="https://msdn.microsoft.com/17294E5D-04D7-43B9-AD41-392344309308">ISpatialAudioObjectgBase::SetEndOfStream</a> for more information on the managing the lifetime of spatial audio objects.




## -see-also




<a href="https://msdn.microsoft.com/9DFEF82A-1571-47AB-BE0E-059BCCC8289A">ISpatialAudioRenderStreamForHrtf</a>
 

 

