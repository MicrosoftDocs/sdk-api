---
UID: NF:securitybaseapi.CveEventWrite
title: CveEventWrite function (securitybaseapi.h)
description: A tracing function for publishing events when an attempted security vulnerability exploit is detected in your user-mode application.
helpviewer_keywords: ["CveEventWrite","CveEventWrite function [ETW]","etw.cveeventwrite","securitybaseapi/CveEventWrite"]
old-location: etw\cveeventwrite.htm
tech.root: ETW
ms.assetid: 81CDC4A8-67B3-40AE-B492-89EF47BC5C4D
ms.date: 12/05/2018
ms.keywords: CveEventWrite, CveEventWrite function [ETW], etw.cveeventwrite, securitybaseapi/CveEventWrite
req.header: securitybaseapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CveEventWrite
 - securitybaseapi/CveEventWrite
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-security-base-l1-2-2.dll
 - Advapi32.dll
 - KernelBase.dll
 - API-MS-Win-Eventing-Provider-L1-1-1.dll
 - API-MS-Win-Security-Base-L1-2-1.dll
api_name:
 - CveEventWrite
---

# CveEventWrite function


## -description

A tracing function for publishing events when an attempted security vulnerability exploit is detected in your user-mode application.

## -parameters

### -param CveId [in]

A pointer to the CVE ID associated with the vulnerability for which this event is being raised.

### -param AdditionalDetails [in, optional]

A pointer to a string giving additional details that the event producer may want to provide to the consumer of this event.

## -returns

Returns ERROR_SUCCESS if successful or one of the following values on error.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more of the parameters is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ARITHMETIC_OVERFLOW</b></dt>
</dl>
</td>
<td width="60%">
The event size is larger than the allowed maximum (64k - header).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The session buffer size is too small for the event.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Occurs when filled buffers are trying to flush to disk, but disk IOs are not happening fast enough. This 
        happens when the disk is slow and event traffic is heavy. Eventually, there are no more free (empty) buffers 
        and the event is dropped.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_LOG_FILE_FULL</b></dt>
</dl>
</td>
<td width="60%">
The real-time playback file is full. Events are not logged to the session until a real-time consumer 
        consumes the events from the playback file. Do not stop logging events based on this error code.

</td>
</tr>
</table>

## -remarks

The CveEventWrite function publishes a CVE-based event. This function should be called only in scenarios where an attempt to exploit a known, patched vulnerability is detected by the application. Ideally, this function call should be added as part of the fix (update) itself.

The default consumer for this event is EventLog-Application. To enable another consumer, the provider can be added to the consumer session.

Provider GUID: 85a62a0d-7e17-485f-9d4f-749a287193a6

Source Name: Microsoft-Windows-Audit-CVE or Audit-CVE

