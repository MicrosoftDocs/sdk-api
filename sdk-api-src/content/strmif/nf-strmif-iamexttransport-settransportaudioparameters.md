---
UID: NF:strmif.IAMExtTransport.SetTransportAudioParameters
title: IAMExtTransport::SetTransportAudioParameters
author: windows-driver-content
description: The SetTransportAudioParameters assigns audio parameter settings for external transport.
old-location: dshow\iamexttransport_settransportaudioparameters.htm
old-project: DirectShow
ms.assetid: e013dd73-7276-48b3-bf5f-ffb4b3d49419
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: IAMExtTransport interface [DirectShow],SetTransportAudioParameters method, IAMExtTransport.SetTransportAudioParameters, IAMExtTransport::SetTransportAudioParameters, IAMExtTransportSetTransportAudioParameters, SetTransportAudioParameters, SetTransportAudioParameters method [DirectShow], SetTransportAudioParameters method [DirectShow],IAMExtTransport interface, dshow.iamexttransport_settransportaudioparameters, strmif/IAMExtTransport::SetTransportAudioParameters
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	IAMExtTransport.SetTransportAudioParameters
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMExtTransport::SetTransportAudioParameters


## -description



The <code>SetTransportAudioParameters</code> assigns audio parameter settings for external transport.



This method is not implemented.


## -parameters




### -param Param [in]

Specifies the audio parameter you want to set as a <b>long</b> integer.

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>ED_TRANSAUDIO_ENABLE_OUTPUT</td>
<td>Enable audio channel(s) for output.</td>
</tr>
<tr>
<td>ED_TRANSAUDIO_ENABLE_RECORD</td>
<td>Enable audio channel(s) for recording.</td>
</tr>
<tr>
<td>ED_TRANSAUDIO_ENABLE_SELSYNC</td>
<td>Enable audio channel(s) for selsync recording.</td>
</tr>
<tr>
<td>ED_TRANSAUDIO_SET_MONITOR</td>
<td>Set the monitor output source.</td>
</tr>
<tr>
<td>ED_TRANSAUDIO_SET_SOURCE</td>
<td>Set the active audio input.</td>
</tr>
</table>
 


### -param Value [in]

Specifies which audio channel or channels is assigned the parameter as a <b>long</b> integer.


## -returns



When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.




## -remarks



Specify an exact channel or channels in <i>Value</i> by selecting ED_AUDIO_1 through ED_AUDIO_24 (use a bitwise OR to combine), or all channels by selecting ED_AUDIO_ALL.

<h3><a id="DV_Implementation"></a><a id="dv_implementation"></a><a id="DV_IMPLEMENTATION"></a>DV Implementation</h3>

<a href="https://msdn.microsoft.com/146ca753-fe41-49d3-8b1c-077e10a28192">MSDV</a> does not support this method. It returns E_NOTIMPL.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/4ce48038-bfcf-4b1f-8053-3446929a5f06">IAMExtTransport Interface</a>



<a href="https://msdn.microsoft.com/90650920-f151-4e19-9133-4f1eb5eecbc2">IAMExtTransport::GetTransportAudioParameters</a>
 

 

