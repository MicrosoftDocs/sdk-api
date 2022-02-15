---
UID: NF:iphlpapi.UnenableRouter
title: UnenableRouter function (iphlpapi.h)
description: The UnenableRouter function decrements the reference count that tracks the number of requests to enable IPv4 forwarding. When this reference count reaches zero, UnenableRouter turns off IPv4 forwarding on the local computer.
helpviewer_keywords: ["UnenableRouter","UnenableRouter function [IP Helper]","_iphlp_unenablerouter","iphlp.unenablerouter","iphlpapi/UnenableRouter"]
old-location: iphlp\unenablerouter.htm
tech.root: IpHlp
ms.assetid: 95f0387f-24e8-4382-b78e-e59bcec0f2ed
ms.date: 12/05/2018
ms.keywords: UnenableRouter, UnenableRouter function [IP Helper], _iphlp_unenablerouter, iphlp.unenablerouter, iphlpapi/UnenableRouter
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
 - UnenableRouter
 - iphlpapi/UnenableRouter
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
 - UnenableRouter
---

# UnenableRouter function


## -description

The 
<b>UnenableRouter</b> function decrements the reference count that tracks the number of requests to enable IPv4 forwarding. When this reference count reaches zero, 
<b>UnenableRouter</b> turns off IPv4 forwarding on the local computer.

## -parameters

### -param pOverlapped

A pointer to an <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure. This structure should be the same as the one used in the call to 
the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-enablerouter">EnableRouter</a> function.

### -param lpdwEnableCount [out, optional]

An optional pointer to a <b>DWORD</b> variable. This variable receives the number of references remaining.

## -returns

If the function succeeds, the return value is NO_ERROR.

If the function fails, use 
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> to obtain the message string for the returned error.

## -remarks

The <b>UnenableRouter</b> function is specific to IPv4 forwarding. Each call that a process makes to 
<b>UnenableRouter</b> must correspond to a previous call to 
<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-enablerouter">EnableRouter</a> by the same process. The system returns an error on extraneous calls to 
<b>UnenableRouter</b>. As a result, a given process is not able to decrement the reference count that tracks the number of requests for enabling IPv4 forwarding for another process. Also, if IPv4 forwarding was enabled by a given process, it cannot be disabled by a different process.

It is not possible to accurately determine the reference count that tracks the number of requests for enabling IPv4 forwarding since there might be other outstanding <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-enablerouter">EnableRouter</a> requests.
        So the value returned for the <i>lpdwEnableCount</i> parameter is always a large count equal to ULONG_MAX/2.
        

If the process that calls 
<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-enablerouter">EnableRouter</a> terminates without calling 
<b>UnenableRouter</b>, the system  decrements the reference count that tracks requests to enable  IPv4 forwarding as though the process had called 
<b>UnenableRouter</b>. 

After calling the 
<b>UnenableRouter</b>, use the 
<a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> call to close the handle to the event object in the 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure.

## -see-also

<a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-enablerouter">EnableRouter</a>



<a href="/windows/desktop/IpHlp/ip-helper-function-reference">IP Helper Function Reference</a>



<a href="/windows/desktop/IpHlp/ip-helper-start-page">IP Helper Start Page</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a>