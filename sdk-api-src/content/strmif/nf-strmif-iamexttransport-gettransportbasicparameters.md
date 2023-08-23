---
UID: NF:strmif.IAMExtTransport.GetTransportBasicParameters
title: IAMExtTransport::GetTransportBasicParameters (strmif.h)
description: The GetTransportBasicParameters method retrieves general properties of the external transport.
helpviewer_keywords: ["GetTransportBasicParameters","GetTransportBasicParameters method [DirectShow]","GetTransportBasicParameters method [DirectShow]","IAMExtTransport interface","IAMExtTransport interface [DirectShow]","GetTransportBasicParameters method","IAMExtTransport.GetTransportBasicParameters","IAMExtTransport::GetTransportBasicParameters","IAMExtTransportGetTransportBasicParameters","dshow.iamexttransport_gettransportbasicparameters","strmif/IAMExtTransport::GetTransportBasicParameters"]
old-location: dshow\iamexttransport_gettransportbasicparameters.htm
tech.root: dshow
ms.assetid: 7f670efe-4433-496d-b789-925c02b69f58
ms.date: 4/26/2023
ms.keywords: GetTransportBasicParameters, GetTransportBasicParameters method [DirectShow], GetTransportBasicParameters method [DirectShow],IAMExtTransport interface, IAMExtTransport interface [DirectShow],GetTransportBasicParameters method, IAMExtTransport.GetTransportBasicParameters, IAMExtTransport::GetTransportBasicParameters, IAMExtTransportGetTransportBasicParameters, dshow.iamexttransport_gettransportbasicparameters, strmif/IAMExtTransport::GetTransportBasicParameters
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
 - IAMExtTransport::GetTransportBasicParameters
 - strmif/IAMExtTransport::GetTransportBasicParameters
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
 - IAMExtTransport.GetTransportBasicParameters
---

# IAMExtTransport::GetTransportBasicParameters


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetTransportBasicParameters</code> method retrieves general properties of the external transport.

## -parameters

### -param Param [in]

Specifies which property to receive.

### -param pValue [in, out]

Pointer to a variable that receives a <b>long</b> integer value. See Remarks for more information.

### -param ppszData [in, out]

Pointer to a variable of type <b>LPOLESTR</b> that receives a string. See Remarks for more information.

## -returns

When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.

## -remarks

The <i>Param</i> parameter is a flag that specifies which property to retrieve. Some properties are numeric; these are returned in the <i>pValue</i> parameter. Other properties are string values; these are returned in the <i>ppszData</i> parameter. For a list of flags and expected values, see <a href="/windows/desktop/api/strmif/nf-strmif-iamexttransport-settransportbasicparameters">IAMExtTransport::SetTransportBasicParameters</a>.

If the method returns a string, the caller must free the string, using the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function.

<h3><a id="DV_and_MPEG_Camcorder_Implementation"></a><a id="dv_and_mpeg_camcorder_implementation"></a><a id="DV_AND_MPEG_CAMCORDER_IMPLEMENTATION"></a>DV and MPEG Camcorder Implementation</h3>

<a href="/windows/desktop/DirectShow/msdv-driver">MSDV</a> supports the following additional flags:

<ul>
<li>
ED_RAW_EXT_DEV_CMD: Invokes a raw AV/C command. Specify the AV/C command as an array of bytes in the <i>ppszData</i> parameter. Specify the size of the command, in bytes, in the <i>pValue</i> parameter. When the method returns, <i>ppszData</i> contains the response from the device, and <i>pValue</i> contains the size of the response, in bytes. The AV/C command is passed directly to the device with no validation or error checking.

The response payload might be larger than the command. It is the caller's responsibility to allocate enough space in the buffer for the response. The maximum payload size is 512 bytes.

For more information, see <a href="/windows/desktop/DirectShow/issuing-raw-av-c-commands">Issuing Raw AV/C Commands</a>.

</li>
<li>
ED_TRANSBASIC_INPUT_SIGNAL: Retrieves the signal format that the DV camcorder is designed to accept. Returns one of the following constants in <i>pValue</i>.

