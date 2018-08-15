---
UID: NF:strmif.IAMDecoderCaps.GetDecoderCaps
title: IAMDecoderCaps::GetDecoderCaps
author: windows-sdk-content
description: The GetDecoderCaps method queries the decoder for its capabilities.
old-location: dshow\iamdecodercaps_getdecodercaps.htm
old-project: DirectShow
ms.assetid: 727db98f-96a1-4fe1-8315-0280541817c2
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: GetDecoderCaps, GetDecoderCaps method [DirectShow], GetDecoderCaps method [DirectShow],IAMDecoderCaps interface, IAMDecoderCaps interface [DirectShow],GetDecoderCaps method, IAMDecoderCaps.GetDecoderCaps, IAMDecoderCaps::GetDecoderCaps, IAMDecoderCapsGetDecoderCaps, dshow.iamdecodercaps_getdecodercaps, strmif/IAMDecoderCaps::GetDecoderCaps
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMDecoderCaps.GetDecoderCaps
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMDecoderCaps::GetDecoderCaps


## -description



The <code>GetDecoderCaps</code> method queries the decoder for its capabilities.




## -parameters




### -param dwCapIndex [in]

Specifies the capability being queried for.

<table>
<tr>
<th>Constant
                </th>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>AM_QUERY_DECODER_VMR_SUPPORT</td>
<td>0x00000001</td>
<td>Video Mixing Renderer Filter 7 (VMR-7) support</td>
</tr>
<tr>
<td>AM_QUERY_DECODER_DXVA_1_SUPPORT</td>
<td>0x00000002</td>
<td>DirectX Video Acceleration support</td>
</tr>
<tr>
<td>AM_QUERY_DECODER_DVD_SUPPORT</td>
<td>0x00000003</td>
<td>DVD Video support</td>
</tr>
<tr>
<td>AM_QUERY_DECODER_ATSC_SD_SUPPORT</td>
<td>0x00000004</td>
<td>Standard-definition (SD) ATSC video support</td>
</tr>
<tr>
<td>AM_QUERY_DECODER_ATSC_HD_SUPPORT</td>
<td>0x00000005</td>
<td>High-definition (HD) ATSC video support</td>
</tr>
<tr>
<td>AM_GETDECODERCAP_QUERY_VMR9_SUPPORT</td>
<td>0x00000006</td>
<td>Video Mixing Renderer Filter 9 (VMR-9) support</td>
</tr>
<tr>
<td>AM_GETDECODERCAP_QUERY_EVR_SUPPORT</td>
<td>0x00000007</td>
<td>Enhanced Video Renderer (EVR) support.</td>
</tr>
</table>
 


### -param lpdwCap [out]

Receives one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>DECODER_CAP_NOTSUPPORTED</td>
<td>The decoder does not support this capability.</td>
</tr>
<tr>
<td>DECODER_CAP_SUPPORTED</td>
<td>The decoder supports this capability.</td>
</tr>
</table>
 


## -returns



If the method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.




## -remarks



The DVD Graph Builder uses this method when it builds a DVD graph. If the decoder does not support the Video Mixing Renderer filter, then the DVD Graph Builder uses the <a href="https://msdn.microsoft.com/e80938b7-31f0-467b-a3fa-c4511d14758d">Overlay Mixer</a> filter instead.




## -see-also




<a href="https://msdn.microsoft.com/1d2f8284-2deb-4207-b067-24a54d6b286c">Building the DVD Filter Graph</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/3951200b-5a81-4832-9dae-021a76c1ab20">IAMDecoderCaps Interface</a>
 

 

