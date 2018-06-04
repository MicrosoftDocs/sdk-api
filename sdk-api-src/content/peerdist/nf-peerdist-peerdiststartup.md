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

# PeerDistStartup function


## -description


The <b>PeerDistStartup</b> function creates a new Peer Distribution instance handle which must be passed to all other Peer Distribution APIs.


## -parameters




### -param dwVersionRequested [in]

Contains the minimum version of the Peer Distribution requested by the application. The high order byte specifies the minor version number; the low order byte specifies the major version number.


### -param phPeerDist [out]

A pointer to a <b>PEERDIST_INSTANCE_HANDLE</b> variable which upon success receives a newly created handle.


### -param pdwSupportedVersion [out, optional]

A pointer to a variable which, if not <b>NULL</b>, contains the maximum version number that is supported by the Peer Distribution system. The high order byte specifies the minor version number; the low order byte specifies the major version number.  


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>. Otherwise, the function may return one of the following values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEERDIST_ERROR_VERSION_UNSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The requested version is not supported by client side DLL.

</td>
</tr>
</table>
 




## -remarks



<b>PeerDistStartup</b> must be called before any other Peer Distribution functions. When no longer needed, the handle returned by <b>PeerDistStartup</b> should be closed via a call to <a href="https://msdn.microsoft.com/47fe4a77-2895-4d5b-beff-995e12fb0644">PeerDistShutdown</a>.




## -see-also




<a href="https://msdn.microsoft.com/47fe4a77-2895-4d5b-beff-995e12fb0644">PeerDistShutdown</a>
 

 

