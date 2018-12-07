---
UID: NF:spatialaudioclient.ISpatialAudioObjectRenderStreamBase.GetService
title: ISpatialAudioObjectRenderStreamBase::GetService
author: windows-sdk-content
description: Gets additional services from the ISpatialAudioObjectRenderStream.
old-location: coreaudio\ispatialaudioobjectrenderstream_getservice.htm
tech.root: CoreAudio
ms.assetid: 9262C9E1-DE15-460C-9BC2-DAD5163F447E
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetService, GetService method [Core Audio], GetService method [Core Audio],ISpatialAudioObjectRenderStreamBase interface, ISpatialAudioObjectRenderStreamBase interface [Core Audio],GetService method, ISpatialAudioObjectRenderStreamBase.GetService, ISpatialAudioObjectRenderStreamBase::GetService, coreaudio.ispatialaudioobjectrenderstream_getservice, spatialaudioclient/ISpatialAudioObjectRenderStreamBase::GetService
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: spatialaudioclient.h
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
 - spatialaudioclient.h
api_name:
 - ISpatialAudioObjectRenderStreamBase.GetService
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISpatialAudioObjectRenderStreamBase::GetService


## -description


Gets additional services from the <b>ISpatialAudioObjectRenderStream</b>.


## -parameters




### -param riid [in]

The interface ID for the requested service. The client should set this parameter to one of the following REFIID values:

IID_IAudioClock

IID_IAudioClock2

IID_IAudioStreamVolume


### -param service [out]

Pointer to a pointer variable into which the method writes the address of an instance of the requested interface. Through this method, the caller obtains a counted reference to the interface. The caller is responsible for releasing the interface, when it is no longer needed, by calling the interface's <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> method. If the <b>GetService</b> call fails, <i>*ppv </i>is NULL.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Parameter <i>ppv</i> is NULL.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AUDCLNT_E_DEVICE_INVALIDATED</b></dt>
</dl>
</td>
<td width="60%">
The audio endpoint device has been unplugged, or the audio hardware or associated hardware resources have been reconfigured, disabled, removed, or otherwise made unavailable for use.

</td>
</tr>
</table>
 




## -remarks



The <b>GetService</b> method supports the following service interfaces:

<ul>
<li>
<a href="https://msdn.microsoft.com/dbec9468-b555-42a0-a988-dec3a66c9f96">IAudioClock</a>
</li>
<li>
<a href="https://msdn.microsoft.com/4820c93a-a5d8-4ab9-aefc-9377fc76e745">IAudioClock2</a>
</li>
<li>
<a href="https://msdn.microsoft.com/92cc127b-77ac-4fc7-ac3c-319e5d6368d3">IAudioStreamVolume</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/B4D10CC6-62BF-4D20-910F-E39DF812010D">ISpatialAudioObjectRenderStream</a>



<a href="https://msdn.microsoft.com/2C2BE871-EFD1-40E1-B466-6BBD09C56852">ISpatialAudioObjectRenderStreamBase</a>
 

 

