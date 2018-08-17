---
UID: NF:hrtfapoapi.CreateHrtfApo
title: CreateHrtfApo function
author: windows-sdk-content
description: Creates an instance of the IXAPO interface for head-related transfer function (HRTF) processing.
old-location: xaudio2\createhrtfapo.htm
old-project: xaudio2
ms.assetid: 24E3CD0D-FC0D-4B1B-961F-BE48935F7B71
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CreateHrtfApo, CreateHrtfApo function [XAudio2 Audio Mixing APIs], hrtfapoapi/CreateHrtfApo, xaudio2.createhrtfapo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: hrtfapoapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: HrtfEnvironment
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - HrtfApo.dll
api_name:
 - CreateHrtfApo
product: Windows
targetos: Windows
req.lib: 
req.dll: HrtfApo.dll
req.irql: 
req.product: GDI+ 1.1
---

# CreateHrtfApo function


## -description


Creates an instance of the <a href="https://msdn.microsoft.com/en-us/library/Ee415893(v=VS.85).aspx">IXAPO</a> interface for head-related transfer function (HRTF) processing.


## -parameters




### -param init [in]

Pointer to an <a href="https://msdn.microsoft.com/686A2203-A991-427F-9D41-F3C679070127">HrtfApoInit</a> struct. Specifies parameters for XAPO interface initialization.


### -param xApo [out]

The new instance of the <a href="https://msdn.microsoft.com/en-us/library/Ee415893(v=VS.85).aspx">IXAPO</a> interface.


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
The source and environment parameters of the HRTF XAPO are controlled through the <a href="https://msdn.microsoft.com/EDA29173-84B5-4D2F-90B0-546EEEC49539">IXAPOHrtfParameters</a> interface.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); 




## -see-also




<a href="https://msdn.microsoft.com/870a0425-3226-7848-bcc0-0ba7145135cb">Functions</a>



<a href="https://msdn.microsoft.com/en-us/library/Ee415893(v=VS.85).aspx">IXAPO</a>
 

 

