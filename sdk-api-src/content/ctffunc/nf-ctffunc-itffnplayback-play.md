---
UID: NF:ctffunc.ITfFnPlayBack.Play
title: ITfFnPlayBack::Play (ctffunc.h)
description: ITfFnPlayBack::Play method
helpviewer_keywords: ["ITfFnPlayBack interface [Text Services Framework]","Play method","ITfFnPlayBack.Play","ITfFnPlayBack::Play","Play","Play method [Text Services Framework]","Play method [Text Services Framework]","ITfFnPlayBack interface","_tsf_itffnplayback_play_ref","ctffunc/ITfFnPlayBack::Play","tsf.itffnplayback_play"]
old-location: tsf\itffnplayback_play.htm
tech.root: TSF
ms.assetid: 9945bc65-fe9f-42d1-ade1-db016dc7489c
ms.date: 12/05/2018
ms.keywords: ITfFnPlayBack interface [Text Services Framework],Play method, ITfFnPlayBack.Play, ITfFnPlayBack::Play, Play, Play method [Text Services Framework], Play method [Text Services Framework],ITfFnPlayBack interface, _tsf_itffnplayback_play_ref, ctffunc/ITfFnPlayBack::Play, tsf.itffnplayback_play
req.header: ctffunc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctffunc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfFnPlayBack::Play
 - ctffunc/ITfFnPlayBack::Play
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfFnPlayBack.Play
---

# ITfFnPlayBack::Play


## -description

Causes the audio data for a range of text to be played.

## -parameters

### -param pRange [in]

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange</a> object that covers the text to play the audio data for. This range object is obtained by calling <a href="/windows/desktop/api/ctffunc/nf-ctffunc-itffnplayback-queryrange">ITfFnPlayBack::QueryRange</a>.

If the range has zero length, the range played is expanded to cover the entire spoken phrase. If the range has a nonzero length, the range played is expanded to include the entire word, or words, that the range partially covers.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/ctffunc/nn-ctffunc-itffnplayback">ITfFnPlayBack</a>



<a href="/windows/desktop/api/ctffunc/nf-ctffunc-itffnplayback-queryrange">ITfFnPlayBack::QueryRange
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange
      </a>