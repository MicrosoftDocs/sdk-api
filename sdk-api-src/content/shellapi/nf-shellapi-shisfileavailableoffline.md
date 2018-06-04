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

# SHIsFileAvailableOffline function


## -description


Determines whether a file or folder is available for offline use. This function also determines whether the file would be opened from the network, from the local Offline Files cache, or from both locations.


## -parameters




### -param pwszPath

TBD


### -param pdwStatus [out, optional]

Type: <b>LPDWORD</b>

A pointer to a variable of type <b>DWORD</b> that receives one or more of the following flags if the function succeeds.



#### OFFLINE_STATUS_LOCAL (0x01)

If the file is open, it is open in the cache.



#### OFFLINE_STATUS_REMOTE (0x02)

If the file is open, it is open on the server.



#### OFFLINE_STATUS_INCOMPLETE (0x04)

The local copy is currently incomplete. The file cannot be opened in offline mode until it has been synchronized.


#### - pszPath [in]

Type: <b>PCWSTR</b>

A pointer to a string value that specifies the full path to a network file or directory. This path does not need to be in UNC form. If <i>pszPath</i> is not a network path, the function returns E_INVALIDARG.


## -returns



Type: <b>HRESULT</b>

This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The file or directory is cached.  It is available offline unless <b>OFFLINE_STATUS_INCOMPLETE</b> is set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The path is invalid or not a network path. The file or directory is not cached.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The file or directory is not cached.

</td>
</tr>
</table>
 




## -remarks



If <i>pszPath</i> is a directory, <b>SHIsFileAvailableOffline</b> will not return the <b>OFFLINE_STATUS_INCOMPLETE</b> flag.

If <b>SHIsFileAvailableOffline</b> returns both <b>OFFLINE_STATUS_LOCAL</b> and <b>OFFLINE_STATUS_REMOTE</b>, the file or directory is open in both places.  This is common when the server is online.




