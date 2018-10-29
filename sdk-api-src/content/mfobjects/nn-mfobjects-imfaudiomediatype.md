---
UID: NN:mfobjects.IMFAudioMediaType
title: IMFAudioMediaType
author: windows-sdk-content
description: IMFAudioMediaType is no longer available for use as of Windows 7.
old-location: mf\imfaudiomediatype.htm
tech.root: medfound
ms.assetid: 425a4a37-6fd3-4724-9d18-c39cc2862ef7
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: 425a4a37-6fd3-4724-9d18-c39cc2862ef7, IMFAudioMediaType, IMFAudioMediaType interface [Media Foundation], IMFAudioMediaType interface [Media Foundation],described, mf.imfaudiomediatype, mfobjects/IMFAudioMediaType
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - IMFAudioMediaType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFAudioMediaType interface


## -description


<p class="CCE_Message">[<b>IMFAudioMediaType</b> is no longer available for use as of Windows 7. Instead, use the media type attributes to get the properties of the audio format.]

Represents a description of an audio format.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFAudioMediaType</b> interface inherits from <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a>. <b>IMFAudioMediaType</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFAudioMediaType</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6a874e7b-9358-45e1-85be-7207bf46d93e">GetAudioFormat</a>
</td>
<td align="left" width="63%">
Returns a pointer to a <a href="https://msdn.microsoft.com/4f3bf6fb-b15f-43b3-82f1-e7a8a3007057">WAVEFORMATEX</a> structure that describes the audio format.
        

</td>
</tr>
</table> 


## -remarks



<b>Windows Server 2008 and Windows Vista:  </b>If the major type of a media type is <b>MFMediaType_Audio</b>, you can query the media type object for the <b>IMFAudioMediaType</b> interface.

To convert an audio media type into a <a href="https://msdn.microsoft.com/4f3bf6fb-b15f-43b3-82f1-e7a8a3007057">WAVEFORMATEX</a> structure, call <a href="https://msdn.microsoft.com/b124bac2-90de-4358-a079-f509a89c3776">MFCreateWaveFormatExFromMFMediaType</a>.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/e84ba3f6-4857-4340-baca-5847650ea7b8">Media Type Attributes</a>



<a href="https://msdn.microsoft.com/690fda6e-dcbd-44dc-968d-cc949126da81">Media Types</a>
 

 

