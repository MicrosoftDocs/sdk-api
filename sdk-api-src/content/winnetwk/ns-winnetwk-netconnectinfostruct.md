---
UID: NS:winnetwk._NETCONNECTINFOSTRUCT
title: NETCONNECTINFOSTRUCT (winnetwk.h)
description: The NETCONNECTINFOSTRUCT structure contains information about the performance of a network. It is used by the NPGetConnectionPerformance function.
helpviewer_keywords: ["*LPNETCONNECTINFOSTRUCT","LPNETCONNECTINFOSTRUCT","LPNETCONNECTINFOSTRUCT structure pointer [Security]","NETCONNECTINFOSTRUCT","NETCONNECTINFOSTRUCT structure [Security]","WNCON_DYNAMIC","WNCON_FORNETCARD","WNCON_NOTROUTED","WNCON_SLOWLINK","_mnp_netconnectinfostruct","security.netconnectinfostruct","winnetwk/LPNETCONNECTINFOSTRUCT","winnetwk/NETCONNECTINFOSTRUCT"]
old-location: security\netconnectinfostruct.htm
tech.root: security
ms.assetid: 0309667e-cb6c-406f-bb48-ed16602d38b2
ms.date: 12/05/2018
ms.keywords: '*LPNETCONNECTINFOSTRUCT, LPNETCONNECTINFOSTRUCT, LPNETCONNECTINFOSTRUCT structure pointer [Security], NETCONNECTINFOSTRUCT, NETCONNECTINFOSTRUCT structure [Security], WNCON_DYNAMIC, WNCON_FORNETCARD, WNCON_NOTROUTED, WNCON_SLOWLINK, _mnp_netconnectinfostruct, security.netconnectinfostruct, winnetwk/LPNETCONNECTINFOSTRUCT, winnetwk/NETCONNECTINFOSTRUCT'
req.header: winnetwk.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: NETCONNECTINFOSTRUCT, *LPNETCONNECTINFOSTRUCT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _NETCONNECTINFOSTRUCT
 - winnetwk/_NETCONNECTINFOSTRUCT
 - LPNETCONNECTINFOSTRUCT
 - winnetwk/LPNETCONNECTINFOSTRUCT
 - NETCONNECTINFOSTRUCT
 - winnetwk/NETCONNECTINFOSTRUCT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnetwk.h
api_name:
 - NETCONNECTINFOSTRUCT
---

# NETCONNECTINFOSTRUCT structure


## -description

The <b>NETCONNECTINFOSTRUCT</b> structure contains information about the performance of a network. It is used by the 
<a href="/windows/desktop/api/npapi/nf-npapi-npgetconnectionperformance">NPGetConnectionPerformance</a> function.

## -struct-fields

### -field cbStructure

The size of the <b>NETCONNECTINFOSTRUCT</b> structure, in bytes. This is filled in by the caller to indicate the size of the structure passed in. The network provider should leave this field unchanged and can assume that the structure is large enough to contain all fields up to and including <b>dwOptDataSize</b>.

### -field dwFlags

This is a bitmask which may have one or more of the following flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WNCON_FORNETCARD"></a><a id="wncon_fornetcard"></a><dl>
<dt><b>WNCON_FORNETCARD</b></dt>
</dl>
</td>
<td width="60%">
If set, the information returned is for the performance of the netcard used for the connection. This information is returned if information about the actual connection is not available. 




If not set, the information returned is for the current connection with the resource, with any routing degradation taken into consideration.

</td>
</tr>
<tr>
<td width="40%"><a id="WNCON_NOTROUTED"></a><a id="wncon_notrouted"></a><dl>
<dt><b>WNCON_NOTROUTED</b></dt>
</dl>
</td>
<td width="60%">
If set, the connection is not treated as being routed. In other words, routing is not taken into account when estimating the performance. This means actual performance may be much less than the information returned. 




If not set, the connection may be going through routers that limit performance.

</td>
</tr>
<tr>
<td width="40%"><a id="WNCON_SLOWLINK"></a><a id="wncon_slowlink"></a><dl>
<dt><b>WNCON_SLOWLINK</b></dt>
</dl>
</td>
<td width="60%">
If set, the connection is known at some point to be over a medium that is typically slow (for example, a modem using a normal quality phone line). 




Providers that return a value in <b>dwSpeed</b> do not have to set this bit.

</td>
</tr>
<tr>
<td width="40%"><a id="WNCON_DYNAMIC"></a><a id="wncon_dynamic"></a><dl>
<dt><b>WNCON_DYNAMIC</b></dt>
</dl>
</td>
<td width="60%">
If set, some of the information returned is dynamically recalculated. If that is the case, reissuing this request on the connection may return different, more current, information.

</td>
</tr>
</table>

### -field dwSpeed

The speed of the media to the network resource in units of 100bps. For example, a 1,200 baud point-to-point link returns 12.

### -field dwDelay

The delay introduced by the network when sending information, in milliseconds. In other words, the time between when the network starts to send data and the time it is received. This is in addition to any latency that was incorporated into the calculation of <b>dwSpeed</b>, so the value returned will be zero for accessing most resources.

### -field dwOptDataSize

A recommendation for the size of data, in bytes, that is most efficiently sent through the network when an application makes a single request to the network resource. For example, for a disk network resource, this value might be 2048 or 512 when writing a block of data.