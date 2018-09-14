---
UID: NN:spatialaudioclient.ISpatialAudioObject
title: ISpatialAudioObject
author: windows-sdk-content
description: Represents an object that provides audio data to be rendered from a position in 3D space, relative to the user.
old-location: coreaudio\ispatialaudioobject.htm
tech.root: CoreAudio
ms.assetid: EE83AF5F-4342-4CF2-81A7-1123F8DAFA6F
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ISpatialAudioObject, ISpatialAudioObject interface [Core Audio], ISpatialAudioObject interface [Core Audio],described, coreaudio.ispatialaudioobject, spatialaudioclient/ISpatialAudioObject
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: spatialaudioclient.h
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
 - spatialaudioclient.h
api_name:
 - ISpatialAudioObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISpatialAudioObject interface


## -description


Represents an object that provides audio data to  be  rendered from a position in 3D space, relative to the user. Spatial audio objects can be static or dynamic, which you specify with the <i>type</i> parameter to the  <a href="https://msdn.microsoft.com/1B99E7FB-0796-4902-9B00-470FD08F8AFA">ISpatialAudioObjectRenderStream::ActivateSpatialAudioObject</a> method. Dynamic audio objects can be placed in an arbitrary position in space and can be moved over time. Static audio objects are assigned to one or more channels, defined in the <a href="https://msdn.microsoft.com/DFFE770F-41C0-4048-A38F-FB96353E9216">AudioObjectType</a> enumeration, that each correlate to a fixed speaker location that may be a physical or a virtualized speaker.

This interface is a part of  Windows Sonic, Microsoft’s audio platform for more immersive audio which includes integrated spatial sound on Xbox and Windows.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISpatialAudioObject</b> interface inherits from <a href="https://msdn.microsoft.com/54721875-D93A-4C7E-A07E-C286E1A409D3">ISpatialAudioObjectBase</a>. <b>ISpatialAudioObject</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISpatialAudioObject</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/DDF4859E-6510-45D5-82E7-2C5A7F2EC679">SetPosition</a>
</td>
<td align="left" width="63%">
Sets the position in 3D space, relative to the listener, from which the <b>ISpatialAudioObject</b> audio data will be rendered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/DC1B4B9C-BFE0-4308-AD34-500A30C5744F">SetVolume</a>
</td>
<td align="left" width="63%">
Sets an audio amplitude multiplier that will be applied to the audio data provided by the <b>ISpatialAudioObject</b> before it is submitted to the audio rendering engine.

</td>
</tr>
</table> 


## -remarks



<div class="alert"><b>Note</b>  Many of the methods provided by this interface are implemented in the inherited <a href="https://msdn.microsoft.com/54721875-D93A-4C7E-A07E-C286E1A409D3">ISpatialAudioObjectBase</a> interface.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/54721875-D93A-4C7E-A07E-C286E1A409D3">ISpatialAudioObjectBase</a>
 

 

