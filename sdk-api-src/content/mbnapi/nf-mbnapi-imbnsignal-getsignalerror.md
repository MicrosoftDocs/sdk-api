---
UID: NF:mbnapi.IMbnSignal.GetSignalError
title: IMbnSignal::GetSignalError (mbnapi.h)
description: Gets the received signal error rate.
helpviewer_keywords: ["GetSignalError","GetSignalError method [Microsoft Broadband Networks]","GetSignalError method [Microsoft Broadband Networks]","IMbnSignal interface","IMbnSignal interface [Microsoft Broadband Networks]","GetSignalError method","IMbnSignal.GetSignalError","IMbnSignal::GetSignalError","mbn.imbnsignal_getsignalerror","mbnapi/IMbnSignal::GetSignalError"]
old-location: mbn\imbnsignal_getsignalerror.htm
tech.root: mbn
ms.assetid: 028adb54-9c81-4a5b-85f7-5c12ce8d84e4
ms.date: 12/05/2018
ms.keywords: GetSignalError, GetSignalError method [Microsoft Broadband Networks], GetSignalError method [Microsoft Broadband Networks],IMbnSignal interface, IMbnSignal interface [Microsoft Broadband Networks],GetSignalError method, IMbnSignal.GetSignalError, IMbnSignal::GetSignalError, mbn.imbnsignal_getsignalerror, mbnapi/IMbnSignal::GetSignalError
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
 - IMbnSignal::GetSignalError
 - mbnapi/IMbnSignal::GetSignalError
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
 - IMbnSignal.GetSignalError
---

# IMbnSignal::GetSignalError


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Gets the received signal error rate.

## -parameters

### -param signalError [out, retval]

Pointer to the error rate in the received signal.

Mobile Broadband Interfaces report the signal error rate as a coded value that maps to the percentage range of error rates.   This is the Channel Bit Error Rate for GSM and Frame Error Rate for CDMA.  In both the cases, MBN_ERROR_RATE_UNKNOWN specifies an unknown error rate.

The following table shows the values for the error rate codes.

<table>
<tr>
<th>Bit error rate (in %)</th>
<th>Frame error rate (in %)</th>
<th>Coded value (0-7)</th>
</tr>
<tr>
<td>&lt; 0.2</td>
<td>&lt; 0.01</td>
<td>0</td>
</tr>
<tr>
<td>0.2 - 0.4</td>
<td>0.01 - 0.1</td>
<td>1</td>
</tr>
<tr>
<td>0.4 - 0.8</td>
<td>0.1 - 0.5</td>
<td>2</td>
</tr>
<tr>
<td>0.8 - 1.6</td>
<td>0.5 - 1.0</td>
<td>3</td>
</tr>
<tr>
<td>1.6 - 3.2</td>
<td>1.0 - 2.0</td>
<td>4</td>
</tr>
<tr>
<td>3.2 - 6.4</td>
<td>2.0 - 4.0</td>
<td>5</td>
</tr>
<tr>
<td>6.4 - 12.8</td>
<td>4.0 - 8.0</td>
<td>6</td>
</tr>
<tr>
<td>&gt; 12.8</td>
<td>&gt; 8.0</td>
<td>7</td>
</tr>
<tr>
<td>unknown</td>
<td>unknown</td>
<td>MBN_ERROR_RATE_UNKNOWN</td>
</tr>
</table>

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
The method completed successfully

.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_PENDING</b></dt>
</dl>
</td>
<td width="60%">
The error rate is not yet available.  The Mobile Broadband service is current probing the device to retrieve the information.  When the error rate is available, the Mobile Broadband service will call the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsignalevents-onsignalstatechange">OnSignalStateChange</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnsignalevents">IMbnSignalEvents</a>.

</td>
</tr>
</table>

## -remarks

Mobile Broadband interfaces report the signal error rate as a coded value that maps to a percentage range of error rates.   This is the Channel Bit Error Rate for GSM and Frame Error Rate for CDMA.  For both the cases, <b>MBN_ERROR_RATE_UNKNOWN</b> specifies an unknown error rate.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnsignal">IMbnSignal</a>