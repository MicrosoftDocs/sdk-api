---
UID: NN:spatialaudiohrtf.ISpatialAudioObjectForHrtf
title: ISpatialAudioObjectForHrtf
author: windows-sdk-content
description: Represents an object that provides audio data to be rendered from a position in 3D space, relative to the user, a head-relative transfer function (HRTF).
old-location: coreaudio\ispatialaudioobjectforhrtf.htm
old-project: CoreAudio
ms.assetid: E69F1D09-B937-4BCC-A040-18EF8A838289
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: ISpatialAudioObjectForHrtf, ISpatialAudioObjectForHrtf interface [Core Audio], ISpatialAudioObjectForHrtf interface [Core Audio],described, coreaudio.ispatialaudioobjectforhrtf, spatialaudiohrtf/ISpatialAudioObjectForHrtf
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: SpatialAudioHrtfEnvironmentType
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
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# ISpatialAudioObjectForHrtf interface


## -description


Represents an object that provides audio data to  be  rendered from a position in 3D space, relative to the user, a head-relative transfer function (HRTF). Spatial audio objects can be static or dynamic, which you specify with the <i>type</i> parameter to the <a href="https://msdn.microsoft.com/3E26D14B-5F69-4EBD-A48D-D63E24520D59">ISpatialAudioObjectRenderStream::ForHrtfActivateSpatialAudioObject</a>   method. Dynamic audio objects can be placed in an arbitrary position in space and can be moved over time. Static audio objects are assigned to one or more channels, defined in the <a href="https://msdn.microsoft.com/DFFE770F-41C0-4048-A38F-FB96353E9216">AudioObjectType</a> enumeration, that each correlate to a fixed speaker location that may be a physical or a virtualized speaker

This interface is a part of  Windows Sonic, Microsoft’s audio platform for more immersive audio which includes integrated spatial sound on Xbox and Windows.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISpatialAudioObjectForHrtf</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISpatialAudioObjectForHrtf</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/6B4FCDC6-C010-4293-A407-DD8137260B50">GetAudioObjectType</a>
</td>
<td align="left" width="63%">
Gets a value specifying the type of audio object that is represented by the <b>ISpatialAudioObjectForHrtf</b>. This value indicates if the object is dynamic or static. If the object is static, one and only one of the static audio channel values to which the object is assigned is returned.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/jj983413">GetBuffer</a>
</td>
<td align="left" width="63%">
Gets a buffer that is used to supply the audio data for the <b>ISpatialAudioObjectForHrtf</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/25465859-017E-48AC-84B4-702794C6CE43">IsActive</a>
</td>
<td align="left" width="63%">
Gets a value indicating whether the <b>ISpatialAudioObjectForHrtf</b> is valid. 

</td>
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
<a href="https://msdn.microsoft.com/82AA5202-C12C-4DFB-B4C5-745D4756C1FA">SetEndOfStream</a>
</td>
<td align="left" width="63%">
Instructs the system that the final block of audio data has been  submitted for the <b>ISpatialAudioObjectForHrtf</b> so that the object can be deactivated and it's resources reused. 

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

