---
UID: NF:netioapi.InitializeIpForwardEntry
title: InitializeIpForwardEntry function (netioapi.h)
description: Initializes a MIB_IPFORWARD_ROW2 structure with default values for an IP route entry on the local computer.
helpviewer_keywords: ["InitializeIpForwardEntry","InitializeIpForwardEntry function [IP Helper]","iphlp.initializeipforwardentry","netioapi/InitializeIpForwardEntry"]
old-location: iphlp\initializeipforwardentry.htm
tech.root: IpHlp
ms.assetid: 1968c4e5-4b28-4387-a918-3326bc80bb3e
ms.date: 12/05/2018
ms.keywords: InitializeIpForwardEntry, InitializeIpForwardEntry function [IP Helper], iphlp.initializeipforwardentry, netioapi/InitializeIpForwardEntry
req.header: netioapi.h
req.include-header: Iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - InitializeIpForwardEntry
 - netioapi/InitializeIpForwardEntry
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
 - InitializeIpForwardEntry
---

# InitializeIpForwardEntry function


## -description

The 
<b>InitializeIpForwardEntry</b> function  initializes a  <b>MIB_IPFORWARD_ROW2</b> structure with default values for an IP route entry on the local computer.

## -parameters

### -param Row [out]

On entry, a pointer to a 
<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ipforward_row2">MIB_IPFORWARD_ROW2</a> structure entry for an IP route entry. On return, the  <b>MIB_IPFORWARD_ROW2</b> structure pointed to by this parameter is initialized with default values for an IP route entry.

## -returns

This function does not return a value.

## -remarks

The <b>InitializeIpForwardEntry</b> function is defined on Windows Vista and later. 

The <b>InitializeIpForwardEntry</b> function must be used to initialize the members of a
    <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ipforward_row2">MIB_IPFORWARD_ROW2</a> structure entry with default values for an IP route entry for later use with the <a href="/windows/desktop/api/netioapi/nf-netioapi-createipforwardentry2">CreateIpForwardEntry2</a> function.  

On input, <b>InitializeIpForwardEntry</b> must be passed a new <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ipforward_row2">MIB_IPFORWARD_ROW2</a> structure to initialize. 

On output, the <b>ValidLifetime</b> and <b>PreferredLifetime</b> members of the <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ipforward_row2">MIB_IPFORWARD_ROW2</a> structure pointed to by <i>Row</i> parameter will be initialized to infinite and the <b>Loopback</b>,  <b>AutoconfigureAddress</b>, <b>Publish</b>, and <b>Immortal</b> members  will be initialized to <b>TRUE</b>. In addition, the <b>SitePrefixLength</b>,   <b>Metric</b>, and  <b>Protocol</b> members are set to an illegal value and other fields are initialized to zero. 

After calling <b>InitializeIpForwardEntry</b>, an application can then change the
    members in the <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ipforward_row2">MIB_IPFORWARD_ROW2</a> entry it wishes to modify, and then call the <a href="/windows/desktop/api/netioapi/nf-netioapi-createipforwardentry2">CreateIpForwardEntry2</a>  to add the new IP route entry to the local computer.

## -see-also

<a href="/windows/desktop/api/netioapi/nf-netioapi-createipforwardentry2">CreateIpForwardEntry2</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-deleteipforwardentry2">DeleteIpForwardEntry2</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getbestroute2">GetBestRoute2</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getipforwardentry2">GetIpForwardEntry2</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getipforwardtable2">GetIpForwardTable2</a>



<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ipforward_row2">MIB_IPFORWARD_ROW2</a>



<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ipforward_table2">MIB_IPFORWARD_TABLE2</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-notifyroutechange2">NotifyRouteChange2</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-setipforwardentry2">SetIpForwardEntry2</a>