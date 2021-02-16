---
UID: NF:vfw.IAVIStream.FindSample
title: IAVIStream::FindSample (vfw.h)
description: The FindSample method obtains the position in a stream of a key frame or a nonempty frame. Called when an application uses the AVIStreamFindSample function.
helpviewer_keywords: ["FindSample","FindSample method [Windows Multimedia]","FindSample method [Windows Multimedia]","IAVIStream interface","IAVIStream interface [Windows Multimedia]","FindSample method","IAVIStream.FindSample","IAVIStream::FindSample","_win32_IAVIStream_FindSample","multimedia.iavistream_findsample","vfw/IAVIStream::FindSample"]
old-location: multimedia\iavistream_findsample.htm
tech.root: Multimedia
ms.assetid: 77927e6c-beee-4774-b727-5cd608cefb3d
ms.date: 12/05/2018
ms.keywords: FindSample, FindSample method [Windows Multimedia], FindSample method [Windows Multimedia],IAVIStream interface, IAVIStream interface [Windows Multimedia],FindSample method, IAVIStream.FindSample, IAVIStream::FindSample, _win32_IAVIStream_FindSample, multimedia.iavistream_findsample, vfw/IAVIStream::FindSample
req.header: vfw.h
req.include-header: 
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
req.lib: Vfw32.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAVIStream::FindSample
 - vfw/IAVIStream::FindSample
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Vfw32.lib
 - Vfw32.dll
api_name:
 - IAVIStream.FindSample
---

# IAVIStream::FindSample


## -description

The <b>FindSample</b> method obtains the position in a stream of a key frame or a nonempty frame. Called when an application uses the <a href="/windows/desktop/api/vfw/nf-vfw-avistreamfindsample">AVIStreamFindSample</a> function.

## -parameters

### -param lPos

Position of the sample or frame.

### -param lFlags

Applicable flags. The following values are defined.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>FIND_ANY</td>
<td>Searches for a nonempty frame.</td>
</tr>
<tr>
<td>FIND_FORMAT</td>
<td>Searches for a format change.</td>
</tr>
<tr>
<td>FIND_KEY</td>
<td>Searches for a key frame.</td>
</tr>
<tr>
<td>FIND_NEXT</td>
<td>Searches forward through a stream, beginning with the current frame.</td>
</tr>
<tr>
<td>FIND_PREV</td>
<td>Searches backward through a stream, beginning with the current frame.</td>
</tr>
</table>
 

The FIND_ANY, FIND_KEY, and FIND_FORMAT flags are mutually exclusive, as are the FIND_NEXT and FIND_PREV flags. You must specify one value from each group.


#### - ps

Pointer to the interface to a stream.

## -returns

Returns the location of the key frame corresponding to the frame specified by the application.

## -remarks

If key frames are not significant in your custom format, return the position specified for <i>lPos</i>.

For handlers written in C++, <b>FindSample</b> has the following syntax:


```cpp

LONG FindSample(LONG lPos, LONG lFlags) 
 

```

## -see-also

<a href="/windows/desktop/Multimedia/custom-file-and-stream-handler-interfaces">Custom File and Stream Handler Interfaces</a>



<a href="/windows/desktop/Multimedia/custom-file-and-stream-handlers">Custom File and Stream Handlers</a>