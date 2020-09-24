---
UID: NS:tdiinfo.TDIEntityID
title: TDIEntityID (tdiinfo.h)
description: Contains a part of the TDIObjectID structure to represent information about TDI drivers retrieved using the IOCTL_TCP_QUERY_INFORMATION_EX control code.
helpviewer_keywords: ["AT_ENTITY","CL_NL_ENTITY","CL_TL_ENTITY","CO_NL_ENTITY","CO_TL_ENTITY","ER_ENTITY","GENERIC_ENTITY","IF_ENTITY","TDIEntityID","TDIEntityID structure [Windows API]","tdiinfo/TDIEntityID","winprog.tdientityid"]
old-location: winprog\tdientityid.htm
tech.root: winprog
ms.assetid: d95a96b5-c062-44c5-9a66-b27db531800a
ms.date: 12/05/2018
ms.keywords: AT_ENTITY, CL_NL_ENTITY, CL_TL_ENTITY, CO_NL_ENTITY, CO_TL_ENTITY, ER_ENTITY, GENERIC_ENTITY, IF_ENTITY, TDIEntityID, TDIEntityID structure [Windows API], tdiinfo/TDIEntityID, winprog.tdientityid
req.header: tdiinfo.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: TDIEntityID
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TDIEntityID
 - tdiinfo/TDIEntityID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - tdiinfo.h
api_name:
 - TDIEntityID
---

# TDIEntityID structure


## -description

<p class="CCE_Message">[This structure may be altered or unavailable in future versions of Windows.]

Contains a part of the <a href="/windows/desktop/api/tdiinfo/ns-tdiinfo-tdiobjectid">TDIObjectID</a> structure to represent information about TDI drivers retrieved using the <a href="/windows/desktop/api/tcpioctl/ni-tcpioctl-ioctl_tcp_query_information_ex">IOCTL_TCP_QUERY_INFORMATION_EX</a> control code.

## -struct-fields

### -field tei_entity

The type of entity being addressed. This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GENERIC_ENTITY"></a><a id="generic_entity"></a><dl>
<dt><b>GENERIC_ENTITY</b></dt>
</dl>
</td>
<td width="60%">
Used when requesting a list of all entities.

</td>
</tr>
<tr>
<td width="40%"><a id="AT_ENTITY"></a><a id="at_entity"></a><dl>
<dt><b>AT_ENTITY</b></dt>
</dl>
</td>
<td width="60%">
Identifies an address-translation (AT) entity.

</td>
</tr>
<tr>
<td width="40%"><a id="CL_NL_ENTITY"></a><a id="cl_nl_entity"></a><dl>
<dt><b>CL_NL_ENTITY</b></dt>
</dl>
</td>
<td width="60%">
Identifies a connectionless (CL) network-layer (NL) entity.

</td>
</tr>
<tr>
<td width="40%"><a id="CO_NL_ENTITY"></a><a id="co_nl_entity"></a><dl>
<dt><b>CO_NL_ENTITY</b></dt>
</dl>
</td>
<td width="60%">
Identifies a connected, directed-packet (CO) network-layer (NL) entity.

</td>
</tr>
<tr>
<td width="40%"><a id="CL_TL_ENTITY"></a><a id="cl_tl_entity"></a><dl>
<dt><b>CL_TL_ENTITY</b></dt>
</dl>
</td>
<td width="60%">
Identifies a connectionless (CL) transport-layer (TL) entity.

</td>
</tr>
<tr>
<td width="40%"><a id="CO_TL_ENTITY"></a><a id="co_tl_entity"></a><dl>
<dt><b>CO_TL_ENTITY</b></dt>
</dl>
</td>
<td width="60%">
Identifies a connected, directed-packet (CO) transport-layer (TL) entity.

</td>
</tr>
<tr>
<td width="40%"><a id="ER_ENTITY"></a><a id="er_entity"></a><dl>
<dt><b>ER_ENTITY</b></dt>
</dl>
</td>
<td width="60%">
Identifies an Echo-Request/Echo-Reply (ER) entity.

</td>
</tr>
<tr>
<td width="40%"><a id="IF_ENTITY"></a><a id="if_entity"></a><dl>
<dt><b>IF_ENTITY</b></dt>
</dl>
</td>
<td width="60%">
Identifies an interface entity.

</td>
</tr>
</table>

### -field tei_instance

An opaque value that can uniquely identify an entity, if a specific one is being addressed.

## -see-also

<a href="/windows/desktop/api/tcpioctl/ni-tcpioctl-ioctl_tcp_query_information_ex">IOCTL_TCP_QUERY_INFORMATION_EX</a>



<a href="/previous-versions/windows/desktop/mib/management-information-base-reference">Management Information Base
			 Reference</a>



<a href="/windows/desktop/api/tdiinfo/ns-tdiinfo-tdiobjectid">TDIObjectID</a>