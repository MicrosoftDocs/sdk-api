---
UID: NF:npapi.NPCancelConnection
title: NPCancelConnection function (npapi.h)
description: Disconnects a network connection.
helpviewer_keywords: ["NPCancelConnection","NPCancelConnection function [Security]","_mnp_npcancelconnection","npapi/NPCancelConnection","security.npcancelconnection"]
old-location: security\npcancelconnection.htm
tech.root: security
ms.assetid: e06768b2-760c-48f1-a6a4-896c3ea286f6
ms.date: 12/05/2018
ms.keywords: NPCancelConnection, NPCancelConnection function [Security], _mnp_npcancelconnection, npapi/NPCancelConnection, security.npcancelconnection
req.header: npapi.h
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
req.lib: davclnt.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NPCancelConnection
 - npapi/NPCancelConnection
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Npapi.h
api_name:
 - NPCancelConnection
---

# NPCancelConnection function


## -description

The <b>NPCancelConnection</b> function disconnects a network connection. The changes you make to the connection are remembered if the connection is to a device. If, however, the connection is to a remote network resource, changes are not remembered.

## -parameters

### -param lpName [in]

Pointer to the name of either the redirected local device or the remote network resource to disconnect from.

### -param fForce [in]

Indicates whether the disconnect should continue in the event of open files or jobs on the connection. If <b>FALSE</b> is specified, the call will fail if there are open files or jobs.

## -returns

If the function succeeds, it will return WN_SUCCESS. Otherwise, it will return an error. This can be one of the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
<i>lpName</i> is not a redirected device or is not currently connected to <i>lpName</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_OPEN_FILES</b></dt>
</dl>
</td>
<td width="60%">
There are open files, and <i>fForce</i> was set to <b>FALSE</b>.

</td>
</tr>
</table>

