---
UID: NF:netioapi.FreeMibTable
title: FreeMibTable function (netioapi.h)
description: Frees the buffer allocated by the functions that return tables of network interfaces, addresses, and routes (GetIfTable2 and GetAnycastIpAddressTable, for example).
helpviewer_keywords: ["FreeMibTable","FreeMibTable function [IP Helper]","iphlp.freemibtable","netioapi/FreeMibTable"]
old-location: iphlp\freemibtable.htm
tech.root: IpHlp
ms.assetid: 31c8cdc4-73c7-4e82-8226-c90320046199
ms.date: 12/05/2018
ms.keywords: FreeMibTable, FreeMibTable function [IP Helper], iphlp.freemibtable, netioapi/FreeMibTable
req.header: netioapi.h
req.include-header: Iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - FreeMibTable
 - netioapi/FreeMibTable
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
 - FreeMibTable
---

# FreeMibTable function


## -description

The 
<b>FreeMibTable</b> function  frees the buffer allocated by the functions that return tables of network interfaces, addresses, and routes (<a href="/windows/desktop/api/netioapi/nf-netioapi-getiftable2">GetIfTable2</a> and <a href="/windows/desktop/api/netioapi/nf-netioapi-getanycastipaddresstable">GetAnycastIpAddressTable</a>, for example).

## -parameters

### -param Memory [in]

A pointer to the buffer to free.

## -returns

This function does not return a value.

## -remarks

The <b>FreeMibTable</b> function is defined on Windows Vista and later. 

The <b>FreeMibTable</b> function is used to free the internal buffers used by various functions to retrieve tables of interfaces, addresses, and routes. When these tables are no longer needed, then <b>FreeMibTable</b> should be called to release the memory used by these tables.

## -see-also

<a href="/windows/desktop/api/netioapi/nf-netioapi-getanycastipaddresstable">GetAnycastIpAddressTable</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getifstacktable">GetIfStackTable</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getiftable2">GetIfTable2</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getiftable2ex">GetIfTable2Ex</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getinvertedifstacktable">GetInvertedIfStackTable</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getipforwardtable2">GetIpForwardTable2</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getipinterfacetable">GetIpInterfaceTable</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getipnettable2">GetIpNetTable2</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getippathtable">GetIpPathTable</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getmulticastipaddresstable">GetMulticastIpAddressTable</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getunicastipaddresstable">GetUnicastIpAddressTable</a>