---
UID: NN:strmif.IEncoderAPI
title: IEncoderAPI
author: windows-sdk-content
description: IEncoderAPI is no longer available for use.
old-location: mstv\iencoderapi.htm
tech.root: mstv
ms.assetid: 823b79a1-1bf5-4aab-80dd-0e77ba950127
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IEncoderAPI, IEncoderAPI interface [Microsoft TV Technologies], IEncoderAPI interface [Microsoft TV Technologies],described, IEncoderAPIInterface, mstv.iencoderapi, strmif/IEncoderAPI
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEncoderAPI interface


## -description


<p class="CCE_Message">[<b>IEncoderAPI</b> is no longer available for use. Instead, use <a href="https://msdn.microsoft.com/cc3f1bd9-1d36-45e6-94e2-07f2800fd073">ICodecAPI</a>.]

The <b>IEncoderAPI</b> interface defines a standard way for applications and drivers to communicate with third-party hardware or software encoders that implement the interface. For more information on this interface, see <a href="https://msdn.microsoft.com/3d19152f-17a3-4576-a2a2-5b827d9ca8d1">Encoder API</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEncoderAPI</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEncoderAPI</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEncoderAPI</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/86eb8008-6d1c-4de7-8a88-b42f33ca24d3">GetDefaultValue</a>
</td>
<td align="left" width="63%">
Retrieves the default value for a parameter, if one exists.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fb48a460-c891-4fbe-8fe2-f900f8b405b7">GetParameterRange</a>
</td>
<td align="left" width="63%">
Retrieves the valid range of values that the parameter supports, in cases where the parameter supports a stepped range as opposed to a list of specific values.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/406316b5-1de0-4a89-b1bc-2f3b63ab0739">GetParameterValues</a>
</td>
<td align="left" width="63%">
Retrieves the list of values supported by the given parameter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/62f69677-05cd-46ab-8b77-96e10f8fbb1d">GetValue</a>
</td>
<td align="left" width="63%">
Retrieves the current value of a specified parameter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ad94b70f-fd35-44b4-8322-9891cd7f17cc">IsAvailable</a>
</td>
<td align="left" width="63%">
Queries whether a given parameter is available.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bbcbde18-2b2d-48b0-9f52-185648f502ce">IsSupported</a>
</td>
<td align="left" width="63%">
Queries whether a given parameter is supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a7dc0964-64b9-4ea3-8948-19ec100d64f5">SetValue</a>
</td>
<td align="left" width="63%">
Sets the current value of a parameter.

</td>
</tr>
</table> 


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
<td>Secifies the peak bit rate. This parameter is relevant only when <b>ENCAPIPARAM_BITRATE_MODE</b> has been set to <b>VariableBitRatePeak</b>.</td>
</tr>
<tr>
<td>ENCAPIPARAM_BITRATE_MODE</td>
<td>Specifies the bit-rate mode, as a <a href="https://msdn.microsoft.com/ccceae9a-6d1d-4453-bd84-88cefc20320e">VIDEOENCODER_BITRATE_MODE</a> enumeration value (32-bit signed long).</td>
</tr>
</table>
 

The following table describes the expected behavior of an encoder under extremely high or low bitrate conditions in the two variable bitrate modes defined in <a href="https://msdn.microsoft.com/ccceae9a-6d1d-4453-bd84-88cefc20320e">VIDEOENCODER_BITRATE_MODE</a>.

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
This interface supports OpenCable Unidirectional Cable Receiver (OCUR) devices. See <a href="https://msdn.microsoft.com/7b641b94-9854-4ca8-8362-a9e1e49bbdd2">OCUR Devices</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd375602(v=VS.85).aspx">Encoder API</a>
 

 

