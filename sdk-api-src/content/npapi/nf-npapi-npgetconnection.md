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

# NPGetConnection function


## -description


Retrieves information about a connection.


## -parameters




### -param lpLocalName [in]

Pointer to the name of the local device the caller is interested in. The network provider can assume this name is syntactically valid.


### -param lpRemoteName [out]

Pointer to a buffer that will receive the remote name used to make the connection. This buffer is allocated by the caller. 


### -param lpnBufferLen

TBD




#### - lpBufferSize [in, out]

Pointer to the size, in characters, of the <i>lpRemoteName</i> buffer. If the call fails because the buffer is not big enough, <i>lpBufferSize</i> is set to the required buffer size.


## -returns



If the function succeeds, it should return WN_SUCCESS. Otherwise, it should return an error code, which can be one of the following:

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
The device specified by <i>lpLocalName</i> is not redirected by this provider.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WN_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The buffer was too small to receive all of the data.

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
 




## -remarks



The <b>NPGetConnection</b> function can return information only about a network connection that is currently connected. To retrieve information about a network connection that is currently disconnected, use 
<a href="https://msdn.microsoft.com/6beb0a9e-4f32-4e83-be78-858185b30521">NPGetConnection3</a>.



