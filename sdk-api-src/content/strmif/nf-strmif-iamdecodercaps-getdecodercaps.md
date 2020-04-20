---
UID: NF:strmif.IAMDecoderCaps.GetDecoderCaps
title: IAMDecoderCaps::GetDecoderCaps (strmif.h)
description: The GetDecoderCaps method queries the decoder for its capabilities.helpviewer_keywords: ["GetDecoderCaps","GetDecoderCaps method [DirectShow]","GetDecoderCaps method [DirectShow]","IAMDecoderCaps interface","IAMDecoderCaps interface [DirectShow]","GetDecoderCaps method","IAMDecoderCaps.GetDecoderCaps","IAMDecoderCaps::GetDecoderCaps","IAMDecoderCapsGetDecoderCaps","dshow.iamdecodercaps_getdecodercaps","strmif/IAMDecoderCaps::GetDecoderCaps"]
old-location: dshow\iamdecodercaps_getdecodercaps.htm
tech.root: DirectShow
ms.assetid: 727db98f-96a1-4fe1-8315-0280541817c2
ms.date: 12/05/2018
ms.keywords: GetDecoderCaps, GetDecoderCaps method [DirectShow], GetDecoderCaps method [DirectShow],IAMDecoderCaps interface, IAMDecoderCaps interface [DirectShow],GetDecoderCaps method, IAMDecoderCaps.GetDecoderCaps, IAMDecoderCaps::GetDecoderCaps, IAMDecoderCapsGetDecoderCaps, dshow.iamdecodercaps_getdecodercaps, strmif/IAMDecoderCaps::GetDecoderCaps
f1_keywords:
- strmif/IAMDecoderCaps.GetDecoderCaps
dev_langs:
- c++
req.header: strmif.h
req.include-header: Dshow.h
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
- IAMDecoderCaps.GetDecoderCaps
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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



The DVD Graph Builder uses this method when it builds a DVD graph. If the decoder does not support the Video Mixing Renderer filter, then the DVD Graph Builder uses the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/overlay-mixer-filter">Overlay Mixer</a> filter instead.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/building-the-dvd-filter-graph">Building the DVD Filter Graph</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamdecodercaps">IAMDecoderCaps Interface</a>
 

 

