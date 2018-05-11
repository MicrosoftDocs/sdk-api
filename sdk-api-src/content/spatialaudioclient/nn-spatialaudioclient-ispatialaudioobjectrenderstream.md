---
UID: NN:spatialaudioclient.ISpatialAudioObjectRenderStream
title: ISpatialAudioObjectRenderStream
author: windows-driver-content
description: Provides methods for controlling a spatial audio object render stream, including starting, stopping, and resetting the stream.
old-location: coreaudio\ispatialaudioobjectrenderstream.htm
old-project: CoreAudio
ms.assetid: B4D10CC6-62BF-4D20-910F-E39DF812010D
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: ISpatialAudioObjectRenderStream, ISpatialAudioObjectRenderStream interface [Core Audio], ISpatialAudioObjectRenderStream interface [Core Audio],described, coreaudio.ispatialaudioobjectrenderstream, spatialaudioclient/ISpatialAudioObjectRenderStream
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: AudioObjectType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	spatialaudioclient.h
api_name:
-	ISpatialAudioObjectRenderStream
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# ISpatialAudioObjectRenderStream interface


## -description


Provides methods for controlling a spatial audio object render stream, including starting, stopping, and resetting the stream. Also provides methods for activating new <a href="https://msdn.microsoft.com/EE83AF5F-4342-4CF2-81A7-1123F8DAFA6F">ISpatialAudioObject</a> instances and notifying the system when you are beginning and ending the process of updating activated spatial audio objects and data.

This interface is a part of  Windows Sonic, Microsoft’s audio platform for more immersive audio which includes integrated spatial sound on Xbox and Windows.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISpatialAudioObjectRenderStream</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISpatialAudioObjectRenderStream</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISpatialAudioObjectRenderStream</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1B99E7FB-0796-4902-9B00-470FD08F8AFA">ActivateSpatialAudioObject</a>
</td>
<td align="left" width="63%">
Activates an <a href="https://msdn.microsoft.com/EE83AF5F-4342-4CF2-81A7-1123F8DAFA6F">ISpatialAudioObject</a> for audio rendering.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9D858556-2EBE-4DF6-878B-BE0E12079248">BeginUpdatingAudioObjects</a>
</td>
<td align="left" width="63%">
Puts the system into the state where audio object data can be submitted for processing and the <a href="https://msdn.microsoft.com/EE83AF5F-4342-4CF2-81A7-1123F8DAFA6F">ISpatialAudioObject</a> state can be modified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/111DB695-66F6-45DD-B3B6-1DFB0D5D29FC">EndUpdatingAudioObjects</a>
</td>
<td align="left" width="63%">
Notifies the system that the app has finished supplying audio data for the spatial audio objects activated with <a href="https://msdn.microsoft.com/1B99E7FB-0796-4902-9B00-470FD08F8AFA">ActivateSpatialAudioObject</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5E17B53A-B999-4B08-9DFB-96D55E7F9CF7">GetAvailableDynamicObjectCount</a>
</td>
<td align="left" width="63%">
Gets the number of dynamic spatial audio objects that are currently available.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9262C9E1-DE15-460C-9BC2-DAD5163F447E">GetService</a>
</td>
<td align="left" width="63%">
Gets additional services from the <b>ISpatialAudioObjectRenderStream</b>.

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