<table>
<tr>
<th>Constant</th>
<th>Description </th>
</tr>
<tr>
<td>ED_TRANSBASIC_SIGNAL_525_60_SD</td>
<td>NTSC SD signal. </td>
</tr>
<tr>
<td>ED_TRANSBASIC_SIGNAL_525_60_SDL</td>
<td>NTSC SDL (long-play) signal. </td>
</tr>
<tr>
<td>ED_TRANSBASIC_SIGNAL_625_50_SD</td>
<td>PAL SD signal.</td>
</tr>
<tr>
<td>ED_TRANSBASIC_SIGNAL_625_50_SDL</td>
<td>PAL SDL (long-play) signal.</td>
</tr>
<tr>
<td>ED_TRANSBASIC_SIGNAL_MPEG2TS</td>
<td>D-VHS signal.</td>
</tr>
</table>
 

</li>
<li>ED_TRANSBASIC_OUTPUT_SIGNAL: Retrieves the signal format that the DV camcorder is designed to transmit. Returns one of the constants listed for the ED_TRANSBASIC_INPUT_SIGNAL flag. 
</li>
</ul>

<a href="/windows/desktop/DirectShow/mstape-driver">MSTape</a> supports additional values for ED_TRANSBASIC_INPUT_SIGNAL and ED_TRANSBASIC_OUTPUT_SIGNAL.

<table>
<tr>
<th>Constant</th>
<th>Description </th>
</tr>
<tr>
<td>ED_TRANSBASIC_SIGNAL_2500_60_MPEG</td>
<td>25-Mbps/60 MPEG stream.</td>
</tr>
<tr>
<td>ED_TRANSBASIC_SIGNAL_1250_60_MPEG</td>
<td>12.5-Mbps/60 MPEG stream.</td>
</tr>
<tr>
<td>ED_TRANSBASIC_SIGNAL_0625_60_MPEG</td>
<td>6.25-Mbps/60 MPEG stream.</td>
</tr>
<tr>
<td>ED_TRANSBASIC_SIGNAL_2500_50_MPEG</td>
<td>25-Mbps/50 MPEG stream.</td>
</tr>
<tr>
<td>ED_TRANSBASIC_SIGNAL_1250_50_MPEG</td>
<td>12.5-Mbps/50 MPEG stream.</td>
</tr>
<tr>
<td>ED_TRANSBASIC_SIGNAL_0625_50_MPEG</td>
<td>6.25-Mbps/50 MPEG stream.</td>
</tr>
<tr>
<td>ED_TRANSBASIC_SIGNAL_UNKNOWN</td>
<td>Unknown signal format.</td>
</tr>
</table>
 

These flags are defined in the header file Xprtdefs.h.

In Windows XP Service Pack 2 and later, the following additional signal types are defined for the ED_TRANSBASIC_INPUT_SIGNAL and ED_TRANSBASIC_OUTPUT_SIGNAL flags.

<table>
<tr>
<th>Constant</th>
<th>Description</th>
</tr>
<tr>
<td>ED_TRANSBASIC_SIGNAL_525_60_DV25</td>
<td>DVCPRO 25, 525-60.</td>
</tr>
<tr>
<td>ED_TRANSBASIC_SIGNAL_625_50_DV25</td>
<td>DVCPRO 25, 625-50. </td>
</tr>
<tr>
<td>ED_TRANSBASIC_SIGNAL_525_60_DV50</td>
<td>DVCPRO 50, 525-60.</td>
</tr>
<tr>
<td>ED_TRANSBASIC_SIGNAL_625_50_DV50</td>
<td>DVCPRO 50, 625-50.</td>
</tr>
<tr>
<td>ED_TRANSBASIC_SIGNAL_HD_60_DVH1</td>
<td>DVCPRO 100, 1080i or 720p</td>
</tr>
<tr>
<td>ED_TRANSBASIC_SIGNAL_HD_50_DVH1</td>
<td>DVCPRO 100, 1080i only</td>
</tr>
</table>
 

To use these constants, include the header file Xprtdefs.h from the Windows SDK.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamexttransport">IAMExtTransport Interface</a>