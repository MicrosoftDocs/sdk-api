---
UID: NF:strmif.IAMExtTransport.SetTransportBasicParameters
title: IAMExtTransport::SetTransportBasicParameters (strmif.h)
description: The SetTransportBasicParameters method sets general properties of the transport.
helpviewer_keywords: ["IAMExtTransport interface [DirectShow]","SetTransportBasicParameters method","IAMExtTransport.SetTransportBasicParameters","IAMExtTransport::SetTransportBasicParameters","IAMExtTransportSetTransportBasicParameters","SetTransportBasicParameters","SetTransportBasicParameters method [DirectShow]","SetTransportBasicParameters method [DirectShow]","IAMExtTransport interface","dshow.iamexttransport_settransportbasicparameters","strmif/IAMExtTransport::SetTransportBasicParameters"]
old-location: dshow\iamexttransport_settransportbasicparameters.htm
tech.root: dshow
ms.assetid: 798fa8d0-3834-4168-86a6-069cae3c3e8e
ms.date: 12/05/2018
ms.keywords: IAMExtTransport interface [DirectShow],SetTransportBasicParameters method, IAMExtTransport.SetTransportBasicParameters, IAMExtTransport::SetTransportBasicParameters, IAMExtTransportSetTransportBasicParameters, SetTransportBasicParameters, SetTransportBasicParameters method [DirectShow], SetTransportBasicParameters method [DirectShow],IAMExtTransport interface, dshow.iamexttransport_settransportbasicparameters, strmif/IAMExtTransport::SetTransportBasicParameters
f1_keywords:
- strmif/IAMExtTransport.SetTransportBasicParameters
dev_langs:
- c++
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
- IAMExtTransport.SetTransportBasicParameters
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMExtTransport::SetTransportBasicParameters


## -description



The <code>SetTransportBasicParameters</code> method sets general properties of the transport.




## -parameters




### -param Param [in]

Specifies which property to set. See Remarks for more information.


### -param Value [in]

Specifies the value of the property as a <b>long</b> integer. See Remarks for more information.


### -param pszData [in]

Specifies the value of the property as an <b>LPOLESTR</b>. See Remarks for more information.


## -returns



When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code. Possible error codes include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Device does not support setting this property.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DEVICE_REMOVED</b></dt>
</dl>
</td>
<td width="60%">
Device was removed.

</td>
</tr>
</table>
 




## -remarks



The <i>Param</i> parameter is a flag that specifies which property to set. For some flags, the property is numeric; use the <i>Value</i> parameter to specify the value. For other flags, the property is a string; use the <i>pszData</i> parameter to specify the value. In either case, the method ignores the other parameter.

For the following flags, the <i>Value</i> parameter takes a defined constant.

<ul>
<li>ED_TRANSBASIC_TIME_FORMAT: Specifies the time format.<table>
<tr>
<th>Constant</th>
<th>Description</th>
</tr>
<tr>
<td>ED_FORMAT_MILLISECONDS</td>
<td>Milliseconds.</td>
</tr>
<tr>
<td>ED_FORMAT_FRAMES</td>
<td>Frames.</td>
</tr>
<tr>
<td>ED_FORMAT_REFERENCE_TIME</td>
<td>Reference time.</td>
</tr>
<tr>
<td>ED_FORMAT_HMSF</td>
<td>Binary coded decimal, representing hours, minutes, seconds, and frames.</td>
</tr>
<tr>
<td>ED_FORMAT_TMSF</td>
<td>Binary coded decimal, representing tracks, minutes, seconds, and frames.</td>
</tr>
</table>
 

</li>
<li>ED_TRANSBASIC_TIME_REFERENCE: Specifies the reference time in use by the device.<table>
<tr>
<th>Constant</th>
<th>Description</th>
</tr>
<tr>
<td>ED_TIMEREF_TIMECODE</td>
<td>Time code.</td>
</tr>
<tr>
<td>ED_TIMEREF_CONTROL_TRACK</td>
<td>Control track.</td>
</tr>
<tr>
<td>ED_TIMEREF_INDEX</td>
<td>Index.</td>
</tr>
<tr>
<td>ED_TIMEREF_ATN</td>
<td>Absolute track number. This constant is defined in the header file Xprtdefs.h.</td>
</tr>
</table>
 

