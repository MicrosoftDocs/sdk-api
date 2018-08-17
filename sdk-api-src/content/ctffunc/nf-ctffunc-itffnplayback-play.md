---
UID: NF:ctffunc.ITfFnPlayBack.Play
title: ITfFnPlayBack::Play
author: windows-sdk-content
description: ITfFnPlayBack::Play method
old-location: tsf\itffnplayback_play.htm
old-project: TSF
ms.assetid: 9945bc65-fe9f-42d1-ade1-db016dc7489c
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITfFnPlayBack interface [Text Services Framework],Play method, ITfFnPlayBack.Play, ITfFnPlayBack::Play, Play, Play method [Text Services Framework], Play method [Text Services Framework],ITfFnPlayBack interface, _tsf_itffnplayback_play_ref, ctffunc/ITfFnPlayBack::Play, tsf.itffnplayback_play
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: ctffunc.h
req.include-header: 
req.redist: TSF 1.0 on Windows 2000 Professional
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
tech.root: 
req.typenames: TfIntegratableCandidateListSelectionStyle
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfFnPlayBack.Play
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
---

# ITfFnPlayBack::Play


## -description




## -parameters




### -param pRange [in]

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/ms628908(v=VS.85).aspx">ITfRange</a> object that covers the text to play the audio data for. This range object is obtained by calling <a href="https://msdn.microsoft.com/en-us/library/ms538962(v=VS.85).aspx">ITfFnPlayBack::QueryRange</a>.

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




<a href="https://msdn.microsoft.com/en-us/library/ms538958(v=VS.85).aspx">ITfFnPlayBack</a>



<a href="https://msdn.microsoft.com/d6113703-5515-4f1a-8e2e-1373077dafc2">ITfFnPlayBack::QueryRange
      </a>



<a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange
      </a>
 

 

