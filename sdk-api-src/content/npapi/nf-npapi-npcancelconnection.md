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
 



