---
UID: NS:p2p.peer_graph_properties_tag
title: PEER_GRAPH_PROPERTIES (p2p.h)
description: The PEER_GRAPH_PROPERTIES structure contains data about the policy of a peer graph, ID, scope, and other information.
helpviewer_keywords: ["*PPEER_GRAPH_PROPERTIES","PEER_GRAPH_PROPERTIES","PEER_GRAPH_PROPERTIES structure [Peer Networking]","PPEER_GRAPH_PROPERTIES","PPEER_GRAPH_PROPERTIES structure pointer [Peer Networking]","p2p.peer_graph_properties","p2p/PPEER_GRAPH_PROPERTIES","p2p/peer_graph_properties_tag"]
old-location: p2p\peer_graph_properties.htm
tech.root: p2p
ms.assetid: 15b4eeb4-1040-4f07-8e79-2c09aab9f926
ms.date: 12/05/2018
ms.keywords: '*PPEER_GRAPH_PROPERTIES, PEER_GRAPH_PROPERTIES, PEER_GRAPH_PROPERTIES structure [Peer Networking], PPEER_GRAPH_PROPERTIES, PPEER_GRAPH_PROPERTIES structure pointer [Peer Networking], p2p.peer_graph_properties, p2p/PPEER_GRAPH_PROPERTIES, p2p/peer_graph_properties_tag'
req.header: p2p.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only],Windows XP with SP1 with the Advanced Networking Pack forWindows XP
req.target-min-winversvr: None supported
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
req.typenames: PEER_GRAPH_PROPERTIES, *PPEER_GRAPH_PROPERTIES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - peer_graph_properties_tag
 - p2p/peer_graph_properties_tag
 - PPEER_GRAPH_PROPERTIES
 - p2p/PPEER_GRAPH_PROPERTIES
 - PEER_GRAPH_PROPERTIES
 - p2p/PEER_GRAPH_PROPERTIES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - P2P.h
api_name:
 - PEER_GRAPH_PROPERTIES
---

# PEER_GRAPH_PROPERTIES structure


## -description

The <b>PEER_GRAPH_PROPERTIES</b> structure contains data about the policy of a peer graph, ID, scope, and other information.

## -struct-fields

### -field dwSize

Specifies the size, in bytes, of this data structure.  The <b>dwSize</b> member must be set  to the size of <b>PEER_GRAPH_PROPERTIES</b> before calling <a href="/windows/desktop/api/p2p/nf-p2p-peergraphcreate">PeerGraphCreate</a>. This member is required. There is not a default value.

### -field dwFlags

Flags that control  the behavior of a peer in a graph. The default is does not have flags set. The valid value is identified in the following table.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td><b>PEER_GRAPH_PROPERTY_DEFER_EXPIRATION</b></td>
<td>Specifies when to expire a graph record. When a graph is not connected and this flag is set, expiration does not occur until the graph connects to at least one other member. </td>
</tr>
</table>

### -field dwScope

Specifies the  scope in which the peer graph ID is published. The default value is global.  Valid values are identified in the following table.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td><b>PEER_GRAPH_SCOPE_GLOBAL</b></td>
<td>Scope includes the Internet.</td>
</tr>
<tr>
<td><b>PEER_GRAPH_SCOPE_LINK_LOCAL</b></td>
<td>Scope is restricted to a local subnet.</td>
</tr>
<tr>
<td><b>PEER_GRAPH_SCOPE_SITE_LOCAL</b></td>
<td>Scope is restricted to a site, for example, a corporation intranet.</td>
</tr>
</table>

### -field dwMaxRecordSize

Specifies the value that indicates the largest record that can be added to a peer graph. A valid value is zero (0), which indicates that the default maximum record size is used (60 megabytes), and any value between 1024 bytes and 60 megabytes.

### -field pwzGraphId

Specifies the unique identifier for a peer graph.  This ID must be unique for the computer/user pair. This member is required  and has no default value. If the string value is greater than 256 characters (including the null terminator), an error is returned.

### -field pwzCreatorId

Specifies the unique identifier for the creator of a peer graph. This member is required  and has no default value. If the string value is greater than 256 characters (including the null terminator), an error is returned.

### -field pwzFriendlyName

Specifies the friendly name of a peer graph. This member is optional and can be <b>NULL</b>. The default value is <b>NULL</b>. The maximum length of this string is 256 characters, including the null terminator.

### -field pwzComment

Specifies the comment used to describe a peer  graph. This member is optional and can be <b>NULL</b>. The default value is <b>NULL</b>. The maximum length of this string is 512 characters, including the null terminator.

### -field ulPresenceLifetime

Specifies the number of seconds before a presence record  expires. The default value is 300  seconds (5 minutes). Do not set the value  of   <b>ulPresenceLifetime</b> to less than 300 seconds. If this member is set less than the 300  (5 minutes) default value, then undefined behavior can occur.

### -field cPresenceMax

Specifies how many presence records the Peer Infrastructure keeps in a peer graph at one time.   A node that has its presence published can be enumerated by all other nodes with  <a href="/windows/desktop/api/p2p/nf-p2p-peergraphenumnodes">PeerGraphEnumNodes</a>. Specify how presence records for users are published by specifying one of the values identified in the following table.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>-1</td>
<td>Presence records are automatically published for all users.</td>
</tr>
<tr>
<td>0</td>
<td>Presence records are not automatically published.</td>
</tr>
<tr>
<td>1-N</td>
<td>Up to N number of presence records are  published at one time. The presence records that are published are randomly chosen by the Peer Graphing Infrastructure. </td>
</tr>
</table>

## -remarks

An application can force the Peer Graphing Infrastructure to publish presence information by using <a href="/windows/desktop/api/p2p/nf-p2p-peergraphsetpresence">PeerGraphSetPresence</a>.

Only specific  fields in the <b>PEER_GRAPH_PROPERTIES</b> can be updated when calling <a href="/windows/desktop/api/p2p/nf-p2p-peergraphsetproperties">PeerGraphSetProperties</a>. The following members can be updated:

<ul>
<li><b>pwzFriendlyName</b></li>
<li><b>pwzComment</b></li>
<li><b>ulPresenceLifetime</b></li>
<li><b>cPresenceMax</b></li>
</ul>
The remaining members cannot be modified.

## -see-also

<a href="/windows/desktop/api/p2p/nf-p2p-peergraphcreate">PeerGraphCreate</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphgetproperties">PeerGraphGetProperties</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphsetproperties">PeerGraphSetProperties</a>