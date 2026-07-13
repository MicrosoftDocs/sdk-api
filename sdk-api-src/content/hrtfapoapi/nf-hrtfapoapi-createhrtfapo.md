---
UID: NF:hrtfapoapi.CreateHrtfApo
title: CreateHrtfApo function (hrtfapoapi.h)
description: Creates an instance of the IXAPO interface for head-related transfer function (HRTF) processing.
helpviewer_keywords: ["CreateHrtfApo","CreateHrtfApo function [XAudio2 Audio Mixing APIs]","hrtfapoapi/CreateHrtfApo","xaudio2.createhrtfapo"]
old-location: xaudio2\createhrtfapo.htm
tech.root: xaudio2
ms.assetid: 24E3CD0D-FC0D-4B1B-961F-BE48935F7B71
ms.date: 12/05/2018
ms.keywords: CreateHrtfApo, CreateHrtfApo function [XAudio2 Audio Mixing APIs], hrtfapoapi/CreateHrtfApo, xaudio2.createhrtfapo
req.header: hrtfapoapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: hrtfapo.lib
req.dll: HrtfApo.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreateHrtfApo
 - hrtfapoapi/CreateHrtfApo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - HrtfApo.dll
api_name:
 - CreateHrtfApo
---

# CreateHrtfApo function


## -description

Creates an instance of the <a href="/windows/desktop/api/xapo/nn-xapo-ixapo">IXAPO</a> interface for head-related transfer function (HRTF) processing.

## -parameters

### -param init [in]

Pointer to an <a href="/windows/desktop/api/hrtfapoapi/ns-hrtfapoapi-hrtfapoinit">HrtfApoInit</a> struct. Specifies parameters for XAPO interface initialization.

### -param xApo [out]

The new instance of the <a href="/windows/desktop/api/xapo/nn-xapo-ixapo">IXAPO</a> interface.

## -returns

This function can return the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
An instance of the XAPO object was created successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
HRTF is not supported on the current platform. 

</td>
</tr>
</table>

## -remarks

Audio is processed in blocks of 1024 samples.

Format requirements:

<ul>
<li>Input: mono, 48 kHz, 32-bit float PCM.</li>
<li>Output: stereo, 48 kHz, 32-bit float PCM.</li>
</ul>
The source and environment parameters of the HRTF XAPO are controlled through the <a href="/windows/desktop/api/hrtfapoapi/nn-hrtfapoapi-ixapohrtfparameters">IXAPOHrtfParameters</a> interface.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9);

## -see-also

<a href="/windows/desktop/xaudio2/functions">Functions</a>



<a href="/windows/desktop/api/xapo/nn-xapo-ixapo">IXAPO</a>