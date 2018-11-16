---
UID: NF:strmif.IAMExtTransport.GetTransportAudioParameters
title: IAMExtTransport::GetTransportAudioParameters
author: windows-sdk-content
description: The GetTransportAudioParameters method retrieves audio parameter setting for external transport.
old-location: dshow\iamexttransport_gettransportaudioparameters.htm
tech.root: DirectShow
ms.assetid: 90650920-f151-4e19-9133-4f1eb5eecbc2
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetTransportAudioParameters, GetTransportAudioParameters method [DirectShow], GetTransportAudioParameters method [DirectShow],IAMExtTransport interface, IAMExtTransport interface [DirectShow],GetTransportAudioParameters method, IAMExtTransport.GetTransportAudioParameters, IAMExtTransport::GetTransportAudioParameters, IAMExtTransportGetTransportAudioParameters, dshow.iamexttransport_gettransportaudioparameters, strmif/IAMExtTransport::GetTransportAudioParameters
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMExtTransport.GetTransportAudioParameters
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- strmif.h
: 
- IAMExtTransport.GetTransportAudioParameters
: 
---

# IAMExtTransport::GetTransportAudioParameters


## -description



The <code>GetTransportAudioParameters</code> method retrieves audio parameter setting for external transport.



This method is not implemented.


## -parameters




### -param Param [in]

Specifies the audio parameter, whose value you want receive, as a <b>long</b> integer containing one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>ED_TRANSAUDIO_ENABLE_OUTPUT</td>
<td>Audio output channel(s)</td>
</tr>
<tr>
<td>ED_TRANSAUDIO_ENABLE_RECORD</td>
<td>Audio recording channel(s)</td>
</tr>
<tr>
<td>ED_TRANSAUDIO_ENABLE_SELSYNC</td>
<td>Audio selsync recording channel(s)</td>
</tr>
<tr>
<td>ED_TRANSAUDIO_SET_MONITOR</td>
<td>Monitor output audio channel(s)</td>
</tr>
<tr>
<td>ED_TRANSAUDIO_SET_SOURCE</td>
<td>Audio source channel(s)</td>
</tr>
</table>
 


### -param pValue [out]

Specifies a pointer to a <b>long</b> integer to receive the channel or channels set in the <a href="https://msdn.microsoft.com/e013dd73-7276-48b3-bf5f-ffb4b3d49419">IAMExtTransport::SetTransportAudioParameters</a> method.


## -returns



When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/4ce48038-bfcf-4b1f-8053-3446929a5f06">IAMExtTransport Interface</a>
 

 

