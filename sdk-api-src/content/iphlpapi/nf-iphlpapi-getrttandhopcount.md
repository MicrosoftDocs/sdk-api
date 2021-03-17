---
UID: NF:iphlpapi.GetRTTAndHopCount
title: GetRTTAndHopCount function (iphlpapi.h)
description: The GetRTTAndHopCount function determines the round-trip time (RTT) and hop count to the specified destination.
helpviewer_keywords: ["GetRTTAndHopCount","GetRTTAndHopCount function [IP Helper]","_iphlp_getrttandhopcount","iphlp.getrttandhopcount","iphlpapi/GetRTTAndHopCount"]
old-location: iphlp\getrttandhopcount.htm
tech.root: IpHlp
ms.assetid: 4e84fe6f-40bd-4f0e-bb78-4180e13577aa
ms.date: 12/05/2018
ms.keywords: GetRTTAndHopCount, GetRTTAndHopCount function [IP Helper], _iphlp_getrttandhopcount, iphlp.getrttandhopcount, iphlpapi/GetRTTAndHopCount
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
 - GetRTTAndHopCount
 - iphlpapi/GetRTTAndHopCount
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
 - GetRTTAndHopCount
---

# GetRTTAndHopCount function


## -description

The 
<b>GetRTTAndHopCount</b> function determines the round-trip time (RTT) and hop count to the specified destination.

## -parameters

### -param DestIpAddress [in]

IP address of the destination for which to determine the RTT and hop count, in the form of an <a href="/windows/desktop/api/inaddr/ns-inaddr-in_addr">IPAddr</a> structure.

### -param HopCount [out]

Pointer to a <b>ULONG</b> variable. This variable receives the hop count to the destination specified by the <i>DestIpAddress</i> parameter.

### -param MaxHops [in]

Maximum number of hops to search for the destination. If the number of hops to the destination exceeds this number, the function terminates the search and returns <b>FALSE</b>.

### -param RTT [out]

Round-trip time, in milliseconds, to the destination specified by <i>DestIpAddress</i>.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. Call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> to obtain the error code for the failure.

## -remarks

For information about the <b>IPAddr</b> data type, see 
<a href="/windows/desktop/WinProg/windows-data-types">Windows Data Types</a>. To convert an IP address between dotted decimal notation and <b>IPAddr</b> format, use the 
<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-inet_addr">inet_addr</a> and 
<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-inet_ntoa">inet_ntoa</a> functions.


#### Examples

The following example retrieves and prints the round trip time and hop count to the destination IP address 127.0.0.1.


```cpp
UINT ip = inet_addr("127.0.0.1");
ULONG hopCount = 0;
ULONG RTT = 0;

if(GetRTTAndHopCount(ip, &hopCount, 30, &RTT) == TRUE) {
  printf("Hops: %ld\n", hopCount);
  printf("RTT: %ld\n", RTT);
}
else {
  printf("Error: %ld\n", GetLastError());
}

```

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getbestinterface">GetBestInterface</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getbestroute">GetBestRoute</a>



<a href="/windows/desktop/IpHlp/ip-helper-function-reference">IP Helper Function Reference</a>



<a href="/windows/desktop/IpHlp/ip-helper-start-page">IP Helper Start Page</a>



<a href="/windows/desktop/api/inaddr/ns-inaddr-in_addr">IPAddr</a>