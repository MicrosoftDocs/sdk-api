---
UID: NS:p2p.peer_pnrp_cloud_info_tag
title: PEER_PNRP_CLOUD_INFO (p2p.h)
description: Contains information about a Peer Name Resolution Protocol (PNRP) cloud.
helpviewer_keywords: ["*PPEER_PNRP_CLOUD_INFO","PEER_PNRP_CLOUD_INFO","PEER_PNRP_CLOUD_INFO structure [Peer Networking]","PNRP_GLOBAL_SCOPE","PNRP_LINK_LOCAL_SCOPE","PNRP_SCOPE_ANY","PNRP_SITE_LOCAL_SCOPE","PPEER_PNRP_CLOUD_INFO","PPEER_PNRP_CLOUD_INFO structure pointer [Peer Networking]","p2p.peer_pnrp_cloud_info","p2p/PEER_PNRP_CLOUD_INFO","p2p/PPEER_PNRP_CLOUD_INFO"]
old-location: p2p\peer_pnrp_cloud_info.htm
tech.root: p2p
ms.assetid: b6121bae-22b7-4f23-ac8e-08822beef559
ms.date: 12/05/2018
ms.keywords: '*PPEER_PNRP_CLOUD_INFO, PEER_PNRP_CLOUD_INFO, PEER_PNRP_CLOUD_INFO structure [Peer Networking], PNRP_GLOBAL_SCOPE, PNRP_LINK_LOCAL_SCOPE, PNRP_SCOPE_ANY, PNRP_SITE_LOCAL_SCOPE, PPEER_PNRP_CLOUD_INFO, PPEER_PNRP_CLOUD_INFO structure pointer [Peer Networking], p2p.peer_pnrp_cloud_info, p2p/PEER_PNRP_CLOUD_INFO, p2p/PPEER_PNRP_CLOUD_INFO'
req.header: p2p.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only],Windows XP with SP1 with the Advanced Networking Pack for Windows XP
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: PEER_PNRP_CLOUD_INFO, *PPEER_PNRP_CLOUD_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - peer_pnrp_cloud_info_tag
 - p2p/peer_pnrp_cloud_info_tag
 - PPEER_PNRP_CLOUD_INFO
 - p2p/PPEER_PNRP_CLOUD_INFO
 - PEER_PNRP_CLOUD_INFO
 - p2p/PEER_PNRP_CLOUD_INFO
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
 - PEER_PNRP_CLOUD_INFO
---

# PEER_PNRP_CLOUD_INFO structure


## -description

The <b>PEER_PNRP_CLOUD_INFO</b> structure contains information about a Peer Name Resolution Protocol (PNRP) cloud.

## -struct-fields

### -field pwzCloudName

Pointer to a zero-terminated Unicode string that contains the name of the PNRP cloud. The maximum size of this name is 256 characters.

### -field dwScope

Constant value that specifies the network scope of the PNRP cloud.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PNRP_SCOPE_ANY"></a><a id="pnrp_scope_any"></a><dl>
<dt><b>PNRP_SCOPE_ANY</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
All IP addresses are allowed to register with the PNRP cloud.

</td>
</tr>
<tr>
<td width="40%"><a id="PNRP_GLOBAL_SCOPE"></a><a id="pnrp_global_scope"></a><dl>
<dt><b>PNRP_GLOBAL_SCOPE</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The scope is global; all valid  IP addresses are allowed to register with the PNRP cloud.

</td>
</tr>
<tr>
<td width="40%"><a id="PNRP_SITE_LOCAL_SCOPE"></a><a id="pnrp_site_local_scope"></a><dl>
<dt><b>PNRP_SITE_LOCAL_SCOPE</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The scope is site-local; only IP addresses defined for the site are allowed to register with the PNRP cloud.

</td>
</tr>
<tr>
<td width="40%"><a id="PNRP_LINK_LOCAL_SCOPE"></a><a id="pnrp_link_local_scope"></a><dl>
<dt><b>PNRP_LINK_LOCAL_SCOPE</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The scope is link-local; only IP addresses defined for the local area network are allowed to register with the PNRP cloud.

</td>
</tr>
</table>

### -field dwScopeId

The ID of a specific IP address scope defined for the PNRP cloud.

