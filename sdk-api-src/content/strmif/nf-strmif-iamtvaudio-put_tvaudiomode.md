---
UID: NF:strmif.IAMTVAudio.put_TVAudioMode
title: IAMTVAudio::put_TVAudioMode (strmif.h)
description: The put_TVAudioMode method sets the current TV audio mode.
helpviewer_keywords: ["IAMTVAudio interface [DirectShow]","put_TVAudioMode method","IAMTVAudio.put_TVAudioMode","IAMTVAudio::put_TVAudioMode","IAMTVAudioput_TVAudioMode","dshow.iamtvaudio_put_tvaudiomode","put_TVAudioMode","put_TVAudioMode method [DirectShow]","put_TVAudioMode method [DirectShow]","IAMTVAudio interface","strmif/IAMTVAudio::put_TVAudioMode"]
old-location: dshow\iamtvaudio_put_tvaudiomode.htm
tech.root: dshow
ms.assetid: 7efe43af-db07-4286-b0b7-6527403568f0
ms.date: 12/05/2018
ms.keywords: IAMTVAudio interface [DirectShow],put_TVAudioMode method, IAMTVAudio.put_TVAudioMode, IAMTVAudio::put_TVAudioMode, IAMTVAudioput_TVAudioMode, dshow.iamtvaudio_put_tvaudiomode, put_TVAudioMode, put_TVAudioMode method [DirectShow], put_TVAudioMode method [DirectShow],IAMTVAudio interface, strmif/IAMTVAudio::put_TVAudioMode
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMTVAudio::put_TVAudioMode
 - strmif/IAMTVAudio::put_TVAudioMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMTVAudio.put_TVAudioMode
---

# IAMTVAudio::put_TVAudioMode


## -description

The <code>put_TVAudioMode</code> method sets the current TV audio mode.

## -parameters

### -param lMode [in]

A [TVAudioMode](/windows/desktop/api/strmif/ne-strmif-tvaudiomode) enumeration value that identifies the audio mode.

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

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamtvaudio">IAMTVAudio Interface</a>