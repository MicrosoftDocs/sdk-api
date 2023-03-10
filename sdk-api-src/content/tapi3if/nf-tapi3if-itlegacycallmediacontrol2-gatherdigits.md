---
UID: NF:tapi3if.ITLegacyCallMediaControl2.GatherDigits
title: ITLegacyCallMediaControl2::GatherDigits (tapi3if.h)
description: The GatherDigits method initiates the gathering of digits on the specified call. The application specifies the maximum number of digits to collect.
helpviewer_keywords: ["GatherDigits","GatherDigits method [TAPI 2.2]","GatherDigits method [TAPI 2.2]","ITLegacyCallMediaControl2 interface","ITLegacyCallMediaControl2 interface [TAPI 2.2]","GatherDigits method","ITLegacyCallMediaControl2.GatherDigits","ITLegacyCallMediaControl2::GatherDigits","_tapi3_itlegacycallmediacontrol2_gatherdigits","tapi3.itlegacycallmediacontrol2_gatherdigits","tapi3if/ITLegacyCallMediaControl2::GatherDigits"]
old-location: tapi3\itlegacycallmediacontrol2_gatherdigits.htm
tech.root: tapi3
ms.assetid: ff464b1e-bd4c-4807-b019-cdae6896f897
ms.date: 12/05/2018
ms.keywords: GatherDigits, GatherDigits method [TAPI 2.2], GatherDigits method [TAPI 2.2],ITLegacyCallMediaControl2 interface, ITLegacyCallMediaControl2 interface [TAPI 2.2],GatherDigits method, ITLegacyCallMediaControl2.GatherDigits, ITLegacyCallMediaControl2::GatherDigits, _tapi3_itlegacycallmediacontrol2_gatherdigits, tapi3.itlegacycallmediacontrol2_gatherdigits, tapi3if/ITLegacyCallMediaControl2::GatherDigits
req.header: tapi3if.h
req.include-header: 
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITLegacyCallMediaControl2::GatherDigits
 - tapi3if/ITLegacyCallMediaControl2::GatherDigits
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITLegacyCallMediaControl2.GatherDigits
---

# ITLegacyCallMediaControl2::GatherDigits


## -description

The 
<b>GatherDigits</b> method initiates the gathering of digits on the specified call. The application specifies the maximum number of digits to collect.

## -parameters

### -param DigitMode [in]

The digit mode(s) to monitor. This parameter specifies one or more of the 
<a href="/windows/desktop/Tapi/linedigitmode--constants">LINEDIGITMODE</a> constants.

### -param lNumDigits [in]

The number of digits to collect. 




If this parameter is zero, the method cancels any digit-gathering in progress, without starting a new digit-gathering attempt. For more information, see the following Remarks section.

### -param pTerminationDigits [in]

Pointer to a <b>BSTR</b> representation of the termination digits. If one of the termination digits in the string is detected, that digit is appended to the buffer, digit collection is terminated, and the <b>TE_GATHERDIGITS</b> event is sent to the application.

### -param lFirstDigitTimeout [in]

The length of time, in milliseconds, during which the first digit is expected. If the first digit is not received in this timeframe, digit collection is aborted and a <b>TE_GATHERDIGITS</b> event is sent to the application. The buffer contains only the <b>NULL</b> character, indicating that no digits were received and that the first-digit-timeout terminated digit-gathering. The minimum and maximum timeouts you can specify are found in the AC_GATHERDIGITSMINTIMEOUT and AC_GATHERDIGITSMAXTIMEOUT capabilities.

### -param lInterDigitTimeout [in]

The maximum time, in milliseconds, between consecutive digits. If the next digit is not received in this timeframe, digit collection is aborted and a <b>TE_GATHERDIGITS</b> event is sent to the application. The buffer contains only the digits collected up to this point followed by a <b>NULL</b> character, indicating that an interdigit-timeout terminated the digit-gathering. The minimum and maximum timeouts that can be specified are found in the AC_GATHERDIGITSMINTIMEOUT and AC_GATHERDIGITSMAXTIMEOUT capabilities.

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
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pTerminationDigits</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory to allocate the gather digits buffer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_INVALCALLSTATE</b></dt>
</dl>
</td>
<td width="60%">
The call must be in the <i>connected</i> state.

</td>
</tr>
</table>

## -remarks

The 
<b>GatherDigits</b> method translates to a call to the TAPI 2.<i>x</i>
<a href="/windows/desktop/api/tapi/nf-tapi-linegatherdigits">lineGatherDigits</a> function.

Only one 
<b>GatherDigits</b> call can be outstanding on a call. If you call 
<b>GatherDigits</b> again, before the <b>TE_GATHERDIGITS</b> event has occurred, the second call cancels the previous gathering of digits. Canceled digit-gathering attempts send a <b>TE_GATHERDIGITS</b> event with the digits collected so far.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itlegacycallmediacontrol2">ITLegacyCallMediaControl2</a>