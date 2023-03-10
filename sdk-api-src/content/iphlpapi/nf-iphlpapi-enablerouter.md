---
UID: NF:iphlpapi.EnableRouter
title: EnableRouter function (iphlpapi.h)
description: The EnableRouter function turns on IPv4 forwarding on the local computer. EnableRouter also increments a reference count that tracks the number of requests to enable IPv4 forwarding.
helpviewer_keywords: ["EnableRouter","EnableRouter function [IP Helper]","_iphlp_enablerouter","iphlp.enablerouter","iphlpapi/EnableRouter"]
old-location: iphlp\enablerouter.htm
tech.root: IpHlp
ms.assetid: 779f5840-d58d-4194-baa7-2c6a7aeb7d79
ms.date: 12/05/2018
ms.keywords: EnableRouter, EnableRouter function [IP Helper], _iphlp_enablerouter, iphlp.enablerouter, iphlpapi/EnableRouter
req.header: iphlpapi.h
req.include-header: 
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
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EnableRouter
 - iphlpapi/EnableRouter
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iphlpapi.dll
api_name:
 - EnableRouter
---

# EnableRouter function


## -description

The 
<b>EnableRouter</b> function turns on IPv4 forwarding on the local computer. 
<b>EnableRouter</b> also increments a reference count that tracks the number of requests to enable IPv4 forwarding.

## -parameters

### -param pHandle

A pointer to a handle. This parameter is currently unused.

### -param pOverlapped

A pointer to an 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure. Except for the <b>hEvent</b> member, all members of this structure should be set to zero. The <b>hEvent</b> member should contain a handle to a valid event object. Use the 
<a href="/windows/desktop/api/synchapi/nf-synchapi-createeventa">CreateEvent</a> function to create this event object.

## -returns

If the <b>EnableRouter</b> function succeeds, the return value is ERROR_IO_PENDING.

If the function fails, use <a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> to obtain the message string for the returned error.

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
One of the parameters is invalid. This error is returned if the <i>pOverlapped</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
Use 
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> to obtain the message string for the returned error.

</td>
</tr>
</table>

## -remarks

The <b>EnableRouter</b> function is specific to IPv4 forwarding. If the process that calls 
<b>EnableRouter</b> terminates without calling 
<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-unenablerouter">UnenableRouter</a>, the system  decrements the reference count that tracks the number of requests to enable IPv4 forwarding as though the process had called 
<b>UnenableRouter</b>.

## -see-also

<a href="/windows/desktop/api/synchapi/nf-synchapi-createeventa">CreateEvent</a>



<a href="/windows/desktop/IpHlp/ip-helper-function-reference">IP Helper Function Reference</a>



<a href="/windows/desktop/IpHlp/ip-helper-start-page">IP Helper Start Page</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-unenablerouter">UnenableRouter</a>