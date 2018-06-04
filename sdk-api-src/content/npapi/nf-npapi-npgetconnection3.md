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

# NPGetConnection3 function


## -description


Retrieves information about a network connection, even if it is currently disconnected.


## -parameters




### -param lpLocalName [in]

Pointer to the name of the local device the caller is interested in. The provider can assume that this is syntactically valid.


### -param dwLevel [in]

Value that specifies whether the network connection is currently connected or disconnected.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WNGETCON_CONNECTED"></a><a id="wngetcon_connected"></a><dl>
<dt><b>WNGETCON_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The network connection is connected.

</td>
</tr>
<tr>
<td width="40%"><a id="WNGETCON_DISCONNECTED"></a><a id="wngetcon_disconnected"></a><dl>
<dt><b>WNGETCON_DISCONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The network connection is disconnected.

</td>
</tr>
</table>
 


### -param lpBuffer [out]

Void pointer that receives a buffer that contains the requested information.


### -param lpBufferSize [in, out]

Pointer to the size, in characters, of the <i>lpBuffer</i> buffer. If the call fails because the buffer is not big enough, <i>lpBufferSize</i> is set to the required buffer size.


## -returns




						If the function succeeds, it should return WN_SUCCESS.
					

If the function fails, it should return one of the following values.

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



A network connection can exist in three states: connected, disconnected, and unavailable. The <b>NPGetConnection3</b> function cannot retrieve information about network connections that are currently unavailable. It can, however, retrieve information about network connections that are currently disconnected because Windows stores the connection information.



