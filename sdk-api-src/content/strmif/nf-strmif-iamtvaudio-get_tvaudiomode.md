---
UID: NF:strmif.IAMTVAudio.get_TVAudioMode
title: IAMTVAudio::get_TVAudioMode method
author: windows-driver-content
description: The get_TVAudioMode method retrieves the current TV audio mode.
old-location: dshow\iamtvaudio_get_tvaudiomode.htm
old-project: DirectShow
ms.assetid: fa2e71f3-3aa0-4260-925d-579006459a09
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IAMTVAudio, IAMTVAudio interface [DirectShow], get_TVAudioMode method, IAMTVAudio::get_TVAudioMode, IAMTVAudioget_TVAudioMode, dshow.iamtvaudio_get_tvaudiomode, get_TVAudioMode method [DirectShow], get_TVAudioMode method [DirectShow], IAMTVAudio interface, get_TVAudioMode,IAMTVAudio.get_TVAudioMode, strmif/IAMTVAudio::get_TVAudioMode
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IAMTVAudio.get_TVAudioMode
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMTVAudio::get_TVAudioMode method


## -description



The <code>get_TVAudioMode</code> method retrieves the current TV audio mode.




## -parameters




### -param plMode






#### - plModes [out]

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
 

 

