---
UID: NS:pnrpdef._PNRP_CLOUD_ID
title: PNRP_CLOUD_ID (pnrpdef.h)
description: The PNRP_CLOUD_ID structure contains the values that define a network cloud.
helpviewer_keywords: ["*PPNRP_CLOUD_ID","PNRP_CLOUD_ID","PNRP_CLOUD_ID structure [Peer Networking]","PPNRP_CLOUD_ID","PPNRP_CLOUD_ID structure pointer [Peer Networking]","p2p.pnrp_cloud_id","pnrpdef/PNRP_CLOUD_ID","pnrpdef/PPNRP_CLOUD_ID"]
old-location: p2p\pnrp_cloud_id.htm
tech.root: p2p
ms.assetid: 8187ce9e-e1a9-4dce-902e-8a1c43b4b047
ms.date: 12/05/2018
ms.keywords: '*PPNRP_CLOUD_ID, PNRP_CLOUD_ID, PNRP_CLOUD_ID structure [Peer Networking], PPNRP_CLOUD_ID, PPNRP_CLOUD_ID structure pointer [Peer Networking], p2p.pnrp_cloud_id, pnrpdef/PNRP_CLOUD_ID, pnrpdef/PPNRP_CLOUD_ID'
req.header: pnrpdef.h
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
req.typenames: PNRP_CLOUD_ID, *PPNRP_CLOUD_ID
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PNRP_CLOUD_ID
 - pnrpdef/_PNRP_CLOUD_ID
 - PPNRP_CLOUD_ID
 - pnrpdef/PPNRP_CLOUD_ID
 - PNRP_CLOUD_ID
 - pnrpdef/PNRP_CLOUD_ID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Pnrpdef.h
api_name:
 - PNRP_CLOUD_ID
---

# PNRP_CLOUD_ID structure


## -description

The <b>PNRP_CLOUD_ID</b> structure contains the values that define a network cloud.

## -struct-fields

### -field AddressFamily

Must be AF_INET6.

### -field Scope

Specifies the scope of the cloud. Use one of the following values:

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>PNRP_SCOPE_ANY</td>
<td>The cloud can be in any scope.</td>
</tr>
<tr>
<td>PNRP_GLOBAL_SCOPE</td>
<td>The cloud must be a global scope.</td>
</tr>
<tr>
<td>PNRP_SITE_LOCAL_SCOPE</td>
<td>The cloud must be a site-local scope.</td>
</tr>
<tr>
<td>PNRP_LINK_LOCAL_SCOPE</td>
<td>The cloud must be a link-local scope.</td>
</tr>
</table>

### -field ScopeId

Specifies the ID for this scope.

## -see-also

<a href="/windows/desktop/api/pnrpns/ns-pnrpns-pnrpcloudinfo">PNRPCLOUDINFO</a>