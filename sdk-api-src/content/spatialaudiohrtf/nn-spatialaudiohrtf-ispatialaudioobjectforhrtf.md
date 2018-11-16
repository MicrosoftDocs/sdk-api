---
UID: NN:spatialaudiohrtf.ISpatialAudioObjectForHrtf
title: ISpatialAudioObjectForHrtf
author: windows-sdk-content
description: Represents an object that provides audio data to be rendered from a position in 3D space, relative to the user, a head-relative transfer function (HRTF).
old-location: coreaudio\ispatialaudioobjectforhrtf.htm
tech.root: CoreAudio
ms.assetid: E69F1D09-B937-4BCC-A040-18EF8A838289
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ISpatialAudioObjectForHrtf, ISpatialAudioObjectForHrtf interface [Core Audio], ISpatialAudioObjectForHrtf interface [Core Audio],described, coreaudio.ispatialaudioobjectforhrtf, spatialaudiohrtf/ISpatialAudioObjectForHrtf
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: spatialaudiohrtf.h
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
 - ISpatialAudioObjectForHrtf
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISpatialAudioObjectForHrtf interface


## -description


Represents an object that provides audio data to  be  rendered from a position in 3D space, relative to the user, a head-relative transfer function (HRTF). Spatial audio objects can be static or dynamic, which you specify with the <i>type</i> parameter to the <a href="https://msdn.microsoft.com/3E26D14B-5F69-4EBD-A48D-D63E24520D59">ISpatialAudioObjectRenderStreamForHrtf::ActivateSpatialAudioObjectForHrtf</a>   method. Dynamic audio objects can be placed in an arbitrary position in space and can be moved over time. Static audio objects are assigned to one or more channels, defined in the <a href="https://msdn.microsoft.com/DFFE770F-41C0-4048-A38F-FB96353E9216">AudioObjectType</a> enumeration, that each correlate to a fixed speaker location that may be a physical or a virtualized speaker

This interface is a part of  Windows Sonic, Microsoft’s audio platform for more immersive audio which includes integrated spatial sound on Xbox and Windows.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISpatialAudioObjectForHrtf</b> interface inherits from <a href="https://msdn.microsoft.com/54721875-D93A-4C7E-A07E-C286E1A409D3">ISpatialAudioObjectBase</a>. <b>ISpatialAudioObjectForHrtf</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISpatialAudioObjectForHrtf</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/20934FA5-2B4E-4FC4-B5B5-AFC4024ED2F8">SetDirectivity</a>
</td>
<td align="left" width="63%">
Sets the spatial audio directivity model for the <b>ISpatialAudioObjectForHrtf</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/62C95E6A-C27E-4C17-91E1-D6D80172F15B">SetDistanceDecay</a>
</td>
<td align="left" width="63%">
Sets the decay model that is applied over distance from the position of an <b>ISpatialAudioObjectForHrtf</b> to the position of the listener.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6D96F854-0FAE-4B8B-9033-E2AEB471B38B">SetEnvironment</a>
</td>
<td align="left" width="63%">
Sets the type of acoustic environment that is simulated when audio is processed for the <b>ISpatialAudioObjectForHrtf</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7DE268DC-5AA0-4866-8495-34292AEFB142">SetGain</a>
</td>
<td align="left" width="63%">
Sets the gain for the <b>ISpatialAudioObjectForHrtf</b>. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2B88643A-C81A-4F11-BFD0-EEF4C65861C8">SetOrientation</a>
</td>
<td align="left" width="63%">
Sets the orientation in 3D space, relative to the listener's frame of reference, from which the <b>ISpatialAudioObjectForHrtf</b> audio data will be rendered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4FB6852D-A793-43A1-A58F-E7DCFDB5BBDD">SetPosition</a>
</td>
<td align="left" width="63%">
Sets the position in 3D space, relative to the listener, from which the <b>ISpatialAudioObjectForHrtf</b> audio data will be rendered.

</td>
</tr>
</table> 


## -remarks



<div class="alert"><b>Note</b>  Many of the methods provided by this interface are implemented in the inherited <a href="https://msdn.microsoft.com/54721875-D93A-4C7E-A07E-C286E1A409D3">ISpatialAudioObjectBase</a> interface.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/54721875-D93A-4C7E-A07E-C286E1A409D3">ISpatialAudioObjectBase</a>
 

 

