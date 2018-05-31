---
UID: NF:strmif.IAMTVAudio.put_TVAudioMode
title: IAMTVAudio::put_TVAudioMode
author: windows-sdk-content
description: The put_TVAudioMode method sets the current TV audio mode.
old-location: dshow\iamtvaudio_put_tvaudiomode.htm
old-project: DirectShow
ms.assetid: 7efe43af-db07-4286-b0b7-6527403568f0
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IAMTVAudio interface [DirectShow],put_TVAudioMode method, IAMTVAudio.put_TVAudioMode, IAMTVAudio::put_TVAudioMode, IAMTVAudioput_TVAudioMode, dshow.iamtvaudio_put_tvaudiomode, put_TVAudioMode, put_TVAudioMode method [DirectShow], put_TVAudioMode method [DirectShow],IAMTVAudio interface, strmif/IAMTVAudio::put_TVAudioMode
ms.prod: windows
ms.technology: windows-sdk
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
-	IAMTVAudio.put_TVAudioMode
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMTVAudio::put_TVAudioMode


## -description



The <code>put_TVAudioMode</code> method sets the current TV audio mode.




## -parameters




### -param lMode






#### - plModes [in]

A <a href="https://msdn.microsoft.com/70e26550-0a8f-484e-b919-cfefdcf95f6b">TVAudioMode</a> enumeration value that identifies the audio mode.


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
 

 

