---
UID: NF:strmif.IAMTVAudio.GetHardwareSupportedTVAudioModes
title: IAMTVAudio::GetHardwareSupportedTVAudioModes
author: windows-sdk-content
description: The GetHardwareSupportedTVAudioModes method retrieves a bitmask of the formats available in the hardware.
old-location: dshow\iamtvaudio_gethardwaresupportedtvaudiomodes.htm
tech.root: DirectShow
ms.assetid: 2c67abc9-2419-473b-a2e6-4fc7df50752c
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: GetHardwareSupportedTVAudioModes, GetHardwareSupportedTVAudioModes method [DirectShow], GetHardwareSupportedTVAudioModes method [DirectShow],IAMTVAudio interface, IAMTVAudio interface [DirectShow],GetHardwareSupportedTVAudioModes method, IAMTVAudio.GetHardwareSupportedTVAudioModes, IAMTVAudio::GetHardwareSupportedTVAudioModes, IAMTVAudioGetHardwareSupportedTVAudioModes, dshow.iamtvaudio_gethardwaresupportedtvaudiomodes, strmif/IAMTVAudio::GetHardwareSupportedTVAudioModes
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMTVAudio.GetHardwareSupportedTVAudioModes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMTVAudio::GetHardwareSupportedTVAudioModes


## -description



The <code>GetHardwareSupportedTVAudioModes</code> method retrieves a bitmask of the formats available in the hardware.




## -parameters




### -param plModes [out]

Pointer to a <a href="https://msdn.microsoft.com/70e26550-0a8f-484e-b919-cfefdcf95f6b">TVAudioMode</a> enumeration value that identifies the audio mode.


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation. <b>HRESULT</b> can be one of the following standard constants, or other values not listed.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Method isn't supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK or NOERROR</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/de340594-4410-4896-b206-0f47d4035bc1">IAMTVAudio Interface</a>
 

 

