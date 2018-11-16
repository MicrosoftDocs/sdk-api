---
UID: NN:spatialaudioclient.ISpatialAudioObjectRenderStreamBase
title: ISpatialAudioObjectRenderStreamBase
author: windows-sdk-content
description: Base interface that provides methods for controlling a spatial audio object render stream, including starting, stopping, and resetting the stream.
old-location: coreaudio\ispatialaudioobjectrenderstreambase.htm
tech.root: CoreAudio
ms.assetid: 2C2BE871-EFD1-40E1-B466-6BBD09C56852
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ISpatialAudioObjectRenderStreamBase, ISpatialAudioObjectRenderStreamBase interface [Core Audio], ISpatialAudioObjectRenderStreamBase interface [Core Audio],described, coreaudio.ispatialaudioobjectrenderstreambase, spatialaudioclient/ISpatialAudioObjectRenderStreamBase
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
 - ISpatialAudioObjectRenderStreamBase
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISpatialAudioObjectRenderStreamBase interface


## -description



Base interface that provides methods for controlling a spatial audio object render stream, including starting, stopping, and resetting the stream. Also provides methods for activating new <a href="https://msdn.microsoft.com/EE83AF5F-4342-4CF2-81A7-1123F8DAFA6F">ISpatialAudioObject</a> instances and notifying the system when you are beginning and ending the process of updating activated spatial audio objects and data.

This interface is a part of  Windows Sonic, Microsoft’s audio platform for more immersive audio which includes integrated spatial sound on Xbox and Windows. 




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISpatialAudioObjectRenderStreamBase</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISpatialAudioObjectRenderStreamBase</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISpatialAudioObjectRenderStreamBase</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
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
<a href="https://msdn.microsoft.com/F6F096C0-3384-4463-B25F-99C6A7B3263B">Reset</a>
</td>
<td align="left" width="63%">
Reset a stopped audio stream.   
      


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/25D968AC-F5D2-4CAB-87ED-29FC63E5A5A4">Start</a>
</td>
<td align="left" width="63%">
Starts the spatial audio stream.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6ECD17AB-C37D-4F4E-9D7F-EC48FC3B838C">Stop</a>
</td>
<td align="left" width="63%">
Stops a running audio stream.   

</td>
</tr>
</table> 

