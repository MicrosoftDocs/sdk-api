---
UID: NF:mfobjects.IMFAudioMediaType.GetAudioFormat
title: IMFAudioMediaType::GetAudioFormat
author: windows-sdk-content
description: GetAudioFormat is no longer available for use as of Windows 7.
old-location: mf\imfaudiomediatype_getaudioformat.htm
tech.root: medfound
ms.assetid: 6a874e7b-9358-45e1-85be-7207bf46d93e
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: 6a874e7b-9358-45e1-85be-7207bf46d93e, GetAudioFormat, GetAudioFormat method [Media Foundation], GetAudioFormat method [Media Foundation],IMFAudioMediaType interface, IMFAudioMediaType interface [Media Foundation],GetAudioFormat method, IMFAudioMediaType.GetAudioFormat, IMFAudioMediaType::GetAudioFormat, mf.imfaudiomediatype_getaudioformat, mfobjects/IMFAudioMediaType::GetAudioFormat
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFAudioMediaType.GetAudioFormat
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFAudioMediaType::GetAudioFormat


## -description


<p class="CCE_Message">[<b>GetAudioFormat</b> is no longer available for use as of Windows 7. Instead, use the media type attributes to get the properties of the audio format.]

Returns a pointer to a <a href="https://msdn.microsoft.com/4f3bf6fb-b15f-43b3-82f1-e7a8a3007057">WAVEFORMATEX</a> structure that describes the audio format.


## -parameters






## -returns



This method returns a pointer to a <a href="https://msdn.microsoft.com/4f3bf6fb-b15f-43b3-82f1-e7a8a3007057">WAVEFORMATEX</a> structure.




## -remarks



If you need to convert the media type into a <a href="https://msdn.microsoft.com/4f3bf6fb-b15f-43b3-82f1-e7a8a3007057">WAVEFORMATEX</a> structure, call <a href="https://msdn.microsoft.com/b124bac2-90de-4358-a079-f509a89c3776">MFCreateWaveFormatExFromMFMediaType</a>.

There are no guarantees about how long the returned pointer is valid.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/15aad4ea-7b4b-4a6f-bac7-18e0c281f2a6">Audio Media Types</a>



<a href="https://msdn.microsoft.com/425a4a37-6fd3-4724-9d18-c39cc2862ef7">IMFAudioMediaType</a>



<a href="https://msdn.microsoft.com/690fda6e-dcbd-44dc-968d-cc949126da81">Media Types</a>
 

 

