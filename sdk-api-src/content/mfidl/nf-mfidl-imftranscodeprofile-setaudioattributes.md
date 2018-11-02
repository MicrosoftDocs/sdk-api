---
UID: NF:mfidl.IMFTranscodeProfile.SetAudioAttributes
title: IMFTranscodeProfile::SetAudioAttributes
author: windows-sdk-content
description: Sets audio stream configuration settings in the transcode profile.
old-location: mf\imftranscodeprofile_setaudioattributes.htm
tech.root: medfound
ms.assetid: 4118bb2b-8373-434a-896b-de5a1ba8c793
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IMFTranscodeProfile interface [Media Foundation],SetAudioAttributes method, IMFTranscodeProfile.SetAudioAttributes, IMFTranscodeProfile::SetAudioAttributes, SetAudioAttributes, SetAudioAttributes method [Media Foundation], SetAudioAttributes method [Media Foundation],IMFTranscodeProfile interface, mf.imftranscodeprofile_setaudioattributes, mfidl/IMFTranscodeProfile::SetAudioAttributes
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - mfidl.h
api_name:
 - IMFTranscodeProfile.SetAudioAttributes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFTranscodeProfile::SetAudioAttributes


## -description


Sets audio stream configuration settings  in the transcode profile.

To get a list of compatible audio media types supported by the Media Foundation transform (MFT) encoder , call  <a href="https://msdn.microsoft.com/8750eacb-7e6f-4c17-987b-f4baa4eea847">MFTranscodeGetAudioOutputAvailableTypes</a>. You can get the attributes that are set on the required media type and set them on the transcode profile. To set the audio attributes properly, create a new attribute store and copy the attribute store from the required media media type by calling <a href="https://msdn.microsoft.com/111b55bc-fb8e-45b5-a709-703acd23c4be">IMFAttributes::CopyAllItems</a>. This makes sure that the caller does not hold the references to the media type retrieved from the encoder. For example code, see <a href="https://msdn.microsoft.com/2a482c6f-6e20-419a-a7eb-085c41cc8186">MFCreateTranscodeProfile</a>.


## -parameters




### -param pAttrs [in]

Pointer to the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> interface of an attribute store that contains the configuration settings for the audio stream. The specified attribute values overwrite any existing values stored in the transcode profile. 

The following audio attributes can be set:

<ul>
<li>
<a href="https://msdn.microsoft.com/15aad4ea-7b4b-4a6f-bac7-18e0c281f2a6">Audio Media Types</a>
</li>
<li>
<a href="https://msdn.microsoft.com/73f23aed-d1b9-4821-b1ca-0a07f02b6913">MF_TRANSCODE_DONOT_INSERT_ENCODER</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9a6b6402-ff53-4399-8616-06b7768a8737">MF_TRANSCODE_ENCODINGPROFILE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/872140e8-fd39-446c-a84f-1e04ea95076e">MF_TRANSCODE_QUALITYVSSPEED</a>
</li>
</ul>
To create the attribute store, call <a href="https://msdn.microsoft.com/a79b1edd-5ca1-4550-a6ce-58073155affd">MFCreateAttributes</a>. To set a specific attribute value in the attribute store, the caller must call the appropriate <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> methods depending on the data type of the attribute.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/44af5e03-5f0a-4564-b9d6-b8c935df35b2">Attributes in Media Foundation</a>



<a href="https://msdn.microsoft.com/82e012e0-84d8-4791-8b6f-bda58b498a90">IMFTranscodeProfile</a>



<a href="https://msdn.microsoft.com/24bf68a8-39bf-4302-b28c-71bb23b63469">Transcode API</a>
 

 

