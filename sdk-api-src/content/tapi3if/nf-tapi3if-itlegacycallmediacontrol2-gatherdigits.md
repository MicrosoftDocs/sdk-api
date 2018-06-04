---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# ITLegacyCallMediaControl2::GatherDigits


## -description


The 
<b>GatherDigits</b> method initiates the gathering of digits on the specified call. The application specifies the maximum number of digits to collect.


## -parameters




### -param DigitMode [in]

The digit mode(s) to monitor. This parameter specifies one or more of the 
<a href="https://msdn.microsoft.com/d603ea28-2b93-4548-bb16-78e93087f828">LINEDIGITMODE</a> constants.


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
<a href="https://msdn.microsoft.com/87d5f777-e536-46be-8ad4-437386f04c9b">lineGatherDigits</a> function.

Only one 
<b>GatherDigits</b> call can be outstanding on a call. If you call 
<b>GatherDigits</b> again, before the <b>TE_GATHERDIGITS</b> event has occurred, the second call cancels the previous gathering of digits. Canceled digit-gathering attempts send a <b>TE_GATHERDIGITS</b> event with the digits collected so far.




## -see-also




<a href="https://msdn.microsoft.com/47fa5669-1c74-4c18-8370-3efe35b3573e">ITLegacyCallMediaControl2</a>
 

 

