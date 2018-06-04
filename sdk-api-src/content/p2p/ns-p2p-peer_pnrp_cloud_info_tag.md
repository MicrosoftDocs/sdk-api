---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# peer_pnrp_cloud_info_tag structure


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

