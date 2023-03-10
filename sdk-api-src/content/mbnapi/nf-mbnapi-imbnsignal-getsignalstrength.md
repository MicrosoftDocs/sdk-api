---
UID: NF:mbnapi.IMbnSignal.GetSignalStrength
title: IMbnSignal::GetSignalStrength (mbnapi.h)
description: Gets the signal strength received by the device.
helpviewer_keywords: ["GetSignalStrength","GetSignalStrength method [Microsoft Broadband Networks]","GetSignalStrength method [Microsoft Broadband Networks]","IMbnSignal interface","IMbnSignal interface [Microsoft Broadband Networks]","GetSignalStrength method","IMbnSignal.GetSignalStrength","IMbnSignal::GetSignalStrength","mbn.imbnsignal_getsignalstrength","mbnapi/IMbnSignal::GetSignalStrength"]
old-location: mbn\imbnsignal_getsignalstrength.htm
tech.root: mbn
ms.assetid: 9a580232-4cd2-42f4-a6c7-f777d78241b6
ms.date: 12/05/2018
ms.keywords: GetSignalStrength, GetSignalStrength method [Microsoft Broadband Networks], GetSignalStrength method [Microsoft Broadband Networks],IMbnSignal interface, IMbnSignal interface [Microsoft Broadband Networks],GetSignalStrength method, IMbnSignal.GetSignalStrength, IMbnSignal::GetSignalStrength, mbn.imbnsignal_getsignalstrength, mbnapi/IMbnSignal::GetSignalStrength
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMbnSignal::GetSignalStrength
 - mbnapi/IMbnSignal::GetSignalStrength
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnSignal.GetSignalStrength
---

# IMbnSignal::GetSignalStrength


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Gets the signal strength received by the device.

## -parameters

### -param signalStrength [out, retval]

Pointer to the signal quality received by the device.  When the signal strength is not known or it is not detectable by the device then this is set to <b>MBN_RSSI_UNKNOWN</b>.
If this method returns any value other than S_OK, this parameter is 0.

## -returns

This method can return one of these values.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_PENDING</b></dt>
</dl>
</td>
<td width="60%">
The signal quality is not available.  The Mobile Broadband service is currently probing the device to retrieve this information.  When the signal quality is available, the Mobile Broadband service will call the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsignalevents-onsignalstatechange">OnSignalStateChange</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnsignalevents">IMbnSignalEvents</a>.

</td>
</tr>
</table>

## -remarks

<b>GetSignalStrength</b> reports signal strength received by the Mobile Broadband device. For GSM based devices it reports signal strength as signal strength received in a coded value. For CDMA devices it reports based on the Compensated RSSI (accounts for noise) and not based on Raw RSSI.


The following table contains the coded values that may be returned.<table>
<tr>
<th>Signal Strength (in dBm) </th>
<th>Coded Value (Min: 0 Max: 31)</th>
</tr>
<tr>
<td>-113 or less</td>
<td>0</td>
</tr>
<tr>
<td>-111</td>
<td>1</td>
</tr>
<tr>
<td>-109</td>
<td>2</td>
</tr>
<tr>
<td>...</td>
<td>...</td>
</tr>
<tr>
<td>...</td>
<td>...</td>
</tr>
<tr>
<td>-51 or greater</td>
<td>31</td>
</tr>
<tr>
<td>Unknown or undetectable</td>
<td><b>MBN_RSSI_UNKNOWN</b></td>
</tr>
</table>
 



For recoverable errors <b>E_MBN_PIN_REQUIRED</b>, and <b>E_MBN_RADIO_POWER_OFF</b>, the Mobile Broadband service will query the device again for signal state when the error condition is over. This method will return E_PENDING until the query operation is complete. When the new query is complete, the Mobile Broadband  service will call the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsignalevents-onsignalstatechange">OnSignalStateChange</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnsignalevents">IMbnSignalEvents</a>.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnsignal">IMbnSignal</a>