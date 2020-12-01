---
UID: NF:iphlpapi.GetBestRoute
title: GetBestRoute function (iphlpapi.h)
description: The GetBestRoute function retrieves the best route to the specified destination IP address.
helpviewer_keywords: ["GetBestRoute","GetBestRoute function [IP Helper]","_iphlp_getbestroute","iphlp.getbestroute","iphlpapi/GetBestRoute"]
old-location: iphlp\getbestroute.htm
tech.root: IpHlp
ms.assetid: 5e507d14-f603-467d-9c37-bb048658d0b1
ms.date: 12/05/2018
ms.keywords: GetBestRoute, GetBestRoute function [IP Helper], _iphlp_getbestroute, iphlp.getbestroute, iphlpapi/GetBestRoute
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
 - GetBestRoute
 - iphlpapi/GetBestRoute
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
 - GetBestRoute
---

# GetBestRoute function


## -description

The 
<b>GetBestRoute</b> function retrieves the best route to the specified destination IP address.

## -parameters

### -param dwDestAddr [in]

Destination IP address for which to obtain the best route.

### -param dwSourceAddr [in]

Source IP address. This IP address corresponds to an interface on the local computer. If multiple best routes to the destination address exist, the function selects the route that uses this interface. 




This parameter is optional. The caller may specify zero for this parameter.

### -param pBestRoute [out]

Pointer to a 
<a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipforwardrow">MIB_IPFORWARDROW</a> structure containing the best route for the IP address specified by <i>dwDestAddr</i>.

## -returns

If the function succeeds, the return value is NO_ERROR.

If the function fails, use 
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> to obtain the message string for the returned error.

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getbestinterface">GetBestInterface</a>



<a href="/windows/desktop/IpHlp/ip-helper-function-reference">IP Helper Function Reference</a>



<a href="/windows/desktop/IpHlp/ip-helper-start-page">IP Helper Start Page</a>



<a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipforwardrow">MIB_IPFORWARDROW</a>