</li>
<li>ED_TRANSBASIC_END_STOP_ACTION: Specifies the action the device takes when it reaches the end of the transport medium.<table>
<tr>
<th>Constant</th>
<th>Description</th>
</tr>
<tr>
<td>ED_MODE_STOP</td>
<td>Stop.</td>
</tr>
<tr>
<td>ED_MODE_REWIND</td>
<td>Rewind.</td>
</tr>
<tr>
<td>ED_MODE_FREEZE</td>
<td>Freeze/pause.</td>
</tr>
</table>
 

</li>
<li>ED_TRANSBASIC_RECORD_FORMAT: Specifies the recording speed.<table>
<tr>
<th>Constant</th>
<th>Description</th>
</tr>
<tr>
<td>ED_RECORD_FORMAT_SP</td>
<td>Standard play.</td>
</tr>
<tr>
<td>ED_RECORD_FORMAT_LP</td>
<td>Long play.</td>
</tr>
<tr>
<td>ED_RECORD_FORMAT_EP</td>
<td>Extended play.</td>
</tr>
</table>
 

</li>
<li>ED_TRANSBASIC_SUPERIMPOSE: Specifies whether the on-screen display is enabled or disabled.<table>
<tr>
<th>Constant</th>
<th>Description</th>
</tr>
<tr>
<td>OATRUE</td>
<td>On-screen display is enabled.</td>
</tr>
<tr>
<td>OAFALSE</td>
<td>On-screen display is disabled.</td>
</tr>
</table>
 

</li>
<li>ED_TRANSBASIC_STEP_UNIT: Specifies the step unit.<table>
<tr>
<th>Constant</th>
<th>Description</th>
</tr>
<tr>
<td>ED_STEP_FIELD</td>
<td>Fields.</td>
</tr>
<tr>
<td>ED_STEP_FRAME</td>
<td>Frames.</td>
</tr>
<tr>
<td>ED_STEP_3_2</td>
<td>3/2 Pulldown.</td>
</tr>
</table>
 

</li>
<li>ED_TRANSBASIC_SET_COUNTER_FORMAT: Sets the time format for the counter. See the ED_TRANSBASIC_TIME_FORMAT flag for possible values.</li>
</ul>
For the following flags, use a numeric value in the <i>Value</i> parameter.

<table>
<tr>
<th>Flag
            </th>
<th>Description
            </th>
</tr>
<tr>
<td>ED_TRANSBASIC_STEP_COUNT</td>
<td>Specifies the step count, in units defined by the ED_TRANSBASIC_STEP_UNIT flag.</td>
</tr>
<tr>
<td>ED_TRANSBASIC_SET_FREEZE_TIMEOUT</td>
<td>Specifies the timeout for freeze mode, in units of the current time format.</td>
</tr>
<tr>
<td>ED_TRANSBASIC_SETCLOCK</td>
<td>Sets the clock time.</td>
</tr>
<tr>
<td>ED_TRANSBASIC_SET_COUNTER_VALUE</td>
<td>Sets the value of the counter.</td>
</tr>
</table>
 

For the following flags, use a string in the <i>pszData</i> parameter.

<table>
<tr>
<th>Flag
            </th>
<th>Description
            </th>
</tr>
<tr>
<td>ED_TRANSBASIC_VOLUME_NAME</td>
<td>Specifies the volume name.</td>
</tr>
</table>
 

<h3><a id="DV_Implementation"></a><a id="dv_implementation"></a><a id="DV_IMPLEMENTATION"></a>DV Implementation</h3>

<a href="https://docs.microsoft.com/windows/desktop/DirectShow/msdv-driver">MSDV</a> does not support this method. It returns E_NOTIMPL.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamexttransport">IAMExtTransport Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamexttransport-gettransportbasicparameters">IAMExtTransport::GetTransportBasicParameters</a>
 

 

