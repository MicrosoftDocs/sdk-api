---
UID: NF:mfidl.IMFRateSupport.GetFastestRate
title: IMFRateSupport::GetFastestRate (mfidl.h)
description: Gets the fastest playback rate supported by the object.
helpviewer_keywords: ["00413771-21cb-48a7-9080-2c3d195c366b","GetFastestRate","GetFastestRate method [Media Foundation]","GetFastestRate method [Media Foundation]","IMFRateSupport interface","IMFRateSupport interface [Media Foundation]","GetFastestRate method","IMFRateSupport.GetFastestRate","IMFRateSupport::GetFastestRate","mf.imfratesupport_getfastestrate","mfidl/IMFRateSupport::GetFastestRate"]
old-location: mf\imfratesupport_getfastestrate.htm
tech.root: mf
ms.assetid: 00413771-21cb-48a7-9080-2c3d195c366b
ms.date: 12/05/2018
ms.keywords: 00413771-21cb-48a7-9080-2c3d195c366b, GetFastestRate, GetFastestRate method [Media Foundation], GetFastestRate method [Media Foundation],IMFRateSupport interface, IMFRateSupport interface [Media Foundation],GetFastestRate method, IMFRateSupport.GetFastestRate, IMFRateSupport::GetFastestRate, mf.imfratesupport_getfastestrate, mfidl/IMFRateSupport::GetFastestRate
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFRateSupport::GetFastestRate
 - mfidl/IMFRateSupport::GetFastestRate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFRateSupport.GetFastestRate
---

# IMFRateSupport::GetFastestRate


## -description

Gets the fastest playback rate supported by the object.

## -parameters

### -param eDirection [in]

Specifies whether to query to the fastest forward playback rate or reverse playback rate. The value is a member of the <a href="/windows/desktop/api/mfidl/ne-mfidl-mfrate_direction">MFRATE_DIRECTION</a> enumeration.

### -param fThin [in]

If <b>TRUE</b>, the method retrieves the fastest thinned playback rate. Otherwise, the method retrieves the fastest non-thinned playback rate. For information about thinning, see <a href="/windows/desktop/medfound/about-rate-control">About Rate Control</a>.

### -param pflRate [out]

Receives the fastest playback rate that the object supports.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_REVERSE_UNSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The object does not support reverse playback.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_THINNING_UNSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The object does not support thinning.

</td>
</tr>
</table>

## -remarks

For some formats (such as ASF), thinning means dropping all frames that are not I-frames. If a component produces stream data, such as a media source or a demultiplexer, it should pay attention to the <i>fThin</i> parameter and return MF_E_THINNING_UNSUPPORTED if it cannot thin the stream.

If the component processes or receives a stream (most transforms or media sinks), it may ignore this parameter if it does not care whether the stream is thinned. In the Media Session's implementation of rate support, if the transforms do not explicitly support reverse playback, the Media Session will attempt to playback in reverse with thinning but not without thinning. Therefore, most applications will set <i>fThin</i> to <b>TRUE</b> when using the Media Session for reverse playback.

If <i>eDirection</i> is MFRATE_REVERSE, the method retrieves the fastest reverse playback rate. This is a negative value, assuming the object supports reverse playback.

## -see-also

<a href="/windows/desktop/medfound/how-to-determine-supported-rates">How to Determine Supported Rates</a>



<a href="/windows/desktop/api/mfidl/nn-mfidl-imfratesupport">IMFRateSupport</a>