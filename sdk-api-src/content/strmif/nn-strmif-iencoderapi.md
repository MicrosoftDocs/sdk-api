---
UID: NN:strmif.IEncoderAPI
title: IEncoderAPI (strmif.h)
description: IEncoderAPI is no longer available for use. (IEncoderAPI)
helpviewer_keywords: ["IEncoderAPI","IEncoderAPI interface [Microsoft TV Technologies]","IEncoderAPI interface [Microsoft TV Technologies]","described","IEncoderAPIInterface","mstv.iencoderapi","strmif/IEncoderAPI"]
old-location: mstv\iencoderapi.htm
tech.root: mstv
ms.assetid: 823b79a1-1bf5-4aab-80dd-0e77ba950127
ms.date: 12/05/2018
ms.keywords: IEncoderAPI, IEncoderAPI interface [Microsoft TV Technologies], IEncoderAPI interface [Microsoft TV Technologies],described, IEncoderAPIInterface, mstv.iencoderapi, strmif/IEncoderAPI
req.header: strmif.h
req.include-header: Dshow.h
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEncoderAPI
 - strmif/IEncoderAPI
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
 - IEncoderAPI
---

# IEncoderAPI interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

<p class="CCE_Message">[<b>IEncoderAPI</b> is no longer available for use. Instead, use <a href="/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI</a>.]

The <b>IEncoderAPI</b> interface defines a standard way for applications and drivers to communicate with third-party hardware or software encoders that implement the interface. For more information on this interface, see <a href="/windows/desktop/DirectShow/encoder-api">Encoder API</a>.

## -inheritance

The <b>IEncoderAPI</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEncoderAPI</b> also has these types of members:
<ul>
<li>Methods</li>
</ul>

## -remarks

In the various interface methods, the following GUIDs, defined in uuids.h, are used to indicate which parameter is being set or retrieved.

<table>
<tr>
<th>Parameter
            </th>
<th>Description
            </th>
</tr>
<tr>
<td>ENCAPIPARAM_BITRATE</td>
<td>Specifies the bit rate, in bits per second. In constant bit rate (CBR) mode, the value gives the constant bitrate. In either variable bit rate mode, it gives the average bit rate. The value is a 32-bit unsigned long.</td>
</tr>
<tr>
<td>ENCAPIPARAM_PEAK_BITRATE</td>
<td>Specifies the peak bit rate. This parameter is relevant only when <b>ENCAPIPARAM_BITRATE_MODE</b> has been set to <b>VariableBitRatePeak</b>.</td>
</tr>
<tr>
<td>ENCAPIPARAM_BITRATE_MODE</td>
<td>Specifies the bit-rate mode, as a <a href="/windows/desktop/api/strmif/ne-strmif-videoencoder_bitrate_mode">VIDEOENCODER_BITRATE_MODE</a> enumeration value (32-bit signed long).</td>
</tr>
</table>
 

The following table describes the expected behavior of an encoder under extremely high or low bitrate conditions in the two variable bitrate modes defined in <a href="/windows/desktop/api/strmif/ne-strmif-videoencoder_bitrate_mode">VIDEOENCODER_BITRATE_MODE</a>.

<table>
<tr>
<th>Condition
            </th>
<th>Mode
            </th>
<th>Behavior
            </th>
</tr>
<tr>
<td>Scene falls to black or there is zero motion</td>
<td><b>VariableBitRateAverage</b></td>
<td>Over a short period of time (several seconds) the bit rate will fall below the rate specified for the ENCAPIPARAM_BITRATE parameter. But over a four-minute period of time, the encoder will maintain the average rate, if necessary by adding "dummy" bits to the stream.</td>
</tr>
<tr>
<td>Scene falls to black or there is zero motion.</td>
<td><b>VariableBitRatePeak</b></td>
<td>The bitrate will fall below the expected rate as specified in the value for the ENCAPIPARAM_BITRATE parameter. The rate will stay at that level until a more complicated scene begins.</td>
</tr>
<tr>
<td>The scene is extremely complex.</td>
<td><b>VariableBitRateAverage</b></td>
<td>For a few seconds the rate will go up. If the scene stays complex, the rate will come back down and the picture will become blocky in order to maintain the average as specified in the value for the ENCAPIPARAM_BITRATE parameter.</td>
</tr>
<tr>
<td>The scene is extremely complex.</td>
<td><b>VariableBitRatePeak</b></td>
<td>The rate will go up and stay up, possibly above the expected rate as specified in the value for the ENCAPIPARAM_BITRATE parameter, but never above the peak as specified in the ENCAPIPARAM_PEAK_BITRATE parameter.</td>
</tr>
</table>
 

<h3><a id="OCUR_Devices"></a><a id="ocur_devices"></a><a id="OCUR_DEVICES"></a>OCUR Devices</h3>

This interface supports OpenCable Unidirectional Cable Receiver (OCUR) devices. See <a href="/previous-versions/windows/desktop/mstv/ocur-devices">OCUR Devices</a>.

## -see-also

<a href="/windows/desktop/DirectShow/encoder-api">Encoder API</a>

