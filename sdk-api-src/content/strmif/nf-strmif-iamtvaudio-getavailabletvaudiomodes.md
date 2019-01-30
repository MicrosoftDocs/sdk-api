---
UID: NF:strmif.IAMTVAudio.GetAvailableTVAudioModes
title: IAMTVAudio::GetAvailableTVAudioModes
author: windows-sdk-content
description: The GetAvailableTVAudioModes method retrieves a bitmask of the possible modes.
old-location: dshow\iamtvaudio_getavailabletvaudiomodes.htm
tech.root: DirectShow
ms.assetid: c64dc038-7ebf-4aa4-a7ae-b3eb0e8eaf1a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetAvailableTVAudioModes, GetAvailableTVAudioModes method [DirectShow], GetAvailableTVAudioModes method [DirectShow],IAMTVAudio interface, IAMTVAudio interface [DirectShow],GetAvailableTVAudioModes method, IAMTVAudio.GetAvailableTVAudioModes, IAMTVAudio::GetAvailableTVAudioModes, IAMTVAudioGetAvailableTVAudioModes, dshow.iamtvaudio_getavailabletvaudiomodes, strmif/IAMTVAudio::GetAvailableTVAudioModes
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
 - IAMTVAudio.GetAvailableTVAudioModes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMTVAudio::GetAvailableTVAudioModes


## -description



The <code>GetAvailableTVAudioModes</code> method retrieves a bitmask of the possible modes.




## -parameters




### -param plModes [out]

Pointer to a <a href="https://msdn.microsoft.com/70e26550-0a8f-484e-b919-cfefdcf95f6b">TVAudioMode</a> enumeration type, identifying the audio mode.


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
Null pointer argument.

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
 

 

