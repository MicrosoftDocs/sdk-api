---
UID: NF:tapi3if.ITScriptableAudioFormat.put_Channels
title: ITScriptableAudioFormat::put_Channels (tapi3if.h)
author: windows-sdk-content
description: The put_Channels method sets the nChannels member in the WAVEFORMATEX structure.
old-location: tapi3\itscriptableaudioformat_put_channels.htm
tech.root: Tapi
ms.assetid: 301fd17f-393b-46dd-9d76-1a1e34547629
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITScriptableAudioFormat interface [TAPI 2.2],put_Channels method, ITScriptableAudioFormat.put_Channels, ITScriptableAudioFormat::put_Channels, _tapi3_itscriptableaudioformat_put_channels, put_Channels, put_Channels method [TAPI 2.2], put_Channels method [TAPI 2.2],ITScriptableAudioFormat interface, tapi3.itscriptableaudioformat_put_channels, tapi3if/ITScriptableAudioFormat::put_Channels
ms.topic: method
f1_keywords: ["tapi3if/ITScriptableAudioFormat.put_Channels"]
req.header: tapi3if.h
req.include-header: Tapi3.h
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITScriptableAudioFormat.put_Channels
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITScriptableAudioFormat::put_Channels


## -description


The 
<b>put_Channels</b> method sets the <b>nChannels</b> member in the 
<a href="https://docs.microsoft.com/previous-versions//dd757713(v=vs.85)">WAVEFORMATEX</a> structure.


## -parameters




### -param nNewVal [in]

New value for the <b>nChannels</b> member in the 
<a href="https://docs.microsoft.com/previous-versions//dd757713(v=vs.85)">WAVEFORMATEX</a> structure.


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
Method succeeded.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itscriptableaudioformat">ITScriptableAudioFormat</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itscriptableaudioformat-get_channels">get_Channels</a>
 

 

