---
UID: NF:mfmediaengine.IMFMediaEngineEx.SetStreamSelection
title: IMFMediaEngineEx::SetStreamSelection
author: windows-sdk-content
description: Selects or deselects a stream for playback.
old-location: mf\imfmediaengineex_setstreamselection.htm
tech.root: medfound
ms.assetid: 12F0FDD0-0D8C-496D-B5C4-3FBCBCAAC6FB
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: FALSE, IMFMediaEngineEx interface [Media Foundation],SetStreamSelection method, IMFMediaEngineEx.SetStreamSelection, IMFMediaEngineEx::SetStreamSelection, SetStreamSelection, SetStreamSelection method [Media Foundation], SetStreamSelection method [Media Foundation],IMFMediaEngineEx interface, TRUE, mf.imfmediaengineex_setstreamselection, mfmediaengine/IMFMediaEngineEx::SetStreamSelection
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
 - IMFMediaEngineEx.SetStreamSelection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaEngineEx::SetStreamSelection


## -description


Selects or deselects a stream for playback.




## -parameters




### -param dwStreamIndex [in]

The zero-based index of the stream. To get the number of streams, call <a href="https://msdn.microsoft.com/7F3E805A-FE5C-4B75-9333-AE9819CFAFFA">IMFMediaEngineEx::GetNumberOfStreams</a>.


### -param Enabled [in]

Specifies whether to select or deselect the stream.

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
The stream is selected. During playback, this stream will play.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b><b>FALSE</b></b></dt>
</dl>
</td>
<td width="60%">
The stream is not selected. During playback, this stream will not play.

</td>
</tr>
</table>
 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/EE3591FD-4FE8-4F20-A4E2-52C896229571">IMFMediaEngineEx</a>
 

 

