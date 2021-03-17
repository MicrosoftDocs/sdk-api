---
UID: NF:strmif.IAMExtTransport.GetTransportVideoParameters
title: IAMExtTransport::GetTransportVideoParameters (strmif.h)
description: The GetTransportVideoParameters retrieves video parameter settings for external transport.
helpviewer_keywords: ["GetTransportVideoParameters","GetTransportVideoParameters method [DirectShow]","GetTransportVideoParameters method [DirectShow]","IAMExtTransport interface","IAMExtTransport interface [DirectShow]","GetTransportVideoParameters method","IAMExtTransport.GetTransportVideoParameters","IAMExtTransport::GetTransportVideoParameters","IAMExtTransportGetTransportVideoParameters","dshow.iamexttransport_gettransportvideoparameters","strmif/IAMExtTransport::GetTransportVideoParameters"]
old-location: dshow\iamexttransport_gettransportvideoparameters.htm
tech.root: dshow
ms.assetid: 7a77ecf6-49e4-4d91-a06e-80313b4b8957
ms.date: 12/05/2018
ms.keywords: GetTransportVideoParameters, GetTransportVideoParameters method [DirectShow], GetTransportVideoParameters method [DirectShow],IAMExtTransport interface, IAMExtTransport interface [DirectShow],GetTransportVideoParameters method, IAMExtTransport.GetTransportVideoParameters, IAMExtTransport::GetTransportVideoParameters, IAMExtTransportGetTransportVideoParameters, dshow.iamexttransport_gettransportvideoparameters, strmif/IAMExtTransport::GetTransportVideoParameters
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMExtTransport::GetTransportVideoParameters
 - strmif/IAMExtTransport::GetTransportVideoParameters
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMExtTransport.GetTransportVideoParameters
---

# IAMExtTransport::GetTransportVideoParameters


## -description

The <code>GetTransportVideoParameters</code> retrieves video parameter settings for external transport.



This method is not implemented.

## -parameters

### -param Param [in]

Specifies the video parameter to retrieve. Must be one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>ED_TRANSVIDEO_SET_OUTPUT</td>
<td>Retrieves the output mode.</td>
</tr>
<tr>
<td>ED_TRANSVIDEO_SET_SOURCE</td>
<td>Retrieves the input pin.</td>
</tr>
</table>

### -param pValue [out]

Specifies a pointer to a <b>long</b> integer to receive the video parameter. See Remarks for more information.

## -returns

When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.

## -remarks

If <i>Param</i> equals ED_TRANSVIDEO_SET_OUTPUT, <i>pValue</i> receives one of the following constants.

<table>
<tr>
<th>Value
            </th>
<th>Description
            </th>
</tr>
<tr>
<td>ED_E2E</td>
<td>Input video is displayed on the device's output regardless of the transport mode.</td>
</tr>
<tr>
<td>ED_OFF</td>
<td>Video output is disabled.</td>
</tr>
<tr>
<td>ED_PLAYBACK</td>
<td>Video playing from media is displayed on the device's output.</td>
</tr>
</table>
 

If <i>Param</i> equals ED_TRANSVIDEO_SET_SOURCE, <i>pValue</i> receives the index of the input pin used for the video input. The pin index is zero-based.

<h3><a id="DV_Implementation"></a><a id="dv_implementation"></a><a id="DV_IMPLEMENTATION"></a>DV Implementation</h3>

<a href="/windows/desktop/DirectShow/msdv-driver">MSDV</a> does not support this method. It returns E_NOTIMPL.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamexttransport">IAMExtTransport Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iamexttransport-settransportvideoparameters">IAMExtTransport::SetTransportVideoParameters</a>