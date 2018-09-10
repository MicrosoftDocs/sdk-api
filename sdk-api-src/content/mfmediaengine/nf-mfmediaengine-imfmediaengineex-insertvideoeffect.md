---
UID: NF:mfmediaengine.IMFMediaEngineEx.InsertVideoEffect
title: IMFMediaEngineEx::InsertVideoEffect
author: windows-sdk-content
description: Inserts a video effect.
old-location: mf\imfmediaengineex_insertvideoeffect.htm
tech.root: medfound
ms.assetid: 7F59BE62-D3F1-4C5A-94FD-F864342797BF
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: FALSE, IMFMediaEngineEx interface [Media Foundation],InsertVideoEffect method, IMFMediaEngineEx.InsertVideoEffect, IMFMediaEngineEx::InsertVideoEffect, InsertVideoEffect, InsertVideoEffect method [Media Foundation], InsertVideoEffect method [Media Foundation],IMFMediaEngineEx interface, TRUE, mf.imfmediaengineex_insertvideoeffect, mfmediaengine/IMFMediaEngineEx::InsertVideoEffect
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFMediaEngineEx.InsertVideoEffect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaEngineEx::InsertVideoEffect


## -description


Inserts a video effect.


## -parameters




### -param pEffect [in]

One of the following: 

<ul>
<li>A pointer to the <a href="https://msdn.microsoft.com/3cc502d8-d364-43b9-b0b6-d9474c002b20">IMFTransform</a> interface of a Media Foundation transform (MFT) that implements the video effect.</li>
<li>A pointer to the <a href="https://msdn.microsoft.com/c0936e3c-3cd1-4c1e-a336-2dee7d943963">IMFActivate</a> interface of an activation object. The activation object must create an MFT for the video effect.</li>
</ul>

### -param fOptional [in]

Specifies whether the effect is optional.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b><b>TRUE</b></b></dt>
</dl>
</td>
<td width="60%">
The effect is optional. If the Media Engine cannot add the effect, it ignores the effect and  continues playback.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b><b>FALSE</b></b></dt>
</dl>
</td>
<td width="60%">
The effect is required. If the Media Engine object cannot add the effect, a playback error occurs.

</td>
</tr>
</table>
 


## -returns



This method can return one of these values.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
The maximum number of video effects was reached.

</td>
</tr>
</table>
 




## -remarks



The effect is applied when the next media resource is loaded.




## -see-also




<a href="https://msdn.microsoft.com/EE3591FD-4FE8-4F20-A4E2-52C896229571">IMFMediaEngineEx</a>
 

 

