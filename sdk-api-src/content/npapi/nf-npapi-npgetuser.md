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

# NPGetUser function


## -description


Retrieves the value of the current default user name or the user name used to establish a network connection.


## -parameters




### -param lpName [in]

Pointer to the name of the local device the caller is interested in, or a remote name for a resource that the user has made a connection to. This parameter may be <b>NULL</b> or the empty string if the caller is interested in the name of the user currently logged on to the system. If a remote name for a resource is passed in, and the user is connected to that resource using different names, it is possible that a provider cannot resolve which user name to return. In this case the provider may make an arbitrary choice amongst the possible user names.


### -param lpUserName [out]

Pointer to a buffer to receive the user name. This should be a name that can be passed into the 
<a href="https://msdn.microsoft.com/37a3988c-18ee-400a-85c3-cc3cbdf015ea">NPAddConnection</a> or 
<a href="https://msdn.microsoft.com/b0d730f7-595e-4ea7-8688-db479dcc40b4">NPAddConnection3</a> function to re-establish the connection with the same user name.


### -param lpnBufferLen

TBD




#### - lpBufferSize [in, out]

Pointer to the size, in characters, of the <i>lpUserName</i> buffer. If the call fails because the buffer is not big enough, this location will be used to return the required buffer size.


## -returns



If the function succeeds, it should return WN_SUCCESS. Otherwise it should return an error code, which can be one of the following.

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
The value in the <i>lpName</i> parameter is not the name of a redirected device or a connected remote name.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The buffer, <i>lpUserName</i>, is too small.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_NO_NETWORK</b></dt>
</dl>
</td>
<td width="60%">
The network is not present.

</td>
</tr>
</table>
 



