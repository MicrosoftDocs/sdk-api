---
UID: NF:winbase.RequestWakeupLatency
title: RequestWakeupLatency function (winbase.h)
description: Has no effect and returns STATUS_NOT_SUPPORTED. This function is provided only for compatibility with earlier versions of Windows.Windows Server 2008 and Windows Vista:  Has no effect and always returns success.
helpviewer_keywords: ["LT_DONT_CARE","LT_LOWEST_LATENCY","RequestWakeupLatency","RequestWakeupLatency function","_win32_requestwakeuplatency","base.requestwakeuplatency","winbase/RequestWakeupLatency"]
old-location: base\requestwakeuplatency.htm
tech.root: base
ms.assetid: f30fdfb6-dc7e-47fd-93ad-36655e65d0ae
ms.date: 12/05/2018
ms.keywords: LT_DONT_CARE, LT_LOWEST_LATENCY, RequestWakeupLatency, RequestWakeupLatency function, _win32_requestwakeuplatency, base.requestwakeuplatency, winbase/RequestWakeupLatency
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RequestWakeupLatency
 - winbase/RequestWakeupLatency
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-kernel32-legacy-l1-1-6.dll
 - api-ms-win-core-kernel32-legacy-l1-1-5.dll
 - api-ms-win-core-kernel32-legacy-l1-1-4.dll
 - api-ms-win-core-kernel32-legacy-l1-1-3.dll
 - api-ms-win-core-kernel32-legacy-l1-1-2.dll
 - api-ms-win-core-kernel32-legacy-l1-1-1.dll
 - api-ms-win-core-kernel32-legacy-l1-1-0.dll
 - Kernel32.dll
api_name:
 - RequestWakeupLatency
---

# RequestWakeupLatency function


## -description

<p class="CCE_Message">[<b>RequestWakeupLatency</b> 
    is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in 
    subsequent versions.]

Has no effect and returns <b>STATUS_NOT_SUPPORTED</b>. This function is provided only for compatibility with earlier versions of Windows.

<b>Windows Server 2008 and Windows Vista:  </b>Has no effect and always returns success.

## -parameters

### -param latency [in]

The latency requirement for the time is takes to wake the computer. This parameter can be one of the 
      following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LT_LOWEST_LATENCY"></a><a id="lt_lowest_latency"></a><dl>
<dt><b>LT_LOWEST_LATENCY</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
PowerSystemSleeping1 state (equivalent to ACPI state S0 and APM state Working).

</td>
</tr>
<tr>
<td width="40%"><a id="LT_DONT_CARE"></a><a id="lt_dont_care"></a><dl>
<dt><b>LT_DONT_CARE</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Any latency (default).

</td>
</tr>
</table>

## -returns

The return value is nonzero.

## -remarks

The system uses the wake-up latency requirement when choosing a sleeping state. The latency is not guaranteed 
    because wake-up time is determined by the hardware design of the particular computer.

To cancel a latency request, call 
    <b>RequestWakeupLatency</b> with 
    <b>LT_DONT_CARE</b>.

## -see-also

<a href="/windows/desktop/Power/power-management-functions">Power Management Functions</a>