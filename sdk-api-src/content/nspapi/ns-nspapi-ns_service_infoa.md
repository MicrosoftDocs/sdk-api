---
UID: NS:nspapi._NS_SERVICE_INFOA
title: NS_SERVICE_INFOA (nspapi.h)
description: Contains information about a network service or a network service type in the context of a specified namespace, or a set of default namespaces. (ANSI)
helpviewer_keywords: ["*LPNS_SERVICE_INFOA","*PNS_SERVICE_INFOA","NS_DEFAULT","NS_DNS","NS_MS","NS_NDS","NS_NETBT","NS_NIS","NS_SAP","NS_SERVICE_INFO","NS_SERVICE_INFO structure [Winsock]","NS_SERVICE_INFOA","NS_SERVICE_INFOW","NS_STDA","NS_TCPIP_HOSTS","NS_TCPIP_LOCAL","NS_WINS","NS_X500","_win32_ns_service_info_2","nspapi/NS_SERVICE_INFO","nspapi/NS_SERVICE_INFOA","nspapi/NS_SERVICE_INFOW","winsock.ns_service_info_2"]
old-location: winsock\ns_service_info_2.htm
tech.root: WinSock
ms.assetid: 5bcdeddf-2971-491b-9cf4-70595d3a7ff1
ms.date: 12/05/2018
ms.keywords: '*LPNS_SERVICE_INFOA, *PNS_SERVICE_INFOA, NS_DEFAULT, NS_DNS, NS_MS, NS_NDS, NS_NETBT, NS_NIS, NS_SAP, NS_SERVICE_INFO, NS_SERVICE_INFO structure [Winsock], NS_SERVICE_INFOA, NS_SERVICE_INFOW, NS_STDA, NS_TCPIP_HOSTS, NS_TCPIP_LOCAL, NS_WINS, NS_X500, _win32_ns_service_info_2, nspapi/NS_SERVICE_INFO, nspapi/NS_SERVICE_INFOA, nspapi/NS_SERVICE_INFOW, winsock.ns_service_info_2'
req.header: nspapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: NS_SERVICE_INFOW (Unicode) and NS_SERVICE_INFOA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: NS_SERVICE_INFOA, *PNS_SERVICE_INFOA, *LPNS_SERVICE_INFOA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _NS_SERVICE_INFOA
 - nspapi/_NS_SERVICE_INFOA
 - PNS_SERVICE_INFOA
 - nspapi/PNS_SERVICE_INFOA
 - NS_SERVICE_INFOA
 - nspapi/NS_SERVICE_INFOA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Nspapi.h
api_name:
 - NS_SERVICE_INFO
 - NS_SERVICE_INFOA
 - NS_SERVICE_INFOW
---

# NS_SERVICE_INFOA structure


## -description

The 
<b>NS_SERVICE_INFO</b> structure contains information about a network service or a network service type in the context of a specified namespace, or a set of default namespaces.

## -struct-fields

### -field dwNameSpace

Type: <b>DWORD</b>

Namespace, or a set of default namespaces, to which this service information applies. 




Use one of the following constant values to specify a namespace.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NS_DEFAULT"></a><a id="ns_default"></a><dl>
<dt><b>NS_DEFAULT</b></dt>
</dl>
</td>
<td width="60%">
A set of default namespaces. The set of default namespaces typically includes all the namespaces installed on the system. System administrators, however, can exclude particular namespaces from the set.

</td>
</tr>
<tr>
<td width="40%"><a id="NS_DNS"></a><a id="ns_dns"></a><dl>
<dt><b>NS_DNS</b></dt>
</dl>
</td>
<td width="60%">
The Domain Name System used in the Internet to resolve the name of the host.

</td>
</tr>
<tr>
<td width="40%"><a id="NS_MS"></a><a id="ns_ms"></a><dl>
<dt><b>NS_MS</b></dt>
</dl>
</td>
<td width="60%">
The Microsoft namespace.

</td>
</tr>
<tr>
<td width="40%"><a id="NS_NDS"></a><a id="ns_nds"></a><dl>
<dt><b>NS_NDS</b></dt>
</dl>
</td>
<td width="60%">
The NetWare 4 provider.

</td>
</tr>
<tr>
<td width="40%"><a id="NS_NETBT"></a><a id="ns_netbt"></a><dl>
<dt><b>NS_NETBT</b></dt>
</dl>
</td>
<td width="60%">
The NetBIOS over TCP/IP layer. The operating system registers their computer names with NetBIOS. This namespace is used to convert a computer name to an IP address that uses this registration.

</td>
</tr>
<tr>
<td width="40%"><a id="NS_NIS"></a><a id="ns_nis"></a><dl>
<dt><b>NS_NIS</b></dt>
</dl>
</td>
<td width="60%">
 

</td>
</tr>
<tr>
<td width="40%"><a id="NS_SAP"></a><a id="ns_sap"></a><dl>
<dt><b>NS_SAP</b></dt>
</dl>
</td>
<td width="60%">
The NetWare Service Advertising Protocol. This can access the NetWare bindery, if appropriate. NS_SAP is a dynamic namespace that enables the registration of services.

</td>
</tr>
<tr>
<td width="40%"><a id="NS_STDA"></a><a id="ns_stda"></a><dl>
<dt><b>NS_STDA</b></dt>
</dl>
</td>
<td width="60%">
 

</td>
</tr>
<tr>
<td width="40%"><a id="NS_TCPIP_HOSTS"></a><a id="ns_tcpip_hosts"></a><dl>
<dt><b>NS_TCPIP_HOSTS</b></dt>
</dl>
</td>
<td width="60%">
Lookup value in the &lt;systemroot&gt;\system32\drivers\etc\posts file.

</td>
</tr>
<tr>
<td width="40%"><a id="NS_TCPIP_LOCAL"></a><a id="ns_tcpip_local"></a><dl>
<dt><b>NS_TCPIP_LOCAL</b></dt>
</dl>
</td>
<td width="60%">
Local TCP/IP name resolution mechanisms, including comparisons against the local host name and lookup value in the cache of host to IP address mappings.

</td>
</tr>
<tr>
<td width="40%"><a id="NS_WINS"></a><a id="ns_wins"></a><dl>
<dt><b>NS_WINS</b></dt>
</dl>
</td>
<td width="60%">
The Windows Internet Name System (WINS) namespace.

</td>
</tr>
<tr>
<td width="40%"><a id="NS_X500"></a><a id="ns_x500"></a><dl>
<dt><b>NS_X500</b></dt>
</dl>
</td>
<td width="60%">
The X.500 directory service namespace.

</td>
</tr>
</table>

### -field ServiceInfo

Type: <b>SERVICE_INFO</b>

A 
<a href="/windows/desktop/api/nspapi/ns-nspapi-service_infoa">SERVICE_INFO</a> structure that contains information about a network service or network service type.

## -see-also

<a href="/windows/desktop/api/nspapi/ns-nspapi-service_infoa">SERVICE_INFO</a>

## -remarks

> [!NOTE]
> The nspapi.h header defines NS_SERVICE_INFO as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
